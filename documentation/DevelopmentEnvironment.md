# Development Environment

# Development Environment Setup on Linux

## Libraries Update

```sh
abraham@aarcemor-desk:~$ sudo apt-get update
Get:1 http://security.ubuntu.com trusty-security InRelease [65.9 kB]
Get:2 http://packages.ros.org trusty InRelease [4 031 B]                       
Ign http://extras.ubuntu.com trusty InRelease                                  
Hit http://ppa.launchpad.net trusty InRelease                                  
Ign http://mx.archive.ubuntu.com trusty InRelease                              
Get:3 http://packages.ros.org trusty/main amd64 Packages [702 kB]              
Get:4 http://extras.ubuntu.com trusty Release.gpg [72 B]                       
Get:5 http://mx.archive.ubuntu.com trusty-updates InRelease [65.9 kB]          
Hit http://ppa.launchpad.net trusty/main amd64 Packages                        
Get:6 http://security.ubuntu.com trusty-security/main Sources [116 kB]         
Hit http://extras.ubuntu.com trusty Release                                    
Hit http://ppa.launchpad.net trusty/main i386 Packages                         
Get:7 http://security.ubuntu.com trusty-security/restricted Sources [4 035 B]  
Hit http://extras.ubuntu.com trusty/main Sources                               
Get:8 http://security.ubuntu.com trusty-security/universe Sources [37.3 kB]    
Hit http://ppa.launchpad.net trusty/main Translation-en                        
Get:9 http://security.ubuntu.com trusty-security/multiverse Sources [2 757 B]  
Hit http://extras.ubuntu.com trusty/main amd64 Packages                        
Hit http://mx.archive.ubuntu.com trusty-backports InRelease                    
Get:10 http://security.ubuntu.com trusty-security/main amd64 Packages [493 kB] 
Get:11 http://packages.ros.org trusty/main i386 Packages [702 kB]              
Hit http://extras.ubuntu.com trusty/main i386 Packages                         
Hit http://mx.archive.ubuntu.com trusty Release.gpg                            
Get:12 http://mx.archive.ubuntu.com trusty-updates/main Sources [277 kB]       
Get:13 http://security.ubuntu.com trusty-security/restricted amd64 Packages [13.0 kB]
Get:14 http://security.ubuntu.com trusty-security/universe amd64 Packages [130 kB]
Get:15 http://security.ubuntu.com trusty-security/multiverse amd64 Packages [4 989 B]
Get:16 http://security.ubuntu.com trusty-security/main i386 Packages [464 kB]  
Ign http://repos.tel.red stable InRelease                                      
Get:17 http://mx.archive.ubuntu.com trusty-updates/restricted Sources [5 352 B]
Get:18 http://security.ubuntu.com trusty-security/restricted i386 Packages [12.7 kB]
Get:19 http://security.ubuntu.com trusty-security/universe i386 Packages [130 kB]
Get:20 http://mx.archive.ubuntu.com trusty-updates/universe Sources [157 kB]   
Get:21 http://security.ubuntu.com trusty-security/multiverse i386 Packages [5 170 B]
Hit http://repos.tel.red stable Release.gpg                                    
Get:22 http://security.ubuntu.com trusty-security/main Translation-en [271 kB] 
Get:23 http://mx.archive.ubuntu.com trusty-updates/multiverse Sources [5 936 B]
Ign http://packages.ros.org trusty/main Translation-en_US                      
Get:24 http://security.ubuntu.com trusty-security/multiverse Translation-en [2 570 B]
Ign http://packages.ros.org trusty/main Translation-en                         
Get:25 http://mx.archive.ubuntu.com trusty-updates/main amd64 Packages [781 kB]
Get:26 http://security.ubuntu.com trusty-security/restricted Translation-en [3 206 B]
Get:27 http://security.ubuntu.com trusty-security/universe Translation-en [76.6 kB]
Hit http://repos.tel.red stable Release                                        
Ign http://extras.ubuntu.com trusty/main Translation-en_US                     
Ign http://extras.ubuntu.com trusty/main Translation-en                 
Get:28 http://mx.archive.ubuntu.com trusty-updates/restricted amd64 Packages [15.9 kB]
Get:29 http://mx.archive.ubuntu.com trusty-updates/universe amd64 Packages [362 kB]
Hit http://repos.tel.red stable/non-free amd64 Packages   
Hit http://repos.tel.red stable/non-free i386 Packages                      
Get:30 http://mx.archive.ubuntu.com trusty-updates/multiverse amd64 Packages [13.2 kB]
Get:31 http://mx.archive.ubuntu.com trusty-updates/main i386 Packages [748 kB]
Get:32 http://mx.archive.ubuntu.com trusty-updates/restricted i386 Packages [15.6 kB]
Get:33 http://mx.archive.ubuntu.com trusty-updates/universe i386 Packages [363 kB]
Get:34 http://mx.archive.ubuntu.com trusty-updates/multiverse i386 Packages [13.6 kB]
Get:35 http://mx.archive.ubuntu.com trusty-updates/main Translation-en [391 kB]
Get:36 http://mx.archive.ubuntu.com trusty-updates/multiverse Translation-en [7 227 B]
Get:37 http://mx.archive.ubuntu.com trusty-updates/restricted Translation-en [3 699 B]
Get:38 http://mx.archive.ubuntu.com trusty-updates/universe Translation-en [189 kB]
Ign http://repos.tel.red stable/non-free Translation-en_US                     
Ign http://repos.tel.red stable/non-free Translation-en                        
Hit http://mx.archive.ubuntu.com trusty-backports/main Sources                 
Hit http://mx.archive.ubuntu.com trusty-backports/restricted Sources           
Hit http://mx.archive.ubuntu.com trusty-backports/universe Sources             
Hit http://mx.archive.ubuntu.com trusty-backports/multiverse Sources           
Hit http://mx.archive.ubuntu.com trusty-backports/main amd64 Packages          
Hit http://mx.archive.ubuntu.com trusty-backports/restricted amd64 Packages    
Hit http://mx.archive.ubuntu.com trusty-backports/universe amd64 Packages      
Hit http://mx.archive.ubuntu.com trusty-backports/multiverse amd64 Packages    
Hit http://mx.archive.ubuntu.com trusty-backports/main i386 Packages           
Hit http://mx.archive.ubuntu.com trusty-backports/restricted i386 Packages     
Hit http://mx.archive.ubuntu.com trusty-backports/universe i386 Packages       
Hit http://mx.archive.ubuntu.com trusty-backports/multiverse i386 Packages     
Hit http://mx.archive.ubuntu.com trusty-backports/main Translation-en          
Hit http://mx.archive.ubuntu.com trusty-backports/multiverse Translation-en    
Hit http://mx.archive.ubuntu.com trusty-backports/restricted Translation-en    
Hit http://mx.archive.ubuntu.com trusty-backports/universe Translation-en      
Hit http://mx.archive.ubuntu.com trusty Release                                
Hit http://mx.archive.ubuntu.com trusty/main Sources                           
Hit http://mx.archive.ubuntu.com trusty/restricted Sources                     
Hit http://mx.archive.ubuntu.com trusty/universe Sources                       
Hit http://mx.archive.ubuntu.com trusty/multiverse Sources                     
Hit http://mx.archive.ubuntu.com trusty/main amd64 Packages                    
Hit http://mx.archive.ubuntu.com trusty/restricted amd64 Packages              
Hit http://mx.archive.ubuntu.com trusty/universe amd64 Packages                
Hit http://mx.archive.ubuntu.com trusty/multiverse amd64 Packages              
Hit http://mx.archive.ubuntu.com trusty/main i386 Packages                     
Hit http://mx.archive.ubuntu.com trusty/restricted i386 Packages               
Hit http://mx.archive.ubuntu.com trusty/universe i386 Packages                 
Hit http://mx.archive.ubuntu.com trusty/multiverse i386 Packages               
Hit http://mx.archive.ubuntu.com trusty/main Translation-en                    
Hit http://mx.archive.ubuntu.com trusty/multiverse Translation-en              
Hit http://mx.archive.ubuntu.com trusty/restricted Translation-en              
Hit http://mx.archive.ubuntu.com trusty/universe Translation-en                
Ign http://mx.archive.ubuntu.com trusty/main Translation-en_US                 
Ign http://mx.archive.ubuntu.com trusty/multiverse Translation-en_US           
Ign http://mx.archive.ubuntu.com trusty/restricted Translation-en_US           
Ign http://mx.archive.ubuntu.com trusty/universe Translation-en_US             
Fetched 6 655 kB in 25s (264 kB/s)                                            
Reading package lists... Done
abraham@aarcemor-desk:~$ 
```

