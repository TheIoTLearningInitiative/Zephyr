# Intel Mexico Zephyr Workshop v2.0

- [Gitbook @FlavioDevNull The Zephyr Book](https://flaviodevnull.gitbooks.io/the-zephyr-book/content/)

# Important Links Shared

- [ENC28J60 Stand-alone Ethernet Controller with SPI - Microchip](http://ww1.microchip.com/downloads/en/devicedoc/39662a.pdf)

# Labs, Qemu

```sh
abraham@aarcemor-desk:~/zephyr-project/samples/hello_world/nanokernel$ make pristine
abraham@aarcemor-desk:~/zephyr-project/samples/hello_world/nanokernel$ make BOARD=qemu_x86
abraham@aarcemor-desk:~/zephyr-project/samples/hello_world/nanokernel$ make BOARD=qemu
```

```sh
abraham@aarcemor-desk:~/zephyr-project/samples/hello_world/nanokernel$ make qemumake[1]: Entering directory `/home/abraham/zephyr-project'
make[2]: Entering directory `/home/abraham/zephyr-project/samples/hello_world/nanokernel/outdir'
  Using /home/abraham/zephyr-project as source for kernel
  GEN     ./Makefile
  CHK     include/generated/version.h
  CHK     misc/generated/configs.c
  CHK     include/generated/offsets.h
To exit from QEMU enter: 'CTRL+a, x'
[QEMU] CPU: qemu32
Hello World!
```