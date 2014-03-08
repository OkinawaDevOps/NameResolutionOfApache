# Apacheインストール手順

## 環境
- OS : CentOS 6.3 64bit
    - インストールパッケージは base, Development tools
- Kernel : `2.6.32-279.el6.x86_64`
- Apache : Version 2.4.7


## インストール手順

### 事前作業
```
cd /usr/local/src

wget http://ftp.kddilabs.jp/infosystems/apache//httpd/httpd-2.4.7.tar.gz
wget http://ftp.yz.yamagata-u.ac.jp/pub/network/apache//apr/apr-1.5.0.tar.gz
wget http://ftp.kddilabs.jp/infosystems/apache//apr/apr-util-1.5.3.tar.gz

tar xvzf httpd-2.4.7.tar.gz

cd /usr/local/src/httpd-2.4.7/srclib
tar xvzf /usr/local/src/apr-1.5.0.tar.gz
tar xvzf /usr/local/src/apr-util-1.5.3.tar.gz
mv apr-1.5.0 apr
mv apr-util-1.5.3 apr-util
cd ../

yum install openssl-devel
yum -y install pcre-devel
```

### Apacheインストール

```
./configure --prefix=/usr/local/httpd-2.4.7 --with-included-apr --enable-so --enable-ssl=shared --enable-rewrite=shared --with-mpm=prefork

make

make install
```

### 起動スクリプト設置
```
ln -s /usr/local/httpd-2.4.7 /usr/local/apache2

cp -fp /usr/local/src/httpd-2.4.7/build/rpm/httpd.init /etc/init.d/httpd

cd /etc/init.d

vi httpd

変更箇所は下記

[root@centos6 init.d]# diff /usr/local/src/httpd-2.4.7/build/rpm/httpd.init httpd
43c43
< prog=$(basename $0 | sed -e 's/^[SK][0-9][0-9]//')
---
> prog=httpd
45,46c45,46
< if [ -f /etc/sysconfig/${prog} ]; then
<         . /etc/sysconfig/${prog}
---
> if [ -f /etc/sysconfig/httpd ]; then
>         . /etc/sysconfig/httpd
60,62c60,62
< httpd=${HTTPD-/usr/sbin/httpd}
< pidfile=${PIDFILE-/var/run/${prog}.pid}
< lockfile=${LOCKFILE-/var/lock/subsys/${prog}}
---
> httpd=${HTTPD-/usr/local/apache2/bin/httpd}
> pidfile=${PIDFILE-/usr/local/apache2/logs/httpd.pid}
> lockfile=${LOCKFILE-/var/lock/subsys/httpd}
67c67
<      CONFFILE=/etc/httpd/conf/httpd.conf
---
>      CONFFILE=/usr/local/apache2/conf/httpd.conf
[root@centos6 init.d]# 
```


### path設定
```
cp -fp /usr/local/src/aem-middle/profile.apache.sh /etc/profile.d/apache.sh

vi /etc/profile.d/apache.sh


if ! echo ${PATH} | /bin/grep -q /usr/local/apache2/bin ; then
    PATH=/usr/local/apache2/bin:${PATH}
fi


source /etc/profile.d/apache.sh
```


### 自動起動設定
```
chkconfig --add httpd
chkconfig httpd on
chkconfig --list httpd
```

### Apacheの起動
```
service httpd start
```


