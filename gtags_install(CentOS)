# gnu global(gtags)のインストール


## インストール履歴
```
[root@centos6 ~]# cd /usr/local/src/
[root@centos6 src]# wget http://tamacom.com/global/global-6.2.10.tar.gz
--2014-03-08 15:16:40--  http://tamacom.com/global/global-6.2.10.tar.gz
tamacom.com をDNSに問いあわせています... 59.106.191.155
tamacom.com|59.106.191.155|:80 に接続しています... 接続しました。
HTTP による接続要求を送信しました、応答を待っています... 200 OK
長さ: 1366667 (1.3M) [application/x-gzip]
`global-6.2.10.tar.gz' に保存中

100%[==============================================================================>] 1,366,667   2.36M/s 時間 0.6s    

2014-03-08 15:16:41 (2.36 MB/s) - `global-6.2.10.tar.gz' へ保存完了 [1366667/1366667]

[root@centos6 src]# ls -lt
合計 24580
drwxr-xr-x. 17  101   101     4096  3月  8 14:51 2014 php-5.3.27
drwxr-xr-x. 12  501 games     4096  3月  8 12:56 2014 httpd-2.4.7
-rw-r--r--.  1 root root   1366667  1月 16 14:38 2014 global-6.2.10.tar.gz
-rw-r--r--.  1 root root   6747087 11月 23 02:49 2013 httpd-2.4.7.tar.gz
-rw-r--r--.  1 root root    874462 11月 17 02:52 2013 apr-util-1.5.3.tar.gz
-rw-r--r--.  1 root root   1016391 11月 17 02:50 2013 apr-1.5.0.tar.gz
-rw-r--r--.  1 root root  15008639  7月 11 08:40 2013 php-5.3.27.tar.gz
-rw-r--r--.  1 root root     14540 11月  6 00:31 2012 epel-release-6-8.noarch.rpm
-rw-r--r--.  1 root root     12352  7月 10 06:49 2010 libmcrypt-devel-2.5.8-9.el6.x86_64.rpm
-rw-r--r--.  1 root root     97932  7月 10 06:47 2010 libmcrypt-2.5.8-9.el6.x86_64.rpm
-rw-r--r--.  1 root root      1649  5月 12 10:25 2010 RPM-GPG-KEY-EPEL-6
[root@centos6 src]# tar zxvf global-6.2.10.tar.gz
[root@centos6 src]# ls -lt
合計 24584
drwxr-xr-x. 17  101   101     4096  3月  8 14:51 2014 php-5.3.27
drwxr-xr-x. 12  501 games     4096  3月  8 12:56 2014 httpd-2.4.7
-rw-r--r--.  1 root root   1366667  1月 16 14:38 2014 global-6.2.10.tar.gz
drwxr-xr-x. 20  501 wheel     4096  1月 16 13:58 2014 global-6.2.10
-rw-r--r--.  1 root root   6747087 11月 23 02:49 2013 httpd-2.4.7.tar.gz
-rw-r--r--.  1 root root    874462 11月 17 02:52 2013 apr-util-1.5.3.tar.gz
-rw-r--r--.  1 root root   1016391 11月 17 02:50 2013 apr-1.5.0.tar.gz
-rw-r--r--.  1 root root  15008639  7月 11 08:40 2013 php-5.3.27.tar.gz
-rw-r--r--.  1 root root     14540 11月  6 00:31 2012 epel-release-6-8.noarch.rpm
-rw-r--r--.  1 root root     12352  7月 10 06:49 2010 libmcrypt-devel-2.5.8-9.el6.x86_64.rpm
-rw-r--r--.  1 root root     97932  7月 10 06:47 2010 libmcrypt-2.5.8-9.el6.x86_64.rpm
-rw-r--r--.  1 root root      1649  5月 12 10:25 2010 RPM-GPG-KEY-EPEL-6
[root@centos6 src]# cd global-6.2.10
[root@centos6 global-6.2.10]#
[root@centos6 global-6.2.10]# ./configure 
checking for a BSD-compatible install... /usr/bin/install -c
checking whether build environment is sane... yes
checking for a thread-safe mkdir -p... /bin/mkdir -p
checking for gawk... gawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking for gcc... gcc
checking whether the C compiler works... yes
checking for C compiler default output file name... a.out
checking for suffix of executables... 
checking whether we are cross compiling... no
checking for suffix of object files... o
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ISO C89... none needed
checking whether gcc understands -c and -o together... yes
checking for style of include used by make... GNU
checking dependency style of gcc... gcc3
checking whether make sets $(MAKE)... (cached) yes
checking for emacs... no
checking for xemacs... no
checking where .elc files should go... ${datadir}/emacs/site-lisp
checking for perl... /usr/bin/perl
checking for ar... ar
checking how to run the C preprocessor... gcc -E
checking for grep that handles long lines and -e... /bin/grep
checking for egrep... /bin/grep -E
checking for ANSI C header files... yes
checking for sys/types.h... yes
checking for sys/stat.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for memory.h... yes
checking for strings.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for unistd.h... yes
checking minix/config.h usability... no
checking minix/config.h presence... no
checking for minix/config.h... no
checking whether it is safe to define __EXTENSIONS__... yes
checking build system type... x86_64-unknown-linux-gnu
checking host system type... x86_64-unknown-linux-gnu
checking how to print strings... printf
checking for a sed that does not truncate output... /bin/sed
checking for fgrep... /bin/grep -F
checking for ld used by gcc... /usr/bin/ld
checking if the linker (/usr/bin/ld) is GNU ld... yes
checking for BSD- or MS-compatible name lister (nm)... /usr/bin/nm -B
checking the name lister (/usr/bin/nm -B) interface... BSD nm
checking whether ln -s works... yes
checking the maximum length of command line arguments... 1966080
checking whether the shell understands some XSI constructs... yes
checking whether the shell understands "+="... yes
checking how to convert x86_64-unknown-linux-gnu file names to x86_64-unknown-linux-gnu format... func_convert_file_noop
checking how to convert x86_64-unknown-linux-gnu file names to toolchain format... func_convert_file_noop
checking for /usr/bin/ld option to reload object files... -r
checking for objdump... objdump
checking how to recognize dependent libraries... pass_all
checking for dlltool... no
checking how to associate runtime and link libraries... printf %s\n
checking for archiver @FILE support... @
checking for strip... strip
checking for ranlib... ranlib
checking command to parse /usr/bin/nm -B output from gcc object... ok
checking for sysroot... no
checking for mt... no
checking if : is a manifest tool... no
checking for dlfcn.h... yes
checking for objdir... .libs
checking if gcc supports -fno-rtti -fno-exceptions... no
checking for gcc option to produce PIC... -fPIC -DPIC
checking if gcc PIC flag -fPIC -DPIC works... yes
checking if gcc static flag -static works... no
checking if gcc supports -c -o file.o... yes
checking if gcc supports -c -o file.o... (cached) yes
checking whether the gcc linker (/usr/bin/ld -m elf_x86_64) supports shared libraries... yes
checking whether -lc should be explicitly linked in... no
checking dynamic linker characteristics... GNU/Linux ld.so
checking how to hardcode library paths into programs... immediate
checking for shl_load... no
checking for shl_load in -ldld... no
checking for dlopen... no
checking for dlopen in -ldl... yes
checking whether a program can dlopen itself... yes
checking whether a statically linked program can dlopen itself... yes
checking whether stripping libraries is possible... yes
checking if libtool supports shared libraries... yes
checking whether to build shared libraries... yes
checking whether to build static libraries... yes
checking which extension is used for runtime loadable modules... .so
checking which variable specifies run-time module search path... LD_LIBRARY_PATH
checking for the default library search path... /lib /usr/lib /usr/lib64/mysql 
checking for library containing dlopen... -ldl
checking for dlerror... yes
checking for shl_load... (cached) no
checking for shl_load in -ldld... (cached) no
checking for dld_link in -ldld... no
checking for _ prefix in compiled symbols... no
checking whether deplibs are loaded by dlopen... yes
checking for argz.h... yes
checking for error_t... yes
checking for argz_add... yes
checking for argz_append... yes
checking for argz_count... yes
checking for argz_create_sep... yes
checking for argz_insert... yes
checking for argz_next... yes
checking for argz_stringify... yes
checking if argz actually works... yes
checking whether libtool supports -dlopen/-dlpreopen... yes
checking for ltdl.h... no
checking where to find libltdl headers... -I${top_srcdir}/libltdl
checking where to find libltdl library... ${top_build_prefix}libltdl/libltdlc.la
checking for unistd.h... (cached) yes
checking for dl.h... no
checking for sys/dl.h... no
checking for dld.h... no
checking for mach-o/dyld.h... no
checking for dirent.h... yes
checking for closedir... yes
checking for opendir... yes
checking for readdir... yes
checking for strlcat... no
checking for strlcpy... no
checking limits.h usability... yes
checking limits.h presence... yes
checking for limits.h... yes
checking for string.h... (cached) yes
checking for unistd.h... (cached) yes
checking stdarg.h usability... yes
checking stdarg.h presence... yes
checking for stdarg.h... yes
checking sys/time.h usability... yes
checking sys/time.h presence... yes
checking for sys/time.h... yes
checking fcntl.h usability... yes
checking fcntl.h presence... yes
checking for fcntl.h... yes
checking sys/resource.h usability... yes
checking sys/resource.h presence... yes
checking for sys/resource.h... yes
checking for dirent.h that defines DIR... yes
checking for library containing opendir... none required
checking for ANSI C header files... (cached) yes
checking whether stat file-mode macros are broken... no
checking whether time.h and sys/time.h may both be included... yes
checking for an ANSI C-conforming const... yes
checking for off_t... yes
checking for size_t... yes
checking for struct stat.st_blksize... yes
checking whether byte ordering is bigendian... no
checking for int8_t... yes
checking for int16_t... yes
checking for int32_t... yes
checking for u_int8_t... yes
checking for u_int16_t... yes
checking for u_int32_t... yes
checking for ssize_t... yes
checking for caddr_t... yes
checking size of int... 4
checking size of short... 2
checking size of char... 1
checking for working alloca.h... yes
checking for alloca... yes
checking for stdlib.h... (cached) yes
checking for unistd.h... (cached) yes
checking for sys/param.h... yes
checking for getpagesize... yes
checking for working mmap... yes
checking for working memcmp... yes
checking return type of signal handlers... void
checking for strftime... yes
checking for getcwd... yes
checking for putenv... yes
checking for lstat... yes
checking for snprintf... yes
checking for index... yes
checking for rindex... yes
checking for bzero... yes
checking for bcmp... yes
checking for bcopy... yes
checking for strchr... yes
checking for strrchr... yes
checking for memset... yes
checking for memcmp... yes
checking for memmove... yes
checking for putc_unlocked... yes
checking for getc_unlocked... yes
checking for gettimeofday... yes
checking for getrusage... yes
checking whether we are using the GNU DJGPP compiler... no
configure: checking "location of ncurses.h file"...
configure: error: curses library is required but not found.
If you are not going to use gtags-cscope, please try ./configure --disable-gtagscscope
[root@centos6 global-6.2.10]# gc
gcc         gcj-dbtool  gcore       gcov        
[root@centos6 global-6.2.10]# yum install ncurses-devel
Loaded plugins: downloadonly, fastestmirror, security
Loading mirror speeds from cached hostfile
 * base: www.ftp.ne.jp
 * extras: www.ftp.ne.jp
 * updates: www.ftp.ne.jp
Setting up Install Process
Resolving Dependencies
--> Running transaction check
---> Package ncurses-devel.x86_64 0:5.7-3.20090208.el6 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

========================================================================================================================
 Package                        Arch                    Version                             Repository             Size
========================================================================================================================
Installing:
 ncurses-devel                  x86_64                  5.7-3.20090208.el6                  base                  642 k

Transaction Summary
========================================================================================================================
Install       1 Package(s)

Total download size: 642 k
Installed size: 1.7 M
Is this ok [y/N]: y
Downloading Packages:
ncurses-devel-5.7-3.20090208.el6.x86_64.rpm                                                      | 642 kB     00:00     
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
  Installing : ncurses-devel-5.7-3.20090208.el6.x86_64                                                              1/1 
  Verifying  : ncurses-devel-5.7-3.20090208.el6.x86_64                                                              1/1 

Installed:
  ncurses-devel.x86_64 0:5.7-3.20090208.el6                                                                             

Complete!
[root@centos6 global-6.2.10]# 
[root@centos6 global-6.2.10]# ./configure 
checking for a BSD-compatible install... /usr/bin/install -c
checking whether build environment is sane... yes
checking for a thread-safe mkdir -p... /bin/mkdir -p
checking for gawk... gawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking for gcc... gcc
checking whether the C compiler works... yes
checking for C compiler default output file name... a.out
checking for suffix of executables... 
checking whether we are cross compiling... no
checking for suffix of object files... o
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ISO C89... none needed
checking whether gcc understands -c and -o together... yes
checking for style of include used by make... GNU
checking dependency style of gcc... gcc3
checking whether make sets $(MAKE)... (cached) yes
checking for emacs... no
checking for xemacs... no
checking where .elc files should go... ${datadir}/emacs/site-lisp
checking for perl... /usr/bin/perl
checking for ar... ar
checking how to run the C preprocessor... gcc -E
checking for grep that handles long lines and -e... /bin/grep
checking for egrep... /bin/grep -E
checking for ANSI C header files... yes
checking for sys/types.h... yes
checking for sys/stat.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for memory.h... yes
checking for strings.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for unistd.h... yes
checking minix/config.h usability... no
checking minix/config.h presence... no
checking for minix/config.h... no
checking whether it is safe to define __EXTENSIONS__... yes
checking build system type... x86_64-unknown-linux-gnu
checking host system type... x86_64-unknown-linux-gnu
checking how to print strings... printf
checking for a sed that does not truncate output... /bin/sed
checking for fgrep... /bin/grep -F
checking for ld used by gcc... /usr/bin/ld
checking if the linker (/usr/bin/ld) is GNU ld... yes
checking for BSD- or MS-compatible name lister (nm)... /usr/bin/nm -B
checking the name lister (/usr/bin/nm -B) interface... BSD nm
checking whether ln -s works... yes
checking the maximum length of command line arguments... 1966080
checking whether the shell understands some XSI constructs... yes
checking whether the shell understands "+="... yes
checking how to convert x86_64-unknown-linux-gnu file names to x86_64-unknown-linux-gnu format... func_convert_file_noop
checking how to convert x86_64-unknown-linux-gnu file names to toolchain format... func_convert_file_noop
checking for /usr/bin/ld option to reload object files... -r
checking for objdump... objdump
checking how to recognize dependent libraries... pass_all
checking for dlltool... no
checking how to associate runtime and link libraries... printf %s\n
checking for archiver @FILE support... @
checking for strip... strip
checking for ranlib... ranlib
checking command to parse /usr/bin/nm -B output from gcc object... ok
checking for sysroot... no
checking for mt... no
checking if : is a manifest tool... no
checking for dlfcn.h... yes
checking for objdir... .libs
checking if gcc supports -fno-rtti -fno-exceptions... no
checking for gcc option to produce PIC... -fPIC -DPIC
checking if gcc PIC flag -fPIC -DPIC works... yes
checking if gcc static flag -static works... no
checking if gcc supports -c -o file.o... yes
checking if gcc supports -c -o file.o... (cached) yes
checking whether the gcc linker (/usr/bin/ld -m elf_x86_64) supports shared libraries... yes
checking whether -lc should be explicitly linked in... no
checking dynamic linker characteristics... GNU/Linux ld.so
checking how to hardcode library paths into programs... immediate
checking for shl_load... no
checking for shl_load in -ldld... no
checking for dlopen... no
checking for dlopen in -ldl... yes
checking whether a program can dlopen itself... yes
checking whether a statically linked program can dlopen itself... yes
checking whether stripping libraries is possible... yes
checking if libtool supports shared libraries... yes
checking whether to build shared libraries... yes
checking whether to build static libraries... yes
checking which extension is used for runtime loadable modules... .so
checking which variable specifies run-time module search path... LD_LIBRARY_PATH
checking for the default library search path... /lib /usr/lib /usr/lib64/mysql 
checking for library containing dlopen... -ldl
checking for dlerror... yes
checking for shl_load... (cached) no
checking for shl_load in -ldld... (cached) no
checking for dld_link in -ldld... no
checking for _ prefix in compiled symbols... no
checking whether deplibs are loaded by dlopen... yes
checking for argz.h... yes
checking for error_t... yes
checking for argz_add... yes
checking for argz_append... yes
checking for argz_count... yes
checking for argz_create_sep... yes
checking for argz_insert... yes
checking for argz_next... yes
checking for argz_stringify... yes
checking if argz actually works... yes
checking whether libtool supports -dlopen/-dlpreopen... yes
checking for ltdl.h... no
checking where to find libltdl headers... -I${top_srcdir}/libltdl
checking where to find libltdl library... ${top_build_prefix}libltdl/libltdlc.la
checking for unistd.h... (cached) yes
checking for dl.h... no
checking for sys/dl.h... no
checking for dld.h... no
checking for mach-o/dyld.h... no
checking for dirent.h... yes
checking for closedir... yes
checking for opendir... yes
checking for readdir... yes
checking for strlcat... no
checking for strlcpy... no
checking limits.h usability... yes
checking limits.h presence... yes
checking for limits.h... yes
checking for string.h... (cached) yes
checking for unistd.h... (cached) yes
checking stdarg.h usability... yes
checking stdarg.h presence... yes
checking for stdarg.h... yes
checking sys/time.h usability... yes
checking sys/time.h presence... yes
checking for sys/time.h... yes
checking fcntl.h usability... yes
checking fcntl.h presence... yes
checking for fcntl.h... yes
checking sys/resource.h usability... yes
checking sys/resource.h presence... yes
checking for sys/resource.h... yes
checking for dirent.h that defines DIR... yes
checking for library containing opendir... none required
checking for ANSI C header files... (cached) yes
checking whether stat file-mode macros are broken... no
checking whether time.h and sys/time.h may both be included... yes
checking for an ANSI C-conforming const... yes
checking for off_t... yes
checking for size_t... yes
checking for struct stat.st_blksize... yes
checking whether byte ordering is bigendian... no
checking for int8_t... yes
checking for int16_t... yes
checking for int32_t... yes
checking for u_int8_t... yes
checking for u_int16_t... yes
checking for u_int32_t... yes
checking for ssize_t... yes
checking for caddr_t... yes
checking size of int... 4
checking size of short... 2
checking size of char... 1
checking for working alloca.h... yes
checking for alloca... yes
checking for stdlib.h... (cached) yes
checking for unistd.h... (cached) yes
checking for sys/param.h... yes
checking for getpagesize... yes
checking for working mmap... yes
checking for working memcmp... yes
checking return type of signal handlers... void
checking for strftime... yes
checking for getcwd... yes
checking for putenv... yes
checking for lstat... yes
checking for snprintf... yes
checking for index... yes
checking for rindex... yes
checking for bzero... yes
checking for bcmp... yes
checking for bcopy... yes
checking for strchr... yes
checking for strrchr... yes
checking for memset... yes
checking for memcmp... yes
checking for memmove... yes
checking for putc_unlocked... yes
checking for getc_unlocked... yes
checking for gettimeofday... yes
checking for getrusage... yes
checking whether we are using the GNU DJGPP compiler... no
configure: checking "location of ncurses.h file"...
Found ncurses on /usr/include/ncurses.h
checking for ncurses version... 5.7
checking for an ANSI C-conforming const... (cached) yes
checking for mode_t... yes
checking for pid_t... yes
checking for size_t... (cached) yes
checking for sighandler_t... no
checking for sigsetjmp... yes
checking for fixkeypad... no
checking for strerror... yes
checking for home-etc support... no
checking for pread/pwrite support... no
checking for exuberant ctags program... using /usr/bin/ctags
checking whether exuberant ctags --gtags works... no
checking for POSIX sort program... using /bin/sort
checking default mode of sitekeys directory... 755
checking that generated files are newer than configure... done
configure: creating ./config.status
config.status: creating Makefile
config.status: creating gtags.conf
config.status: creating Doxyfile
config.status: creating libutil/langmap.h
config.status: creating htags/global.cgi.tmpl
config.status: creating htags/completion.cgi.tmpl
config.status: creating libutil/Makefile
config.status: creating gtags/Makefile
config.status: creating htags/Makefile
config.status: creating libdb/Makefile
config.status: creating global/Makefile
config.status: creating gozilla/Makefile
config.status: creating gtags-cscope/Makefile
config.status: creating globash/Makefile
config.status: creating htags-refkit/Makefile
config.status: creating libglibc/Makefile
config.status: creating doc/Makefile
config.status: creating icons/Makefile
config.status: creating jquery/Makefile
config.status: creating jquery/images/Makefile
config.status: creating script/Makefile
config.status: creating libparser/Makefile
config.status: creating plugin-factory/Makefile
config.status: creating libltdl/Makefile
config.status: creating config.h
config.status: executing depfiles commands
config.status: executing libtool commands
[root@centos6 global-6.2.10]#
[root@centos6 global-6.2.10]# make
[root@centos6 global-6.2.10]# make install
Making install in libglibc
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/libglibc' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/libglibc' に入ります
make[2]: `install-exec-am' に対して行うべき事はありません.
make[2]: `install-data-am' に対して行うべき事はありません.
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/libglibc' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/libglibc' から出ます
Making install in libutil
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/libutil' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/libutil' に入ります
make[2]: `install-exec-am' に対して行うべき事はありません.
make[2]: `install-data-am' に対して行うべき事はありません.
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/libutil' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/libutil' から出ます
Making install in libparser
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/libparser' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/libparser' に入ります
make[2]: `install-exec-am' に対して行うべき事はありません.
make[2]: `install-data-am' に対して行うべき事はありません.
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/libparser' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/libparser' から出ます
Making install in libltdl
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/libltdl' に入ります
make  install-am
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/libltdl' に入ります
make[3]: ディレクトリ `/usr/local/src/global-6.2.10/libltdl' に入ります
make[3]: ディレクトリ `/usr/local/src/global-6.2.10/libltdl' から出ます
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/libltdl' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/libltdl' から出ます
Making install in plugin-factory
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/plugin-factory' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/plugin-factory' に入ります
make[2]: `install-exec-am' に対して行うべき事はありません.
 /bin/mkdir -p '/usr/local/share/gtags'
 /usr/bin/install -c -m 644 PLUGIN_HOWTO '/usr/local/share/gtags'
 /bin/mkdir -p '/usr/local/lib/gtags'
 /bin/sh ../libtool   --mode=install /usr/bin/install -c   exuberant-ctags.la user-custom.la '/usr/local/lib/gtags'
