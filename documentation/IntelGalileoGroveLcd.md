# Grove LCD

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

