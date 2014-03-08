# Apache における名前解決について

DevOpsOkinawa#2 にて当日自宅対応になってしまい欠席を余儀 (与儀) なくされた @taka16_o さんと @yamanetoshi とでソースを掘削して確認してみました。

## はじめに

以下を使用することが前提となっています。

- Apache 2.4.7
- apr 1.5
- apr-util 1.5.3
- pcre-devel (libpcre3-dev)

また、ソースコードをコンパイルする Debian GNU/Linux で言うと binutils あたりのパケジも導入必須となるはずです。

## コンパイル

補足資料として @taka16_o さんに以下を投入してもらっています。

- [Apacheインストール手順](apache_install.md)
- [PHP 導入に関する資料](PHP_install.md)

[Apacheインストール手順](apache_install.md) を参考に以下を実行。

     $ ./configure --with-included-apr --enable-so --enable-ssl=shared --enable-rewrite=shared --with-mpm=prefork

apr が srclib 配下に必要、ということで apr および apr-util を取得して展開してリトライした結果、以下メセジが出力され途中終了。

    configure: error: pcre-config for libpcre not found. PCRE is required and available from http://pcre.org/

libpcre3-dev パケジを導入することで対処。

    $ sudo apt-get install libpcre3-dev

これで configure が通った。make もしています。make install は勿論していません。

## 名前解決部分のアタリを付けてみた

以下で grep してみた。下手な鉄砲の何発かの一つ。

    $ find server |xargs grep resolver 2>/dev/null

server/vhost.c あたりに check resolver configuration なる文字列あり。

    if (strcmp(host, "*") == 0 || strcasecmp(host, "_default_") == 0) {
        rv = apr_sockaddr_info_get(&my_addr, NULL, APR_UNSPEC, port, 0, p);
        if (rv) {
            return "Could not determine a wildcard address ('0.0.0.0') -- "
                "check resolver configuration.";
        }
    }
    else {
        rv = apr_sockaddr_info_get(&my_addr, host, APR_UNSPEC, port, 0, p);
        if (rv != APR_SUCCESS) {
            ap_log_error(APLOG_MARK, APLOG_ERR, rv, NULL, APLOGNO(00547)
                "Could not resolve host name %s -- ignoring!", host);
            return NULL;
        }
    }

apr_sockaddr_info_get がアヤシいと判断。しかし server ディレクトリの中には見当らず。

## 再度確認

実は上記は事前にちょっとだけ確認してみた記録でその時には srclib 配下に apr および apr-util を展開していませんでした。ので展開されている状態で再度 gtags -v を実行。

その後、apr_sockaddr_info_get を検索してみると srclib/apr/network_io/unix/sockaddr.c で定義を確認。

    APR_DECLARE(apr_status_t) apr_sockaddr_info_get(apr_sockaddr_t **sa,
                                                    const char *hostname, 
                                                    apr_int32_t family, apr_port_t port,
                                                    apr_int32_t flags, apr_pool_t *p)
    {

この中を確認していくと良いようですが、APR_DECLARE とかなマクロの確認もした方が良いのかどうか。

## apr_sockaddr_info_get 手続き掘削

この手続きは find_address なる手続きの戻りを戻しているだけな模様 (ざっくり)。

    return find_addresses(sa, hostname, family, port, flags, 

この手続きは HAVE_GETADDRINFO というマクロが定義されているかどうかで定義が変わる形になっているようです。

HAVE_GETADDRINFO の場合、呼び出される find_addresses 手続きから以下を呼び出しています。

    return call_resolver(sa, hostname, family, port, flags, p);

で、この call_resolver が getaddrinfo を呼び出していますね。これは IP アドレスでの名前解決を行なうための手続きだったはずです。

glib か
----------------

openbsd の ML なナニを見つけたのですが getaddrinfo は最初の一発目のみ resolver を使い (res_init という手続き?)、そこでしか resolv.conf が読み込まれない、という記述がありました。

つーことは glib のソース見なきゃ、なのかorz

ソースファイルは lib/libc/net/getaddrinfo.c らしいがどうなるか。

ソース入手
---------------

以下で良いのかどうか。

    $ apt-get source libc6

これで落ちてきたのが eglibc-2.13 のソースになってますがこれで良いのかどうか。

そして sysdeps/posix/getaddrinfo.c の以下の部分が核心?

      if (naddrs > 1)
        {
          /* Read the config file.  */
          __libc_once_define (static, once);
          __typeof (once) old_once = once;
          __libc_once (once, gaiconf_init);

そろそろ時間切れ。