```sh
xe1gyq@jessie:~# apt-get install git make gcc gcc-multilib g++ libc6-dev-i386 g++-multilib python3-ply
```

## Development Environment SDK

```sh
abraham@aarcemor-desk:~$ wget https://nexus.zephyrproject.org/content/repositories/releases/org/zephyrproject/zephyr-sdk/0.8-i686/zephyr-sdk-0.8-i686-setup.run--2016-06-25 11:48:38--  https://nexus.zephyrproject.org/content/repositories/releases/org/zephyrproject/zephyr-sdk/0.8-i686/zephyr-sdk-0.8-i686-setup.run
Resolving nexus.zephyrproject.org (nexus.zephyrproject.org)... 199.19.213.246
Connecting to nexus.zephyrproject.org (nexus.zephyrproject.org)|199.19.213.246|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 378809314 (361M) [application/octet-stream]
Saving to: ‘zephyr-sdk-0.8-i686-setup.run’

100%[======================================>] 378 809 314 1.29MB/s   in 5m 42s 

2016-06-25 11:54:21 (1.06 MB/s) - ‘zephyr-sdk-0.8-i686-setup.run’ saved [378809314/378809314]

abraham@aarcemor-desk:~$ chmod +x zephyr-sdk-0.8-i686-setup.run 
abraham@aarcemor-desk:~$ sudo ./zephyr-sdk-<version>-i686-setup.run
[sudo] password for abraham: 
Verifying archive integrity... All good.
Uncompressing SDK for Zephyr  100%  
Enter target directory for SDK (default: /opt/zephyr-sdk/): 
Installing SDK to /opt/zephyr-sdk
Creating directory /opt/zephyr-sdk
Success
 [*] Installing x86 tools... 
 [*] Installing arm tools... 
 [*] Installing arc tools... 
 [*] Installing iamcu tools... 
 [*] Installing mips tools... 
 [*] Installing nios2 tools... 
 [*] Installing additional host tools... 
Success installing SDK. SDK is ready to be used.
abraham@aarcemor-desk:~$ 
```

