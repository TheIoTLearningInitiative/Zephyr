# Samples Shell

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
