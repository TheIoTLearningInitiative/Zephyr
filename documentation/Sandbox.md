# Sandbox

```sh
    xe1gyq@jessie:~# apt-get install git make gcc gcc-multilib g++ libc6-dev-i386 g++-multilib
    xe1gyq@jessie:~$ git clone https://gerrit.zephyrproject.org/r/zephyr zephyr-project
    Cloning into 'zephyr-project'...
    remote: Counting objects: 3, done
    remote: Finding sources: 100% (3/3)
    remote: Total 60526 (delta 0), reused 60526 (delta 0)
    Receiving objects: 100% (60526/60526), 19.74 MiB | 1.09 MiB/s, done.
    Resolving deltas: 100% (40213/40213), done.
    Checking connectivity... done.
    user@host:~$ cd zephyr-project 
    user@host:~$ ls
    xe1gyq@jessie:~/zephyr-project$ ls
    arch    doc      include  Kconfig         kernel  LICENSE   Makefile.inc  net      scripts  zephyr-env.sh
    boards  drivers  Kbuild   Kconfig.zephyr  lib     Makefile  misc          samples  tests
    xe1gyq@jessie:~/zephyr-project$ source zephyr-env.sh
    xe1gyq@jessie:~/zephyr-project$ wget https://nexus.zephyrproject.org/content/repositories/releases/org/zephyrproject/zephyr-sdk/0.7.5-i686/zephyr-sdk-0.7.5-i686-setup.run
    --2016-03-20 00:14:08--  https://nexus.zephyrproject.org/content/repositories/releases/org/zephyrproject/zephyr-sdk/0.7.5-i686/zephyr-sdk-0.7.5-i686-setup.run
    Resolving nexus.zephyrproject.org (nexus.zephyrproject.org)... 199.19.213.246
    Connecting to nexus.zephyrproject.org (nexus.zephyrproject.org)|199.19.213.246|:443... connected.
    HTTP request sent, awaiting response... 200 OK
    Length: 308466774 (294M) [application/octet-stream]
    Saving to: ‘zephyr-sdk-0.7.5-i686-setup.run’
    
    zephyr-sdk-0.7.5-i686-setup.ru 100%[====================================================>] 294.18M  1.05MB/s   in 6m 37s 
    
    2016-03-20 00:20:45 (759 KB/s) - ‘zephyr-sdk-0.7.5-i686-setup.run’ saved [308466774/308466774]
    xe1gyq@jessie:~/zephyr-project$ chmod +x zephyr-sdk-0.7.5-i686-setup.run
    xe1gyq@jessie:~/zephyr-project$ ./zephyr-sdk-0.7.5-i686-setup.run
    xe1gyq@jessie:~/zephyr-project$ ./zephyr-sdk-0.7.5-i686-setup.run 
    Verifying archive integrity... All good.
    Uncompressing SDK for Zephyr  100%  
    Enter target directory for SDK (default: /opt/zephyr-sdk/): /home/xe1gyq/zephyr/zephyr-sdk/
    Installing SDK to /home/xe1gyq/zephyr/zephyr-sdk
    Creating directory /home/xe1gyq/zephyr/zephyr-sdk
    Success
     [*] Installing x86 tools... 
     [*] Installing arm tools... 
     [*] Installing arc tools... 
     [*] Installing iamcu tools... 
     [*] Installing mips tools... 
     [*] Installing additional host tools
     Success installing SDK. SDK is ready to be used.
     xe1gyq@jessie:~/zephyr-project$ export ZEPHYR_GCC_VARIANT=zephyr
     xe1gyq@jessie:~/zephyr-project$ export ZEPHYR_SDK_INSTALL_DIR=/home/xe1gyq/zephyr/zephyr-sdk/
     xe1gyq@jessie:~/zephyr-project$ cat <<EOF > ~/.zephyrrc
     > export ZEPHYR_GCC_VARIANT=zephyr
     > export ZEPHYR_SDK_INSTALL_DIR=/home/xe1gyq/zephyr/zephyr-sdk/
     > EOF
     xe1gyq@jessie:~/zephyr-project$ cd
```