libtool: install: /usr/bin/install -c .libs/exuberant-ctags.so /usr/local/lib/gtags/exuberant-ctags.so
libtool: install: /usr/bin/install -c .libs/exuberant-ctags.lai /usr/local/lib/gtags/exuberant-ctags.la
libtool: install: /usr/bin/install -c .libs/user-custom.so /usr/local/lib/gtags/user-custom.so
libtool: install: /usr/bin/install -c .libs/user-custom.lai /usr/local/lib/gtags/user-custom.la
libtool: install: /usr/bin/install -c .libs/exuberant-ctags.a /usr/local/lib/gtags/exuberant-ctags.a
libtool: install: chmod 644 /usr/local/lib/gtags/exuberant-ctags.a
libtool: install: ranlib /usr/local/lib/gtags/exuberant-ctags.a
libtool: install: /usr/bin/install -c .libs/user-custom.a /usr/local/lib/gtags/user-custom.a
libtool: install: chmod 644 /usr/local/lib/gtags/user-custom.a
libtool: install: ranlib /usr/local/lib/gtags/user-custom.a
libtool: finish: PATH="/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin:/root/bin:/sbin" ldconfig -n /usr/local/lib/gtags
----------------------------------------------------------------------
Libraries have been installed in:
   /usr/local/lib/gtags

