---
author: marshall.guillory
comments: false
date: 2015-11-30 08:00:09+00:00
layout: post
link: https://www.opendataplane.org/blog/opendataplane-v1-5-0-release-published-to-the-repo/
slug: opendataplane-v1-5-0-release-published-to-the-repo
title: OpenDataPlane v1.5.0 Release published to the repo!
wordpress_id: 1852
categories:
- News Hub
tags:
- ARM
- Cavium
- Cisco
- ENEA
- HiSilicon
- Linaro Networking Group (LNG)
- Linux
- Linux on Arm
- LNG
- networking
- NFV
- ODP
- OpenDataPlane
- release
- SDN
- Software Defined Networking
---

[The OpenDataPlane team is pleased to announce the ODP v1.5.0](https://git.linaro.org/lng/odp.git/tag/?h=v1.5.0.0) release of the OpenDataPlane API's. Features delivered:


## Epic

  * [[ODP-8](https://projects.linaro.org/browse/ODP-8)] – Implement Ordered Queues to TM

## Story

  * [[ODP-64](https://projects.linaro.org/browse/ODP-64)] – RPM fedora packaging for Linux-generic ODP on Linaro Releases


  * [[ODP-65](https://projects.linaro.org/browse/ODP-65)] – Debian packaging for Linux-generic ODP on Linaro Releases


  * [[ODP-66](https://projects.linaro.org/browse/ODP-66)] – RPM RHEL packaging for Linux-generic ODP on Linaro Releases


  * [[ODP-69](https://projects.linaro.org/browse/ODP-69)] – Update libpcap for ODP 1.0


  * [[ODP-81](https://projects.linaro.org/browse/ODP-81)] – Classification complete tests


  * [[ODP-104](https://projects.linaro.org/browse/ODP-104)] – ODP needs tcpreplay like functionality


  * [[ODP-105](https://projects.linaro.org/browse/ODP-105)] – Rename buffers to event as appropriate


  * [[ODP-125](https://projects.linaro.org/browse/ODP-125)] – Update API-NEXT with header files for tuple-based traffic spreading


  * [[ODP-167](https://projects.linaro.org/browse/ODP-167)] – create test superlib


  * [[ODP-174](https://projects.linaro.org/browse/ODP-174)] – User guide outline


  * [[ODP-179](https://projects.linaro.org/browse/ODP-179)] – Unbind CPU cycles from Time API


  * [[ODP-189](https://projects.linaro.org/browse/ODP-189)] – move ODP-netmap to 1.3


  * [[ODP-215](https://projects.linaro.org/browse/ODP-215)] – don’t return control cpu in worker cpu mask


  * [[ODP-219](https://projects.linaro.org/browse/ODP-219)] – Use only correct resolution and timer period


  * [[ODP-220](https://projects.linaro.org/browse/ODP-220)] – Bump ODP-DPDK to 1.4 version of ODP API


  * [[ODP-233](https://projects.linaro.org/browse/ODP-233)] – switch args for diff function in CPU cycle API as it was done for time API


  * [[ODP-253](https://projects.linaro.org/browse/ODP-253)] – Fix linking for ODP-OVS packaging


  * [[ODP-284](https://projects.linaro.org/browse/ODP-284)] – Allow validation tests to be run without automake infrastructure


[OpenDataPlane v1.5.0.0](https://git.linaro.org/lng/odp.git/tag/?h=v1.5.0.0)
* API:

– api: buffer: add functions to alloc/free multiple buffers at once

– api: cpu: change order of arguments for diff function

– api: crypto: add AES128-CBC encrypt/decrypt methods

– api: crypto: add HMAC-SHA-256-128 support

– api: crypto: move enums from platform types to odp and rename to fit the API format

– api: packet: add functions to alloc/free multiple packets at once

– api: queue: add odp_queue_info() function to retrieve queue information

– api: time: change order of arguments for diff function

– api: time: unbind CPU cycles from time API
* ODP docs:

– userguide: add baseline overview to document

– images: add additional user guide images

– implementers-guide: convert to ODP standard layout

– implementers-guide: fix broken doxygen build from tarball

– users-guide: move EXTRA_DIST down to its makefile

– Makefile: add docs to the tarball

– improve asciidoc presentation

– users-guide convert to asciidoc

– images: add resource_management.msc for users-guide

– images: add svg for user-guide
* Validation

– performance: odp_pktio_perf: fix potential overflow in wait loop

– test/example: avoid “cycle” word usage

– ability to specify test install directory

– buffer: add tests for buffer alloc/free multi functions

– crypto: add test for AES128 CBC

– crypto: add test for HMAC-SHA-256-128

– crypto: limit packet size to maximum supported by platform

– packet: add tests for packet alloc/free multi functions

– queue: api validation tests for odp_queue_info()

– remove strict dependency on CUnit 2.1-3

– scheduler: add missing ticketlock unlock
* General:

– rpm packaging support

– linux-generic: config: increase ODP_CONFIG_SCHED_GRPS to 256

– linux-generic: cpumask: warn that CPU0 is used by control and worker thread

– linux-generic: packet: add implementation for packet alloc/free multi

– linux-generic: pool: add buffer_alloc_multi function

– linux-generic: pool: add implementation for buffer alloc/free multi

– linux-generic: queue: add odp_queue_info() function

– linux-generic: validation: add run-test script for post install testing

– platform: move list of API files to Makefile.inc so it is common to all platforms
