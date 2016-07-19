# Boards

```sh
abraham@aarcemor-desk:~/zephyr-project$ ls
arch    drivers  Kbuild          kernel   MAINTAINERS   misc     scripts
boards  ext      Kconfig         lib      Makefile      net      tests
doc     include  Kconfig.zephyr  LICENSE  Makefile.inc  samples  zephyr-env.sh
```

```sh
abraham@aarcemor-desk:~/zephyr-project$ cd arch/
abraham@aarcemor-desk:~/zephyr-project/arch$ ls
arc  arm  Kconfig  Makefile  nios2  x86
```

```sh
abraham@aarcemor-desk:~/zephyr-project/arch$ ls arc/
core  defconfig  include  Kbuild  Kconfig  Makefile  soc
abraham@aarcemor-desk:~/zephyr-project/arch$ ls arc/soc
em11d  em9d  quark_se_ss
```

```sh
abraham@aarcemor-desk:~/zephyr-project/arch$ ls arm/
core  defconfig  include  Kbuild  Kconfig  Makefile  soc
abraham@aarcemor-desk:~/zephyr-project/arch$ ls arm/soc/
atmel_sam3  nordic_nrf5  nxp_kinetis  st_stm32  ti_lm3s6965
```

```sh
abraham@aarcemor-desk:~/zephyr-project/arch$ ls nios2/
core  defconfig  include  Kbuild  Kconfig  Makefile  soc
abraham@aarcemor-desk:~/zephyr-project/arch$ ls nios2/soc
nios2e-zephyr  nios2f-zephyr  nios2-qemu
```

```sh
abraham@aarcemor-desk:~/zephyr-project/arch$ ls x86/
core  debug  defconfig  include  Kbuild  Kconfig  Makefile  soc
abraham@aarcemor-desk:~/zephyr-project/arch$ ls x86/soc/
atom  ia32  quark_d2000  quark_se  quark_x1000
```