If you ever happen to want to link against installed libraries
in a given directory, LIBDIR, you must either use libtool, and
specify the full pathname of the library, or use the `-LLIBDIR'
flag during linking and do at least one of the following:
   - add LIBDIR to the `LD_LIBRARY_PATH' environment variable
     during execution
   - add LIBDIR to the `LD_RUN_PATH' environment variable
     during linking
   - use the `-Wl,-rpath -Wl,LIBDIR' linker flag
   - have your system administrator add LIBDIR to `/etc/ld.so.conf'

See any operating system documentation about shared libraries for
more information, such as the ld(1) and ld.so(8) manual pages.
----------------------------------------------------------------------
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/plugin-factory' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/plugin-factory' から出ます
Making install in libdb
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/libdb' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/libdb' に入ります
make[2]: `install-exec-am' に対して行うべき事はありません.
make[2]: `install-data-am' に対して行うべき事はありません.
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/libdb' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/libdb' から出ます
Making install in global
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/global' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/global' に入ります
 /bin/mkdir -p '/usr/local/bin'
  /bin/sh ../libtool   --mode=install /usr/bin/install -c global '/usr/local/bin'
libtool: install: /usr/bin/install -c global /usr/local/bin/global
 /bin/mkdir -p '/usr/local/share/man/man1'
 /usr/bin/install -c -m 644 global.1 '/usr/local/share/man/man1'
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/global' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/global' から出ます
Making install in gozilla
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/gozilla' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/gozilla' に入ります
 /bin/mkdir -p '/usr/local/bin'
  /bin/sh ../libtool   --mode=install /usr/bin/install -c gozilla '/usr/local/bin'
libtool: install: /usr/bin/install -c gozilla /usr/local/bin/gozilla
 /bin/mkdir -p '/usr/local/share/man/man1'
 /usr/bin/install -c -m 644 gozilla.1 '/usr/local/share/man/man1'
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/gozilla' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/gozilla' から出ます
Making install in gtags
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/gtags' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/gtags' に入ります
 /bin/mkdir -p '/usr/local/bin'
  /bin/sh ../libtool   --mode=install /usr/bin/install -c gtags '/usr/local/bin'
libtool: install: /usr/bin/install -c gtags /usr/local/bin/gtags
 /bin/mkdir -p '/usr/local/share/man/man1'
 /usr/bin/install -c -m 644 gtags.1 '/usr/local/share/man/man1'
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/gtags' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/gtags' から出ます
Making install in htags
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/htags' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/htags' に入ります
 /bin/mkdir -p '/usr/local/bin'
  /bin/sh ../libtool   --mode=install /usr/bin/install -c htags '/usr/local/bin'
libtool: install: /usr/bin/install -c htags /usr/local/bin/htags
 /bin/mkdir -p '/usr/local/share/gtags'
 /usr/bin/install -c -m 644 global.cgi.tmpl ghtml.cgi.tmpl completion.cgi.tmpl bless.sh.tmpl jscode_suggest.tmpl jscode_treeview.tmpl style.css.tmpl '/usr/local/share/gtags'
 /bin/mkdir -p '/usr/local/share/man/man1'
 /usr/bin/install -c -m 644 htags.1 '/usr/local/share/man/man1'
make  install-data-hook
make[3]: ディレクトリ `/usr/local/src/global-6.2.10/htags' に入ります
dir="/usr/local/var/gtags/sitekeys"; \
	if [ ! -d $dir ]; then \
		/bin/mkdir -p $dir; \
		chmod 755 $dir; \
	fi
