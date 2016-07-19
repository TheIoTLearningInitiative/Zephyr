# Laboratory Arduino 101

```sh
abraham@aarcemor-desk:~$ screen /dev/ttyUSB0 115200
```

# Samples Shell

```sh
abraham@aarcemor-desk:~/zephyr-project$ ls
arch    drivers  Kbuild          kernel   MAINTAINERS   misc     scripts
boards  ext      Kconfig         lib      Makefile      net      tests
doc     include  Kconfig.zephyr  LICENSE  Makefile.inc  samples  zephyr-env.sh
abraham@aarcemor-desk:~/zephyr-project$ cd samples/shell/
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ ls
Makefile  prj.conf  src
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ cd src/
abraham@aarcemor-desk:~/zephyr-project/samples/shell/src$ ls
main.c  Makefile
abraham@aarcemor-desk:~/zephyr-project/samples/shell/src$ 
```

## Environment Checking

```sh
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ echo $ZEPHYR_BASE
/home/abraham/zephyr-project
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ echo $ZEPHYR_GCC_VARIANT
zephyr
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ 
```

## Application Template

```sh
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ ls -lhR 
.:
total 12K
-rw-rw-r-- 1 abraham abraham   95 jun 25 12:13 Makefile
-rw-rw-r-- 1 abraham abraham   72 jun 25 12:13 prj.conf
drwxrwxr-x 2 abraham abraham 4.0K jun 25 12:13 src

./src:
total 8.0K
-rw-rw-r-- 1 abraham abraham 1.4K jun 25 12:13 main.c
-rw-rw-r-- 1 abraham abraham   16 jun 25 12:13 Makefile
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ 
```