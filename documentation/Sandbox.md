# Sandbox

# Bluetooth

```sh
abraham@aarcemor-desk:~$ sudo apt-get install bluez bluez-utils bluez-tools libbluetooth-dev python-dev
Reading package lists... Done
Building dependency tree       
Reading state information... Done
python-dev is already the newest version.
bluez-tools is already the newest version.
bluez is already the newest version.
libbluetooth-dev is already the newest version.
bluez-utils is already the newest version.
0 upgraded, 0 newly installed, 0 to remove and 393 not upgraded.
abraham@aarcemor-desk:~$ 
```

```sh
abraham@aarcemor-desk:~$ git clone https://github.com/conorpp/btproxy
Cloning into 'btproxy'...
remote: Counting objects: 310, done.
remote: Total 310 (delta 0), reused 0 (delta 0), pack-reused 310
Receiving objects: 100% (310/310), 120.06 KiB | 0 bytes/s, done.
Resolving deltas: 100% (186/186), done.
Checking connectivity... done.
```

```sh
abraham@aarcemor-desk:~$ cd btproxy/
abraham@aarcemor-desk:~/btproxy$ sudo python setup.py install
...
Adding PyBluez 0.22 to easy-install.pth file

Installed /usr/local/lib/python2.7/dist-packages/PyBluez-0.22-py2.7-linux-x86_64.egg
Finished processing dependencies for btproxy==0.1
abraham@aarcemor-desk:~/btproxy$ 
```

# 

```sh
abraham@aarcemor-desk:~/bluez$ sudo apt-get install libical-dev
```

```sh
abraham@aarcemor-desk:~$ git clone https://git.kernel.org/pub/scm/bluetooth/bluez.git
abraham@aarcemor-desk:~$ cd bluez
```

```sh
abraham@aarcemor-desk:~/bluez$ ./configure --prefix=/usr --mandir=/usr/share/man --sysconfdir=/etc --localstatedir=/var --enable-experimental --with-systemdsystemunitdir=/lib/systemd/system --with-systemduserunitdir=/usr/lib/systemd
```