make[3]: ディレクトリ `/usr/local/src/global-6.2.10/htags' から出ます
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/htags' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/htags' から出ます
Making install in htags-refkit
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/htags-refkit' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/htags-refkit' に入ります
make[2]: `install-exec-am' に対して行うべき事はありません.
make[2]: `install-data-am' に対して行うべき事はありません.
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/htags-refkit' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/htags-refkit' から出ます
Making install in globash
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/globash' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/globash' に入ります
 /bin/mkdir -p '/usr/local/bin'
 /usr/bin/install -c globash '/usr/local/bin'
 /bin/mkdir -p '/usr/local/share/gtags'
 /usr/bin/install -c -m 644 globash.rc '/usr/local/share/gtags'
 /bin/mkdir -p '/usr/local/share/man/man1'
 /usr/bin/install -c -m 644 globash.1 '/usr/local/share/man/man1'
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/globash' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/globash' から出ます
Making install in doc
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/doc' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/doc' に入ります
make[2]: `install-exec-am' に対して行うべき事はありません.
 /bin/mkdir -p '/usr/local/share/info'
 /usr/bin/install -c -m 644 ./global.info '/usr/local/share/info'
 install-info --info-dir='/usr/local/share/info' '/usr/local/share/info/global.info'
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/doc' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/doc' から出ます
Making install in icons
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/icons' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/icons' に入ります
make[2]: `install-exec-am' に対して行うべき事はありません.
 /bin/mkdir -p '/usr/local/share/gtags/icons'
 /usr/bin/install -c -m 644 index.png c.png text.png dir.png back.png help.png first.png last.png left.png right.png top.png bottom.png n_first.png n_last.png n_left.png n_right.png n_top.png n_bottom.png pglobe.png '/usr/local/share/gtags/icons'
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/icons' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/icons' から出ます
Making install in jquery
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/jquery' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/jquery' に入ります
make[2]: `install-exec-am' に対して行うべき事はありません.
 /bin/mkdir -p '/usr/local/share/gtags/jquery'
 /usr/bin/install -c -m 644 jquery.js jquery.suggest.css jquery.suggest.js jquery.treeview.css jquery.treeview.js '/usr/local/share/gtags/jquery'
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/jquery' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/jquery' から出ます
Making install in jquery/images
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/jquery/images' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/jquery/images' に入ります
make[2]: `install-exec-am' に対して行うべき事はありません.
 /bin/mkdir -p '/usr/local/share/gtags/jquery/images'
 /usr/bin/install -c -m 644 file.png folder-closed.png folder.png minus.png plus.png treeview-black-line.png treeview-black.png treeview-default-line.png treeview-default.png treeview-famfamfam-line.png treeview-famfamfam.png treeview-gray-line.png treeview-gray.png treeview-red-line.png treeview-red.png '/usr/local/share/gtags/jquery/images'
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/jquery/images' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/jquery/images' から出ます
Making install in script
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/script' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/script' に入ります
make[2]: `install-exec-am' に対して行うべき事はありません.
 /bin/mkdir -p '/usr/local/share/gtags'
 /usr/bin/install -c -m 644 SERVERSIDE_HOWTO '/usr/local/share/gtags'
 /bin/mkdir -p '/usr/local/share/gtags/script'
 /usr/bin/install -c -m 644 less-global elvis-global global-client gtags-client htags-client '/usr/local/share/gtags/script'
