Intel Galileo
==

### Official Documentation

## Creating a GRUB2 Boot Loader Image from a Linux Host

```sh
    root@jessie:~# apt-get install bison autoconf libopts25-dev flex automake
    xe1gyq@jessie:~$ cd $ZEPHYR_BASE
    xe1gyq@jessie:~/zephyr-project$ ./scripts/build_grub.sh
    ~/zephyr-project/scripts/grub ~/zephyr-project
    Cloning into 'src'...
    remote: Counting objects: 90290, done.
    ...
    
```

## Preparing the Boot Device

```sh
    xe1gyq@jessie:~$ cd $ZEPHYR_BASE/samples/hello_world/nanokernel
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ make BOARD=galileo
```