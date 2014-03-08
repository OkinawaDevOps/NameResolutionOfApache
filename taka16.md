# taka16 用メモ 2014/03/08

## Apache 2.4.7のインストールと手順書の作成
- 13:00 ~
- CentOS 6.3にApache 2.4.7をsourceからインストールし、手順を作成。
- yamaneさんに手順書共有し、Apache関連のタスク完了。
- 手順書は下記に記述
    - https://github.com/OkinawaDevOps/NameResolutionOfApache/blob/master/Apache_install.md


## ソースコード読みの準備など
- 14:40 ~
- 私がソースコード追っかけるのになれていないので、とりあえずソースコード追う準備を実施。その間yamaneさんはガリガリ掘削
- gtagsのインストール
    - 参考URL01 http://d.hatena.ne.jp/m1200056/20121124/1353778084
    - 参考URL02 http://uguisu.skr.jp/Windows/gtags.html
    - インストール履歴 https://github.com/OkinawaDevOps/NameResolutionOfApache/blob/master/gtags_install(CentOS).md


## コード読み
- yamaneさんの軌跡を追っかけてみる事に。
    - https://github.com/OkinawaDevOps/NameResolutionOfApache/blob/master/yamane.md

### 履歴
#### resolver のwordを含むファイルの検索
```
[root@centos6 httpd-2.4.7]# pwd
/usr/local/src/httpd-2.4.7
[root@centos6 httpd-2.4.7]# find server |xargs grep resolver 2>/dev/null
server/vhost.c:                "check resolver configuration.";
バイナリー・ファイルserver/.libs/libmain.aは一致しました
バイナリー・ファイルserver/vhost.oは一致しました
[root@centos6 httpd-2.4.7]# cat server/vhost.c | grep resolver
                "check resolver configuration.";
[root@centos6 httpd-2.4.7]#
```

195行目にresolver の文字列あり `apr_sockaddr_info_get`という関数
```
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

```


#### `srclib/apr/network_io/unix/sockaddr.c|595|`にて`apr_sockaddr_info_get`の定義を確認
```
APR_DECLARE(apr_status_t) apr_sockaddr_info_get(apr_sockaddr_t **sa,
                                                const char *hostname,
                                                apr_int32_t family, apr_port_t port,
                                                apr_int32_t flags, apr_pool_t *p)
```


上記の処理は`find_addresses`の戻り値を返す
```
return find_addresses(sa, hostname, family, port, flags, p);
```

今日はここまでで時間切れ


## 振り返り
- 久々のSourceからのApacheインストール
- 普段自分が行っているサーバの設定がサーバ上で動くミドルウェアでどのようにして読み込まれているかという疑問に取り組む事ができた。
- 上のレイヤーばっかりでなくそこから少し下のレイヤーに掘り下げていくのも楽しい。特にあまり下の方の知識がないまま過ごしている自分にとっては刺激があった。
- gtags便利。今回初めて使ったが、下を掘っていく際に助けられました。
- 次回はLinuxのスクリプト(ifup や ifdown, /etc/init.d/network)などを読んでみたいかも。