make  install-data-hook
make[3]: ディレクトリ `/usr/local/src/global-6.2.10/script' に入ります
if cd /usr/local/share/gtags/script; then \
		chmod 755 less-global elvis-global global-client gtags-client htags-client; \
	fi
make[3]: ディレクトリ `/usr/local/src/global-6.2.10/script' から出ます
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/script' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/script' から出ます
Making install in gtags-cscope
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/gtags-cscope' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/gtags-cscope' に入ります
 /bin/mkdir -p '/usr/local/bin'
  /bin/sh ../libtool   --mode=install /usr/bin/install -c gtags-cscope '/usr/local/bin'
libtool: install: /usr/bin/install -c gtags-cscope /usr/local/bin/gtags-cscope
 /bin/mkdir -p '/usr/local/share/man/man1'
 /usr/bin/install -c -m 644 gtags-cscope.1 '/usr/local/share/man/man1'
make[2]: ディレクトリ `/usr/local/src/global-6.2.10/gtags-cscope' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10/gtags-cscope' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10' に入ります
make[2]: ディレクトリ `/usr/local/src/global-6.2.10' に入ります
make[2]: `install-exec-am' に対して行うべき事はありません.
 /bin/mkdir -p '/usr/local/share/gtags'
 /usr/bin/install -c -m 644 AUTHORS COPYING COPYING.LIB ChangeLog FAQ INSTALL LICENSE NEWS README THANKS BOKIN_MODEL BOKIN_MODEL_FAQ DONORS BUILD_TOOLS gtags.conf gtags.el gtags.pl gtags.vim gtags-cscope.vim elvis.rc elvis-2.2_0.patch ctags-5.8.patch '/usr/local/share/gtags'
make[2]: ディレクトリ `/usr/local/src/global-6.2.10' から出ます
make[1]: ディレクトリ `/usr/local/src/global-6.2.10' から出ます
[root@centos6 global-6.2.10]#
[root@centos6 global-6.2.10]# cp /usr/local/share/gtags/gtags.
gtags.conf  gtags.el    gtags.pl    gtags.vim   
[root@centos6 global-6.2.10]# cp /usr/local/share/gtags/gtags.vim /usr/share/vim/vim
vim72/    vimfiles/ 
[root@centos6 global-6.2.10]# cp /usr/local/share/gtags/gtags.vim /usr/share/vim/vim72/plugin/
[root@centos6 global-6.2.10]#
```
