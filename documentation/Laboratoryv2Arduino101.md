# Laboratory Arduino 101

```sh
user@workstation:~$ screen /dev/ttyUSB0 115200
```

```sh

```

```sh
pymelab@workstation:~/Intel/Zephyr/zephyr-project/samples/hello_world/microkernel$ sudo dfu-util -a x86_app -D outdir/arduino_101/zephyr.bin 
sudo: imposible resolver el anfitrión workstation
dfu-util 0.5

(C) 2005-2008 by Weston Schmidt, Harald Welte and OpenMoko Inc.
(C) 2010-2011 Tormod Volden (DfuSe support)
This program is Free Software and has ABSOLUTELY NO WARRANTY

dfu-util does currently only support DFU version 1.0

Opening DFU USB device... ID 8087:0aba
Run-time device DFU version 0011
Found DFU: [8087:0aba] devnum=0, cfg=1, intf=0, alt=2, name="x86_app"
Claiming USB DFU Interface...
Setting Alternate Setting #2 ...
Determining device status: state = dfuIDLE, status = 0
dfuIDLE, continuing
DFU mode device DFU version 0011
Device returned transfer size 2048
No valid DFU suffix signature
Warning: File has no DFU suffix
bytes_per_hash=248
Copying data from PC to DFU device
Starting download: [##################################################] finished!
state(2) = dfuIDLE, status(0) = No error condition is present
Done!
pymelab@workstation:~/Intel/Zephyr/zephyr-project/samples/hello_world/microkernel$ 
```