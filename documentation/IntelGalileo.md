# Intel Galileo

# Official Documentation

## Creating a GRUB2 Boot Loader Image from a Linux Host

```sh
user@workstation:~$ sudo apt-get install bison autoconf libopts25-dev flex automake
```

```sh
user@workstation:~$ cd $ZEPHYR_BASE
```

```sh
user@workstation:~/Intel/Zephyr/zephyr-project$ ls
arch         doc      fs       Kconfig         lib          Makefile      net      tests
boards       drivers  include  Kconfig.zephyr  LICENSE      Makefile.inc  samples  usb
defaults.tc  ext      Kbuild   kernel          MAINTAINERS  misc          scripts  zephyr-env.sh
```

```sh
user@workstation:~/Intel/Zephyr/zephyr-project$ ./scripts/build_grub.sh
...
...
~/Intel/Zephyr/zephyr-project/scripts/grub ~/Intel/Zephyr/zephyr-project
~/Intel/Zephyr/zephyr-project
```

```sh
user@workstation:~/Intel/Zephyr/zephyr-project$ samples/hello_world/nanokernel/
```

```sh
user@workstation:~/Intel/Zephyr/zephyr-project/samples/hello_world/nanokernel$ make pristine && make BOARD=galileo
...
...
  LINK    zephyr.lnk
  SIDT    staticIdt.o
  LINK    zephyr.elf
  BIN     zephyr.bin
```

```sh
user@workstation:~/Intel/Zephyr/zephyr-project/samples/hello_world/nanokernel$ dmesg
...
...
[470637.182794] mmc0: new SD card at address e624
[470637.188637] mmcblk0: mmc0:e624 SU01G 968 MiB 
[470637.189523]  mmcblk0: p1
```



## Preparing the Boot Device

```sh
    xe1gyq@jessie:~$ cd $ZEPHYR_BASE/samples/hello_world/nanokernel
```

```sh
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
```

```sh
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ ls outdir/zephyr.strip 
arch     ext               include               kernel       linker.cmd  net      staticIdt.o  zephyr.elf  zephyr.map
boards   final-linker.cmd  int_vector_alloc.o    lib          Makefile    scripts  usb          zephyr.lnk  zephyr.stat
drivers  fs                irq_int_vector_map.o  libzephyr.a  misc        src      zephyr.bin   zephyr.lst  zephyr.strip
```

```sh
xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ file outdir/zephyr.strip 
    outdir/zephyr.strip: ELF 32-bit LSB executable, Intel 80386, version 1 (SYSV), statically linked, stripped
    
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ mount -t vfat /dev/sdb1 /media/sdcard/
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ mkdir /media/sdcard/efi
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ mkdir /media/sdcard/efi/boot
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ mkdir /media/sdcard/kernel
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ cp $ZEPHYR_BASE/samples/hello_world/nanokernel/outdir/zephyr.strip /media/cdrom/kernel/
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ cp $ZEPHYR_BASE/scripts/grub/bin/grub.efi /media/cdrom/efi/boot/bootia32.efi
    xe1gyq@jessie:~/zephyr-project/samples/hello_world/nanokernel$ nano /media/cdrom/efi/boot/grub.cfg
```

```sh
set default=0
set timeout=10

menuentry "Zephyr Kernel" {
   multiboot /kernel/zephyr.strip
}
```

Booting the Galileo Board

```sh
    Press [Enter] to directly boot.
    Press [F7]    to show boot menu options.
```

```sh
    Booting `Zephyr Kernel'
    WARNING: no console will be available to OS
    error: no suitable video mode found.
```

# Let´s Get To Work

## Samples Shell

Compile and run samples/shell

```sh
    xe1gyq@jessie:~/zephyr-project/samples/shell$ cd $ZEPHYR_BASE/samples/shell
    xe1gyq@jessie:~/zephyr-project/samples/shell$ make distclean
    xe1gyq@jessie:~/zephyr-project/samples/shell$ make BOARD=galileo
    xe1gyq@jessie:~/zephyr-project/samples/shell# mount -t vfat /dev/sdb1 /media/sdcard/
    xe1gyq@jessie:~/zephyr-project/samples/shell# cp $ZEPHYR_BASE/samples/shell/outdir/zephyr.strip /media/sdcard/kernel/
    xe1gyq@jessie:~/zephyr-project/samples/shell$ umount /media/sdcard/
    xe1gyq@jessie:~/zephyr-project/samples/shell$  
```

Booting the Galileo Board

```sh
    WARNING: no console will be available to OS
    error: no suitable video mode found.
    shell> help
    Available commands:
    help
    ping
    ticks
    highticks
    shell> 
    shell> ping
    pong
    shell> ticks
    ticks: 2616
    shell> highticks
    highticks: 438339144
    shell> 
```

## Samples Drivers Grove-Lcd

```sh
    xe1gyq@jessie:~/zephyr-project$ cd $ZEPHYR_BASE/samples/drivers/grove_lcd
    xe1gyq@jessie:~/zephyr-project/samples/drivers/grove_lcd$ make distclean
    xe1gyq@jessie:~/zephyr-project/samples/drivers/grove_lcd$ make BOARD=galileo
    xe1gyq@jessie:~/zephyr-project/samples/drivers/grove_lcd# mount -t vfat /dev/sdb1 /media/sdcard/
    xe1gyq@jessie:~/zephyr-project/samples/drivers/grove_lcd# cp $ZEPHYR_BASE/samples/drivers/grove_lcd/outdir/zephyr.strip /media/sdcard/kernel/
    xe1gyq@jessie:~/zephyr-project/samples/drivers/grove_lcd$ umount /media/sdcard/
    xe1gyq@jessie:~/zephyr-project/samples/drivers/grove_lcd$ 
```

Booting the Galileo Board ... LCD Working?