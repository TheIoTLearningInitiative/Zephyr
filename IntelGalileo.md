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
    xe1gyq@jessie:~/zephyr-project$ ls $ZEPHYR_BASE/scripts/grub/bin/grub.efi
    /home/xe1gyq/zephyr-project/scripts/grub/bin/grub.efi
    xe1gyq@jessie:~/zephyr-project$ file $ZEPHYR_BASE/scripts/grub/bin/grub.efi
    /home/xe1gyq/zephyr-project/scripts/grub/bin/grub.efi: PE32 executable (EFI application) Intel 80386 (stripped to external PDB), for MS Windows
    xe1gyq@jessie:~/zephyr-project$ 
```

### Preparing the Boot Device

```sh
    xe1gyq@jessie:~$ cd $ZEPHYR_BASE/samples/hello_world/nanokernel
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ make BOARD=galileo
    make[1]: Entering directory '/home/xe1gyq/zephyr-project'
    make[2]: Entering directory '/home/xe1gyq/zephyr-project/samples/hello_world/nanokernel/outdir'
      Using /home/xe1gyq/zephyr-project as source for kernel
      GEN     ./Makefile
      CHK     include/generated/version.h
      CHK     misc/generated/configs.c
      CHK     include/generated/offsets.h
    make[2]: Leaving directory '/home/xe1gyq/zephyr-project/samples/hello_world/nanokernel/outdir'
    make[1]: Leaving directory '/home/xe1gyq/zephyr-project'
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ ls outdir/zephyr.strip 
    outdir/zephyr.strip
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ file outdir/zephyr.strip 
    outdir/zephyr.strip: ELF 32-bit LSB executable, Intel 80386, version 1 (SYSV), statically linked, stripped
    
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ mount -t vfat /dev/sdb1 /media/sdcard/
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ mkdir /media/sdcard/efi
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ mkdir /media/sdcard/efi/boot
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ mkdir /media/sdcard/kernel
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ cp $ZEPHYR_BASE/samples/hello_world/nanokernel/outdir/zephyr.strip /media/cdrom/kernel/
    
```