```sh
xe1gyq@jessie:~/zephyr-project$ cd $ZEPHYR_BASE/samples/hello_world/microkernel
xe1gyq@jessie:~/zephyr-project/samples/hello_world/microkernel$ make
Using /home/xe1gyq/zephyr-project/boards/qemu_x86/qemu_x86_defconfig as base
Merging /home/xe1gyq/zephyr-project/kernel/configs/micro.config
Merging prj.conf
#
# configuration written to .config
#
make[1]: Entering directory '/home/xe1gyq/zephyr-project'
make[2]: Entering directory '/home/xe1gyq/zephyr-project/samples/hello_world/microkernel/outdir'
  GEN     ./Makefile
scripts/kconfig/conf --silentoldconfig Kconfig
  Using /home/xe1gyq/zephyr-project as source for kernel
  GEN     ./Makefile
  CHK     include/generated/version.h
  UPD     include/generated/version.h
  HOSTCC  scripts/gen_idt/gen_idt.o
  HOSTLD  scripts/gen_idt/gen_idt
  CHK     misc/generated/configs.c
  UPD     misc/generated/configs.c
  CHK     include/generated/offsets.h
  UPD     include/generated/offsets.h
  CHK     misc/generated/sysgen/prj.mdef
  UPD     misc/generated/sysgen/prj.mdef
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
  CC      kernel/microkernel/k_task.o
  CC      kernel/microkernel/k_idle.o
  CC      kernel/microkernel/k_init.o
  CC      kernel/microkernel/k_command_packet.o
  CC      kernel/microkernel/k_move_data.o
  CC      kernel/microkernel/k_ticker.o
  CC      kernel/microkernel/k_memory_map.o
  CC      kernel/microkernel/k_memory_pool.o
  CC      kernel/microkernel/k_irq.o
  CC      kernel/microkernel/k_nop.o
  CC      kernel/microkernel/k_offload.o
  CC      kernel/microkernel/k_event.o
  CC      kernel/microkernel/k_mailbox.o
  CC      kernel/microkernel/k_mutex.o
  CC      kernel/microkernel/k_fifo.o
  CC      kernel/microkernel/k_semaphore.o
  CC      kernel/microkernel/k_timer.o
  CC      kernel/microkernel/k_pipe_buffer.o
  CC      kernel/microkernel/k_pipe.o
  CC      kernel/microkernel/k_pipe_get.o
  CC      kernel/microkernel/k_pipe_put.o
  CC      kernel/microkernel/k_pipe_util.o
  CC      kernel/microkernel/k_pipe_xfer.o
  CC      kernel/microkernel/k_server.o
  LD      kernel/microkernel/built-in.o
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
  LD      kernel/nanokernel/built-in.o
  LD      kernel/built-in.o
  CC      misc/printk.o
  CC      misc/debug/mem_safe_check_boundaries.o
  LD      misc/debug/built-in.o
  CC      misc/generated/configs.o
  CC      misc/generated/sysgen/kernel_main.o
  LD      misc/generated/sysgen/built-in.o
  LD      misc/generated/built-in.o
  LD      misc/built-in.o
  LD      net/built-in.o
  CC      boards/qemu_x86/board.o
  LD      boards/qemu_x86/built-in.o
  LD      boards/built-in.o
  AS      arch/x86/core/i386_sysV_abi/intstub.o
  AS      arch/x86/core/i386_sysV_abi/swap.o
  CC      arch/x86/core/i386_sysV_abi/thread.o
  LD      arch/x86/core/i386_sysV_abi/built-in.o
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
  CC      arch/x86/core/strtask.o
  AS      arch/x86/core/errno.o
  LD      arch/x86/core/built-in.o
  CC      arch/x86/soc/ia32/soc.o
  LD      arch/x86/soc/ia32/built-in.o
  LD      arch/x86/built-in.o
  LD      arch/built-in.o
  LD      drivers/aio/built-in.o
  CC      drivers/console/uart_console.o
  LD      drivers/console/built-in.o
  CC      drivers/interrupt_controller/i8259.o
  CC      drivers/interrupt_controller/system_apic.o
  CC      drivers/interrupt_controller/loapic_intr.o
  CC      drivers/interrupt_controller/ioapic_intr.o
  LD      drivers/interrupt_controller/built-in.o
  LD      drivers/random/built-in.o
  CC      drivers/serial/uart_ns16550.o
  LD      drivers/serial/built-in.o
  CC      drivers/timer/hpet.o
  CC      drivers/timer/sys_clock_init.o
  LD      drivers/timer/built-in.o
  LD      drivers/built-in.o
  CC      samples/hello_world/microkernel/src/main.o
  LD      samples/hello_world/microkernel/src/built-in.o
  LINK    zephyr.lnk
  SIDT    staticIdt.o
  LINK    zephyr.elf
  BIN     zephyr.bin
make[2]: Leaving directory '/home/xe1gyq/zephyr-project/samples/hello_world/microkernel/outdir'
make[1]: Leaving directory '/home/xe1gyq/zephyr-project'
```