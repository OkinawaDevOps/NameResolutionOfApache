# やまね用メモ

## コンパイル

     $ ./configure --with-included-apr --enable-so --enable-ssl=shared --enable-rewrite=shared --with-mpm=prefork

- apr (Apache Portable Runtime Library) 必要

srclib 配下に apr および apr-util を取得して展開し、リトライすると以下のメセジで途中終了。


    configure: error: pcre-config for libpcre not found. PCRE is required and available from http://pcre.org/

以下で対処。

    $ sudo apt-get install libpcre3-dev

これで configure が通った。

## アタリを付けた方法

以下で grep してみた。

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

