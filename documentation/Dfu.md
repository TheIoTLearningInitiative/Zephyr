# DFU

> Device Firmware Upgrade

```sh
abraham@aarcemor-desk:~$ git clone https://github.com/Stefan-Schmidt/dfu-util.git
Cloning into 'dfu-util'...
remote: Counting objects: 1051, done.
remote: Compressing objects: 100% (326/326), done.
remote: Total 1051 (delta 718), reused 1051 (delta 718), pack-reused 0
Receiving objects: 100% (1051/1051), 209.68 KiB | 147.00 KiB/s, done.
Resolving deltas: 100% (718/718), done.
Checking connectivity... done.
abraham@aarcemor-desk:~$ cd dfu-util/
abraham@aarcemor-desk:~/dfu-util$ ls
autogen.sh  configure.ac  device-logs  doc          README  TODO
ChangeLog   COPYING       DEVICES.txt  Makefile.am  src     www
abraham@aarcemor-desk:~/dfu-util$ 
```

```sh
abraham@aarcemor-desk:~/dfu-util$ ./autogen.sh 
autoreconf: Entering directory `.'
autoreconf: configure.ac: not using Gettext
autoreconf: running: aclocal 
autoreconf: configure.ac: tracing
autoreconf: configure.ac: creating directory m4
autoreconf: configure.ac: not using Libtool
autoreconf: running: /usr/bin/autoconf
autoreconf: running: /usr/bin/autoheader
autoreconf: running: automake --add-missing --copy --no-force
configure.ac:16: installing 'm4/compile'
configure.ac:7: installing 'm4/install-sh'
configure.ac:7: installing 'm4/missing'
src/Makefile.am: installing 'm4/depcomp'
autoreconf: Leaving directory `.'
abraham@aarcemor-desk:~/dfu-util$ 
```

```sh
abraham@aarcemor-desk:~/dfu-util$ ls
aclocal.m4      ChangeLog    configure.ac  DEVICES.txt  Makefile.am  src
autogen.sh      config.h.in  COPYING       doc          Makefile.in  TODO
autom4te.cache  configure    device-logs   m4           README       www
abraham@aarcemor-desk:~/dfu-util$ ./configure 
```

```sh
abraham@aarcemor-desk:~/dfu-util$ dfu-util -V
dfu-util 0.7

Copyright 2005-2008 Weston Schmidt, Harald Welte and OpenMoko Inc.
Copyright 2010-2012 Tormod Volden and Stefan Schmidt
This program is Free Software and has ABSOLUTELY NO WARRANTY
Please report bugs to dfu-util@lists.gnumonks.org

abraham@aarcemor-desk:~/dfu-util$ 
```