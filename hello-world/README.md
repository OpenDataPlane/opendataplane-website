---
title: ODP Hello World
description: |-
    The odp hello world git repository aims to make it as simple as possible to build and run ODP applications.
layout: container-breadcrumb
permalink: /hello-world/
specific_css: /assets/css/syntax.css
---
# ODP Hello World

The odp hello world git repository aims to make it as simple as possible to build and run ODP applications. After cloning the repo the script setup_odp_example.sh will install the nessisary ODP libaries and you can then complile the hello world examples.

## Steps to reproduce:

WARNING: this will install packages into your system and this only needs to be done once, after that the files can be simply built with make

```bash
git clone [https://git.linaro.org/lng/odp-example.git](https://git.linaro.org/lng/odp-example.git)
cd odp-example
./setup_odp_example.sh
```

You should get an output similar to this

```bash
desktop:~/git/odp-example# ./setup_odp_example.sh

Default distribution determined to be jessie

converted 'http://deb.opendataplane.org/odp.key' (ANSI_X3.4-1968) -> 'http://deb.opendataplane.org/odp.key' (UTF-8)
--2016-09-08 17:29:03-- http://deb.opendataplane.org/odp.key
Resolving deb.opendataplane.org (deb.opendataplane.org)... 54.224.40.137
Connecting to deb.opendataplane.org (deb.opendataplane.org)|54.224.40.137|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 939 [application/pgp-keys]
Saving to: 'STDOUT'

- 100%[=============================================>] 939 --.-KB/s in 0s

2016-09-08 17:29:03 (268 MB/s) - written to stdout [939/939]

OK
deb http://deb.opendataplane.org jessie main
Hit http://deb.opendataplane.org jessie InRelease
Get:1 http://deb.opendataplane.org jessie/main amd64 Packages [20.0 kB]
Hit http://security.debian.org jessie/updates InRelease
Get:2 http://security.debian.org jessie/updates/main amd64 Packages [387 kB]
Ign http://httpredir.debian.org jessie InRelease
Hit http://httpredir.debian.org jessie-updates InRelease
Hit http://httpredir.debian.org jessie Release.gpg
Get:3 http://httpredir.debian.org jessie-updates/main amd64 Packages [17.6 kB]
Hit http://httpredir.debian.org jessie Release
Get:4 http://httpredir.debian.org jessie/main amd64 Packages [9032 kB]
Fetched 9457 kB in 1s (5509 kB/s)
Reading package lists... Done
Reading package lists... Done
Building dependency tree
Reading state information... Done
gcc is already the newest version.
git is already the newest version.
libc6-dev is already the newest version.
make is already the newest version.
pkg-config is already the newest version.
libodp-linux-dev is already the newest version.
libodphelper-linux-dev is already the newest version.
0 upgraded, 0 newly installed, 0 to remove and 9 not upgraded.

Installation of ODP packages done.

Make targets:
all build examples
clean remove derived files

If you need to build against a local odp installation set
PKG_CONFIG_PATH=<path-to-local-odp-installed-dir>/lib/pkgconfig

If you want to use a different installed implementation
set ODPLIB_NAME for the other implementations.
default: odp-linux

make all
make all ODPLIB_NAME=odp-dpdk
```


The examples can now be built. The chosen examples walk though from a very simple application called hello to a generator and loopback pair that requires some configuration to run.

### Environment variables

setup_odp_example takes two environment variables that may have defaults you will need to change

