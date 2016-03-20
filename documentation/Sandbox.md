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
     

```