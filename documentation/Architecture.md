Architecture
==

## Clone Repository In Intel Edison

```
    root@edison:~# git clone https://gerrit.zephyrproject.org/r/zephyr --branch v1.1
```

## Make Help

```
xe1gyq@jessie:~/zephyr-project/samples/hello_world/microkernel$ make help
Cleaning targets:
  clean		  - Remove most generated files but keep configuration and backup files
  mrproper	  - Remove all generated files + config + various backup files
  distclean	  - mrproper + remove editor backup and patch files
  pristine	  - Remove the output directory with all generated files

Configuration targets:

  run <make kconfig-help>

Other generic targets:
  all		  - Build all targets marked with [*]
* zephyr	  - Build a zephyr application
  qemu		  - Build a zephyr application and run it in qemu
  flash		  - Build and flash an application
  debug		  - Build and debug an application using GDB

Supported Boards:

  To build an image for one of the supported boards below, run:

  make BOARD=<BOARD NAME>
  in the application directory.

  To flash the image (if supported), run:

  make BOARD=<BOARD NAME> flash

  make BOARD=arduino_101              - Build for arduino_101
  make BOARD=arduino_101_sss          - Build for arduino_101_sss
  make BOARD=arduino_due              - Build for arduino_due
  make BOARD=basic_atom               - Build for basic_atom
  make BOARD=basic_cortex_m3          - Build for basic_cortex_m3
  make BOARD=basic_minuteia           - Build for basic_minuteia
  make BOARD=frdm_k64f                - Build for frdm_k64f
  make BOARD=galileo                  - Build for galileo
  make BOARD=minnowboard              - Build for minnowboard
  make BOARD=nucleo_f103rb            - Build for nucleo_f103rb
  make BOARD=qemu_cortex_m3           - Build for qemu_cortex_m3
  make BOARD=qemu_x86                 - Build for qemu_x86
  make BOARD=qemu_x86_iamcu           - Build for qemu_x86_iamcu
  make BOARD=quark_d2000_crb          - Build for quark_d2000_crb
  make BOARD=quark_se_devboard        - Build for quark_se_devboard
  make BOARD=quark_se_sss_devboard    - Build for quark_se_sss_devboard
  make BOARD=stm32_mini_a15           - Build for stm32_mini_a15


Build flags:

  make V=0|1 [targets] 0 => quiet build (default), 1 => verbose build
  make V=2   [targets] 2 => give reason for rebuild of target
  make O=dir [targets] Locate all output files in "dir", including .config
  make C=1   [targets] Check all c source with $CHECK (sparse by default)
  make C=2   [targets] Force check of all c source with $CHECK
  make RECORDMCOUNT_WARN=1 [targets] Warn about ignored mcount sections
  make W=n   [targets] Enable extra gcc checks, n=1,2,3 where
		1: warnings which may be relevant and do not occur too often
		2: warnings which occur quite often but may still be relevant
		3: more obscure warnings, can most likely be ignored
		Multiple levels can be combined with W=12 or W=123

Execute "make" or "make all" to build all targets marked with [*] 
```

## Make Menuconfig

```sh
    xe1gyq@jessie:~/zephyr-project$ make menuconfig
    ...
    Architecture (x86 architecture)
    x86 SoC Selection (Generic IA32 SoC)
    x86 Options
    Board Selection (QEMU x86)
    Board Options
    Kernel Type (Micro Kernel)
    General Kernel Options
    Nanokernel Options
    Microkernel Options
    Power Management
    Device Drivers
    Networking
    Cryptography
    Compile and Link Features
    Debugging Options
    Logging Options
    System Monitoring Options
    Boot Options
```

## Architecture, SoC, Board

Look at the following Configurations Options under [Configuration Options Reference Guide](https://www.zephyrproject.org/doc/reference/kconfig/index.html)
and identify which SoC i tight to which Board for the x86 Architecrure

- CONFIG_X86
- CONFIG_SOC
- CONFIG_X86_IAMCU
- CONFIG_SOC_QUARK_D2000
- CONFIG_SOC_QUARK_X1000
- CONFIG_SOC_ATOM
- CONFIG_SOC_QUARK_SE
- CONFIG_SOC_IA32
- CONFIG_CPU_ATOM
- CONFIG_CPU_MINUTEIA

Now confirm your answers are correct by looking at the Zephyr Kernel Configuration, x86 SoC & Board Selection

```sh
    xe1gyq@jessie:~/zephyr-project$ make menuconfig
    ...
    x86 SoC Selection (Generic IA32 SoC)
    x86 Options
    Board Selection (QEMU x86)
    Board Options
    ...
```sh
