# X86 Emulation (QEMU)

```sh
pymelab@workstation:~/zephyr-project$ ls
arch         drivers  Kbuild          lib          Makefile.inc  scripts
boards       ext      Kconfig         LICENSE      misc          tests
defaults.tc  fs       Kconfig.zephyr  MAINTAINERS  net           usb
doc          include  kernel          Makefile     samples       zephyr-env.sh
```

```sh
user@workstation:~/zephyr-project/samples/hello_world/microkernel$ make BOARD=qemu_x86 qemu
make[1]: Entering directory '/home/xe1gyq/zephyr-project'
make[2]: Entering directory '/home/xe1gyq/zephyr-project/samples/hello_world/microkernel/outdir'
  Using /home/xe1gyq/zephyr-project as source for kernel
  GEN     ./Makefile
  CHK     include/generated/version.h
  CHK     misc/generated/configs.c
  CHK     include/generated/offsets.h
  CHK     misc/generated/sysgen/prj.mdef
To exit from QEMU enter: 'CTRL+a, x'
[QEMU] CPU: qemu32
qemu-system-i386: pci_add_option_rom: failed to find romfile "vgabios-cirrus.bin"
Hello World!
QEMU: Terminated
make[2]: Leaving directory '/home/xe1gyq/zephyr-project/samples/hello_world/microkernel/outdir'
make[1]: Leaving directory '/home/xe1gyq/zephyr-project'
user@workstation:~/zephyr-project/samples/hello_world/microkernel$ 
```