```sh
abraham@aarcemor-desk:~$ export ZEPHYR_GCC_VARIANT=zephyr
abraham@aarcemor-desk:~$ export ZEPHYR_SDK_INSTALL_DIR=/opt/zephyr-sdk
abraham@aarcemor-desk:~$ 
```

```sh
abraham@aarcemor-desk:~$ cat << EOF > ~/.zephyrrc
export ZEPHYR_GCC_VARIANT=zephyr
export ZEPHYR_SDK_INSTALL_DIR=/opt/zephyr-sdk
EOF
```

## Download the Code
  
```sh
abraham@aarcemor-desk:~$ git config --global --unset http.proxy
abraham@aarcemor-desk:~$ git config --global --unset https.proxy
```

```sh
xe1gyq@jessie:~$ git clone https://gerrit.zephyrproject.org/r/zephyr zephyr-project
Cloning into 'zephyr-project'...
remote: Counting objects: 3, done
remote: Finding sources: 100% (3/3)
remote: Total 60526 (delta 0), reused 60526 (delta 0)
Receiving objects: 100% (60526/60526), 19.74 MiB | 1.09 MiB/s, done.
Resolving deltas: 100% (40213/40213), done.
Checking connectivity... done.
```

## Setting the Project’s Environment Variables

```sh
abraham@aarcemor-desk:~$ source ~/.zephyrrc
abraham@aarcemor-desk:~$ cd zephyr-project/
abraham@aarcemor-desk:~/zephyr-project$ ls
arch    drivers  Kbuild          kernel   MAINTAINERS   misc     scripts
boards  ext      Kconfig         lib      Makefile      net      tests
doc     include  Kconfig.zephyr  LICENSE  Makefile.inc  samples  zephyr-env.sh
abraham@aarcemor-desk:~/zephyr-project$ source zephyr-env.sh 
abraham@aarcemor-desk:~/zephyr-project$ 
```

