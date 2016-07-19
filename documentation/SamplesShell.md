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

## Make Menuconfig

```sh
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ make menuconfig
make[1]: Entering directory `/home/abraham/zephyr-project'
make[2]: Entering directory `/home/abraham/zephyr-project/samples/shell/outdir'
  GEN     ./Makefile
scripts/kconfig/mconf Kconfig


*** End of the configuration.
*** Execute 'make' to start the build or try 'make help'.

make[2]: Leaving directory `/home/abraham/zephyr-project/samples/shell/outdir'
make[1]: Leaving directory `/home/abraham/zephyr-project'
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ 
```

## Project Configuration

```sh
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ cat prj.conf 
CONFIG_CONSOLE_HANDLER=y
CONFIG_CONSOLE_HANDLER_SHELL=y
CONFIG_PRINTK=y
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ 
```

## Compilation

```sh
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ ls
Makefile  outdir  prj.conf  src
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ make BOARD=arduino_101_factory
Using /home/abraham/zephyr-project/boards/arduino_101/arduino_101_factory_defconfig as base
Merging /home/abraham/zephyr-project/kernel/configs/nano.config
Merging prj.conf
#
# configuration written to .config
#
make[1]: Entering directory `/home/abraham/zephyr-project'
make[2]: Entering directory `/home/abraham/zephyr-project/samples/shell/outdir'
  GEN     ./Makefile
scripts/kconfig/conf --silentoldconfig Kconfig
make[2]: Leaving directory `/home/abraham/zephyr-project/samples/shell/outdir'
make[2]: Entering directory `/home/abraham/zephyr-project/samples/shell/outdir'
  Using /home/abraham/zephyr-project as source for kernel
  GEN     ./Makefile
  CHK     include/generated/version.h
  UPD     include/generated/version.h
  HOSTCC  scripts/gen_idt/gen_idt.o
  HOSTLD  scripts/gen_idt/gen_idt
  CHK     misc/generated/configs.c
  UPD     misc/generated/configs.c
  CHK     include/generated/offsets.h
  UPD     include/generated/offsets.h
  LD      lib/libc/minimal/source/stdlib/built-in.o
  CC      lib/libc/minimal/source/stdout/fprintf.o
  CC      lib/libc/minimal/source/stdout/prf.o
  CC      lib/libc/minimal/source/stdout/sprintf.o
  CC      lib/libc/minimal/source/stdout/stdout_console.o
  LD      lib/libc/minimal/source/stdout/built-in.o
  CC      lib/libc/minimal/source/string/string.o
  LD      lib/libc/minimal/source/string/built-in.o
  LD      lib/libc/minimal/source/built-in.o
  LD      lib/libc/minimal/built-in.o
  LD      lib/libc/built-in.o
  LD      lib/built-in.o
  CC      kernel/nanokernel/nano_fiber.o
  CC      kernel/nanokernel/nano_lifo.o
  CC      kernel/nanokernel/nano_fifo.o
  CC      kernel/nanokernel/nano_stack.o
  CC      kernel/nanokernel/nano_sys_clock.o
  CC      kernel/nanokernel/nano_context.o
  CC      kernel/nanokernel/nano_init.o
  CC      kernel/nanokernel/nano_sema.o
  CC      kernel/nanokernel/version.o
  CC      kernel/nanokernel/device.o
  CC      kernel/nanokernel/nano_timer.o
  CC      kernel/nanokernel/ring_buffer.o
  CC      kernel/nanokernel/errno.o
  LD      kernel/nanokernel/built-in.o
  LD      kernel/built-in.o
  CC      misc/printk.o
  LD      misc/debug/built-in.o
  CC      misc/generated/configs.o
  LD      misc/generated/built-in.o
  LD      misc/built-in.o
  LD      net/built-in.o
  CC      boards/arduino_101/pinmux.o
  CC      boards/arduino_101/board.o
  LD      boards/arduino_101/built-in.o
  LD      boards/built-in.o
  CC      arch/x86/core/iamcu_abi/swap.o
  CC      arch/x86/core/iamcu_abi/intstub.o
  CC      arch/x86/core/iamcu_abi/thread.o
  AS      arch/x86/core/iamcu_abi/iamcu.o
  LD      arch/x86/core/iamcu_abi/built-in.o
  CC      arch/x86/core/fatal.o
  CC      arch/x86/core/cpuhalt.o
  CC      arch/x86/core/msr.o
  CC      arch/x86/core/dynamic.o
  CC      arch/x86/core/intconnect.o
  CC      arch/x86/core/excconnect.o
  CC      arch/x86/core/sys_fatal_error_handler.o
  AS      arch/x86/core/crt0.o
  CC      arch/x86/core/atomic.o
  AS      arch/x86/core/cache_s.o
  CC      arch/x86/core/cache.o
  AS      arch/x86/core/excstub.o
  LD      arch/x86/core/built-in.o
  CC      arch/x86/soc/quark_se/soc.o
  CC      arch/x86/soc/quark_se/soc_config.o
  CC      arch/x86/soc/quark_se/eoi.o
  LD      arch/x86/soc/quark_se/built-in.o
  LD      arch/x86/built-in.o
  LD      arch/built-in.o
  CC      ext/hal/qmsi/drivers/clk.o
  CC      ext/hal/qmsi/drivers/qm_uart.o
  LD      ext/hal/qmsi/built-in.o
  LD      ext/hal/built-in.o
  LD      ext/lib/crypto/built-in.o
  LD      ext/lib/built-in.o
  LD      ext/built-in.o
  CC      drivers/console/console_handler_shell.o
  CC      drivers/console/uart_console.o
  CC      drivers/console/ipm_console_receiver.o
  LD      drivers/console/built-in.o
  CC      drivers/interrupt_controller/system_apic.o
  CC      drivers/interrupt_controller/loapic_intr.o
  CC      drivers/interrupt_controller/ioapic_intr.o
  LD      drivers/interrupt_controller/built-in.o
  CC      drivers/ipm/ipm_quark_se.o
  LD      drivers/ipm/built-in.o
  LD      drivers/pinmux/built-in.o
  LD      drivers/random/built-in.o
  CC      drivers/serial/uart_qmsi.o
  LD      drivers/serial/built-in.o
  CC      drivers/timer/loapic_timer.o
  CC      drivers/timer/sys_clock_init.o
  LD      drivers/timer/built-in.o
  LD      drivers/built-in.o
  CC      samples/shell/src/main.o
  LD      samples/shell/src/built-in.o
  LINK    zephyr.lnk
  SIDT    staticIdt.o
  LINK    zephyr.elf
  BIN     zephyr.bin
make[2]: Leaving directory `/home/abraham/zephyr-project/samples/shell/outdir'
make[1]: Leaving directory `/home/abraham/zephyr-project'
abraham@aarcemor-desk:~/zephyr-project/samples/shell$ 
```