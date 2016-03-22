Intel Galileo
==

## Official Documentation

### Creating a GRUB2 Boot Loader Image from a Linux Host

```sh
    root@jessie:~# apt-get install bison autoconf libopts25-dev flex automake
    xe1gyq@jessie:~$ cd $ZEPHYR_BASE
    xe1gyq@jessie:~/zephyr-project$ ./scripts/build_grub.sh
    ~/zephyr-project/scripts/grub ~/zephyr-project
    Cloning into 'src'...
    remote: Counting objects: 90290, done.
    ...
    make[2]: Leaving directory '/home/xe1gyq/zephyr-project/scripts/grub/src/util/bash-completion.d'
    make[1]: Leaving directory '/home/xe1gyq/zephyr-project/scripts/grub/src'
    ~/zephyr-project/scripts/grub ~/zephyr-project
    ~/zephyr-project
    xe1gyq@jessie:~/zephyr-project$ 
```

### Preparing the Boot Device

```sh
    xe1gyq@jessie:~$ cd $ZEPHYR_BASE/samples/hello_world/nanokernel
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ make BOARD=galileo
```