## Building and Running an Application

```sh
abraham@aarcemor-desk:~/zephyr-project$ cd $ZEPHYR_BASE/samples/hello_world/microkernel
abraham@aarcemor-desk:~/zephyr-project/samples/hello_world/microkernel$ make BOARD=galileo
Using /home/abraham/zephyr-project/boards/galileo/galileo_defconfig as base
Merging /home/abraham/zephyr-project/kernel/configs/micro.config
Merging prj.conf
#
# configuration written to .config
#
make[1]: Entering directory `/home/abraham/zephyr-project'
make[2]: Entering directory `/home/abraham/zephyr-project/samples/hello_world/microkernel/outdir'
  GEN     ./Makefile
scripts/kconfig/conf --silentoldconfig Kconfig
make[2]: Leaving directory `/home/abraham/zephyr-project/samples/hello_world/microkernel/outdir'
make[2]: Entering directory `/home/abraham/zephyr-project/samples/hello_world/microkernel/outdir'
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
  CC      kernel/microkernel/k_nano.o
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
  CC      kernel/nanokernel/nano_sleep.o
  CC      kernel/nanokernel/nano_timer.o
  CC      kernel/nanokernel/errno.o
  LD      kernel/nanokernel/built-in.o
  LD      kernel/built-in.o
  CC      misc/printk.o
  LD      misc/debug/built-in.o
  CC      misc/generated/configs.o
  CC      misc/generated/sysgen/kernel_main.o
  LD      misc/generated/sysgen/built-in.o
  LD      misc/generated/built-in.o
  LD      misc/built-in.o
  LD      net/built-in.o
  CC      boards/galileo/board.o
  CC      boards/galileo/pinmux.o
  LD      boards/galileo/built-in.o
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
  LD      arch/x86/core/built-in.o
  CC      arch/x86/soc/quark_x1000/soc.o
  LD      arch/x86/soc/quark_x1000/built-in.o
  LD      arch/x86/built-in.o
  LD      arch/built-in.o
  LD      ext/hal/built-in.o
  LD      ext/lib/crypto/built-in.o
  LD      ext/lib/built-in.o
  LD      ext/built-in.o
  CC      drivers/adc/adc_ti_adc108s102.o
  LD      drivers/adc/built-in.o
  CC      drivers/console/uart_console.o
  LD      drivers/console/built-in.o
  CC      drivers/gpio/gpio_api_compat.o
  CC      drivers/gpio/gpio_dw.o
  CC      drivers/gpio/gpio_pcal9535a.o
  CC      drivers/gpio/gpio_sch.o
  LD      drivers/gpio/built-in.o
  CC      drivers/i2c/i2c_dw.o
  LD      drivers/i2c/built-in.o
  CC      drivers/interrupt_controller/system_apic.o
  CC      drivers/interrupt_controller/loapic_intr.o
  CC      drivers/interrupt_controller/ioapic_intr.o
  LD      drivers/interrupt_controller/built-in.o
  CC      drivers/pci/pci.o
  CC      drivers/pci/pci_config.o
  CC      drivers/pci/pci_interface.o
  CC      drivers/pci/pci_legacy_bridge.o
  LD      drivers/pci/built-in.o
  LD      drivers/pinmux/built-in.o
  CC      drivers/pwm/pwm_pca9685.o
  LD      drivers/pwm/built-in.o
  LD      drivers/random/built-in.o
  CC      drivers/serial/uart_ns16550.o
  LD      drivers/serial/built-in.o
  CC      drivers/shared_irq/shared_irq.o
  LD      drivers/shared_irq/built-in.o
  CC      drivers/spi/spi_intel.o
  LD      drivers/spi/built-in.o
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
make[2]: Leaving directory `/home/abraham/zephyr-project/samples/hello_world/microkernel/outdir'
make[1]: Leaving directory `/home/abraham/zephyr-project'
abraham@aarcemor-desk:~/zephyr-project/samples/hello_world/microkernel$ 
```
