# やまね用メモ

## コンパイル

     $ ./configure --with-included-apr --enable-so --enable-ssl=shared --enable-rewrite=shared --with-mpm=prefork

- apr (Apache Portable Runtime Library) 必要

srclib 配下に apr および apr-util を取得して展開し、リトライすると以下のメセジで途中終了。


    configure: error: pcre-config for libpcre not found. PCRE is required and available from http://pcre.org/

以下で対処。

    $ sudo apt-get install libpcre3-dev

これで configure が通った。

