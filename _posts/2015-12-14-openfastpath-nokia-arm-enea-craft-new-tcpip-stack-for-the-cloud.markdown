---
author: marshall.guillory
comments: false
date: 2015-12-14 13:33:21+00:00
layout: post
link: https://www.opendataplane.org/blog/openfastpath-nokia-arm-enea-craft-new-tcpip-stack-for-the-cloud/
slug: openfastpath-nokia-arm-enea-craft-new-tcpip-stack-for-the-cloud
title: 'OpenFastPath &#58; Nokia, ARM, Enea craft new TCP/IP stack for the cloud'
wordpress_id: 1898
categories:
- News Hub
tags:
- ARM
- ENEA
- Linaro
- Linaro Networking Group (LNG)
- Linux
- Linux on Arm
- LNG
- networking
- NFV
- Nokia
- ODP
- OpenDataPlane
- Opensource
- SDN
- Software Defined Networking
---
# Nokia, ARM, Enea craft new TCP/IP stack for the cloud

Originally published at [theregister](http://www.theregister.co.uk/2015/12/08/nokia_arm_enea_craft_tcpip_stack_for_the_cloud/) by Richard Chirgwin on December 8, 2015.

<blockquote markdown="1">
A group of major vendors has put forward an open source TCP/IP stack they say is designed to reinvigorate the ancient and rather crusty protocol.

Nokia, ARM, and Enea are offering up both code and tutorials [here](http://www.openfastpath.org/) for their OpenFastPath user-space TCP/IP implementation.

As _The Register_ has previously noted, user-space networking is designed to get TCP/IP out of the kernel space, for two reasons: kernels have absorbed a lot of code over the years; and using the kernel for packet processing involves extra operations to get packets into memory, pass them to the kernel, and push them back out to the interface.
</blockquote>


...<!-- more -->

<blockquote markdown="1">
They say the stack is optimised for OpenDataPlane (ODP) programming interfaces. This will let OpenFastPath take advantage of acceleration in systems-on-a-chip that support ODP, and make the protocol programmable via the ODP environment.

As well as the three founding companies, the OpenFastPath Foundation claims support from AMD, Cavium, Freescale, HP and Linaro.

The group is hoping future contributors will work on interfaces for the open source Data Plane Development Kit (DPDK, [here](http://dpdk.org/)). Currently, data plane integration happens via the ODP-DPDK layer. ®
</blockquote>
