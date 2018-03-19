---
title: Applications
description: |-
    Here you will find Applications that are designed to work with the OpenDataPlane Project.
layout: default-plain
permalink: /applications/
---
## Applications

Applications designed to work with OpenDataPlane.

* * *

{% include image.html name="OpenFastPath.png" alt="Open Fast Path Logo" url="http://www.openfastpath.org/" %}

The exponential growth in data traffic puts ever-increasing demands on the packet processing elements in the network, resulting in a need for high performance IP packet handling. [OpenFastPath](http://www.openfastpath.org/) is an open source implementation of a high performance TCP/IP stack that provides features that network application developers need to cope with today’s fast-paced network. To enable this packet processing OFP uses OpenDataPlane.

* * *

{% include image.html name="vswitch.png" alt="VSwitch Logo" url="http://openvswitch.org/" %}

[Open vSwitch](http://openvswitch.org/) is a production quality, multilayer virtual switch licensed under the open source Apache 2.0 license. It is designed to enable massive network automation through programmatic extension, while still supporting standard management interfaces and protocols (e.g. NetFlow, sFlow, IPFIX, RSPAN, CLI, LACP, 802.1ag). In addition, it is designed to support distribution across multiple physical servers similar to VMware’s vNetwork distributed vswitch or Cisco’s Nexus 1000V. See full feature list [here](http://openvswitch.org/features).

Check out the OpenDataPlane-OVS git repo [here](https://git.linaro.org/lng/odp-ovs.git).

* * *

{% include image.html name="openSSL.jpg" alt="OpenSSL Logo" url="https://www.openssl.org/" %}

[OpenSSL](https://www.openssl.org/) is an open source project that provides a robust, commercial-grade, and full-featured toolkit for the Transport Layer Security (TLS) and Secure Sockets Layer (SSL) protocols. OpenSSL also supports pluggable accelerators, an ODP implimentation of this plugin is [available](https://git.linaro.org/lng/ossl-odp.git). This module uses a hybrid engine approach with a threshold that determines if it is beneficial to perform the operation on the CPU or via the hardware.