*   ODPLIB_NAME which selects the implementation to be installed, this defaults to [odp-linux](https://git.linaro.org/lng/odp.git), which should run on any linux version. The second packaged variant works with PCI NIC devices and is called [odp-dpdk](https://git.linaro.org/lng/odp-dpdk.git) and is implemented using the DPDK SDK – please see the documentation for the differences. To change the default use

    ```bash
    ODPLIB_NAME=odp-dpdk ./setup_odp_example.sh
    ```

*   OS_RELASE which sets the distribution in uses, this defaults to the autodetected distribution. To change the default use

    ```bash
    OS_RELEASE=xenial ./setup_odp_example.sh
    ```

# Building

To build the examples use make

```bash
desktop:/tmp/odp-example# make all
gcc -I/usr/include/odp-linux -I/usr/include/odp -I. -lodp-linux -lodphelper-linux generator.c -o generator
gcc -I/usr/include/odp-linux -I/usr/include/odp -I. -lodp-linux -lodphelper-linux hello.c -o hello
gcc -I/usr/include/odp-linux -I/usr/include/odp -I. -lodp-linux -lodphelper-linux l2fwd.c -o l2fwd
gcc -I/usr/include/odp-linux -I/usr/include/odp -I. -lodp-linux -lodphelper-linux simple_timer.c -o simple_timer
```

Further help is provided by make itself, and it is possible to use pre installed ODP implimentations

```bash
desktop:/tmp/odp-example# make
Make targets:
all build examples
clean remove derived files

If you need to build against a local odp installation set
PKG_CONFIG_PATH=<path-to-local-odp-installed-dir>/lib/pkgconfig

If you want to use a different installed implementation
set ODPLIB_NAME for the other implementations.
default: odp-linux

make all
make all ODPLIB_NAME=odp-dpdk
```

## Dependencies

The setup_odp_example script lists the dependencies it needs to run, generally wget is all that might be required and occasionally lsb-core. These can be installed with the following and the script will take care of everything else.

```bash
sudo apt-get install wget
sudo apt-get install lsb-core
```

## Examples

The README.txt describes the examples that will be built, in addition help can be used to get further details on the possibilities to configure the examples

### Hello

This is a minimal application which demonstrates the startup and shutdown  
steps of an ODP application. It can be also used to debug API related  
build problems, etc. It does not use helpers to minimize dependency to  
anything else than the ODP API header file.

You should get an output similar to this

```bash
desktop:~/odp-example# ./hello
PKTIO: initialized loop interface.
PKTIO: initialized socket mmap, use export ODP_PKTIO_DISABLE_SOCKET_MMAP=1 to disable.
PKTIO: initialized socket mmsg,use export ODP_PKTIO_DISABLE_SOCKET_MMSG=1 to disable.
Hello world from CPU 0!
```

Using the help shows that a different core may be selected.

```bash
desktop:~/git/odp-example# ./hello --help
Usage:
 -c CPU number
 -n Number of iterations
```

### Simple_timer

This application extends on odp_hello by scheduling a timer action for 1 second.

You should get an output similar to this

```bash
desktop:~/git/odp-example# ./simple_timer
 PKTIO: initialized loop interface.
 PKTIO: initialized socket mmap, use export ODP_PKTIO_DISABLE_SOCKET_MMAP=1 to disable.
 PKTIO: initialized socket mmsg,use export ODP_PKTIO_DISABLE_SOCKET_MMSG=1 to disable.
odp_timer.c:681:timer_notify():
 1 ticks overrun on timer pool "timer_pool", timer resolution too high
timer tick 0, time ns 1012679885
timer tick 1, time ns 2031700370
timer tick 2, time ns 3043004845
timer tick 3, time ns 4057569569
timer tick 4, time ns 5067224538
```

Notice that in this case the very low performance machine resulted in warnings that the HW was not capable of the resolution requested

### generator / l2fwd pair

As applications get more complex the helper library is required, this provides  
support for launching odp_threads and posix threads or processes.

These applications can be used as a pair between physical machines, multiple odp  
process or vms. The generator can be configured to send packets and count their  
return, the l2fwd will loop back all the packets it is sent. This combination  
can be used to try out different scheduling options in the l2fwd application.

You should get an output similar to this when setting up the loopback machine with l2fwd

```bash
$ip addr
...
3: wlan0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP group default qlen 1000
link/ether 80:1f:02:7e:6d:31 brd ff:ff:ff:ff:ff:ff
inet192.168.1.220/24 brd 192.168.1.255 scope global wlan0
valid_lft forever preferred_lft forever
inet6 fe80::2661:d0f8:e8ee:4cd6/64 scope link
valid_lft forever preferred_lft forever

$./l2fwd –interface eth0
...
11 pps, 11 max pps, 0 rx drops, 0 tx drops
12 pps, 12 max pps, 0 rx drops, 0 tx drops
11 pps, 12 max pps, 0 rx drops, 0 tx drops
12 pps, 12 max pps, 0 rx drops, 0 tx drops
```

When setting up the generator

```bash
$ip addr
...
2: enp3s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP group default qlen 1000
link/ether 34:17:eb:e0:9d:8f brd ff:ff:ff:ff:ff:ff
inet 192.168.1.217/24 brd 192.168.1.255 scope global dynamic enp3s0
valid_lft 56533sec preferred_lft 56533sec
inet6 fe80::ce50:75e4:b420:d50/64 scope link
valid_lft forever preferred_lft forever

$odp_generator -I enp3s0 --srcmac 34:17:eb:e0:9d:8f --dstmac 80:1f:02:7e:6d:31 --srcip 192.168.1.217 --dstip 192.168.1.220 -m p -i 100
...
[01] ICMP Echo Reply seq 36 time 5.0
[02] send pkt no:38 seq 38
[01] ICMP Echo Reply seq 37 time 5.0
[02] send pkt no:39 seq 39
[01] ICMP Echo Reply seq 38 time 5.0
[02] send pkt no:40 seq 40
[01] ICMP Echo Reply seq 39 time 5.0
[02] send pkt no:41 seq 41
[01] ICMP Echo Reply seq 40 time 5.0
[02] send pkt no:42 seq 42

```
