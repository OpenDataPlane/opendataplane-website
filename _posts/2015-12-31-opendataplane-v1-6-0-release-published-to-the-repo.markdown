---
author: marshall.guillory
comments: false
date: 2015-12-31 12:00:32+00:00
layout: post
link: https://www.opendataplane.org/uncategorized/opendataplane-v1-6-0-release-published-to-the-repo/
slug: opendataplane-v1-6-0-release-published-to-the-repo
title: OpenDataPlane v1.6.0 Release published to the repo!
wordpress_id: 1920
tags:
- ARM
- Linaro
- Linaro Networking Group (LNG)
- LNG
- networking
- NFV
- ODP
- OpenDataPlane
- release
- SDN
- Software Defined Networking
---
{% include image.html name="ODPv1.6.0tag.png" alt="ODPv1.6.0tag"%}

[The OpenDataPlane team is pleased to announce the ODP v1.6.0](https://git.linaro.org/lng/odp.git/tag/refs/tags/v1.6.0.0) release of the OpenDataPlane API's. Features delivered:

## Epic

  * [[ODP-1](https://projects.linaro.org/browse/ODP-1)] – ODP – Open VSwitch (OVS)


  * [[ODP-2](https://projects.linaro.org/browse/ODP-2)] – ODP-DPDK


  * [[ODP-6](https://projects.linaro.org/browse/ODP-6)] – ODP Validation


  * [[ODP-7](https://projects.linaro.org/browse/ODP-7)] – API Examples & Documentation


  * [[ODP-10](https://projects.linaro.org/browse/ODP-10)] – API Performance


  * [[ODP-13](https://projects.linaro.org/browse/ODP-13)] – Native Apps


  * [[ODP-16](https://projects.linaro.org/browse/ODP-16)] – Linux-generic


  * [[ODP-30](https://projects.linaro.org/browse/ODP-30)] – Check helper/linux.c implementation


  * [[ODP-109](https://projects.linaro.org/browse/ODP-109)] – Investigate use of spinlocks in pktio implementation


  * [[ODP-137](https://projects.linaro.org/browse/ODP-137)] – Add traffic manager to ODP API


  * [[ODP-204](https://projects.linaro.org/browse/ODP-204)] – Investigate NGiNX performance on OFP


  * [[ODP-214](https://projects.linaro.org/browse/ODP-214)] – Investigate port of TREX to ODP


  * [[ODP-236](https://projects.linaro.org/browse/ODP-236)] – Unbind time measurements from cpu cycles and add new time API


  * [[ODP-265](https://projects.linaro.org/browse/ODP-265)] – Update release process in assciidoc


  * [[ODP-267](https://projects.linaro.org/browse/ODP-267)] – Modify OE recipe to use run-test script from ODP


  * [[ODP-296](https://projects.linaro.org/browse/ODP-296)] – Add documentation for time API


## Story

  * [[ODP-31](https://projects.linaro.org/browse/ODP-31)] – Check platfrom/linux-dpdk/odp_init.c implementation


  * [[ODP-84](https://projects.linaro.org/browse/ODP-84)] – Investigate ODP port for ivshmem


  * [[ODP-87](https://projects.linaro.org/browse/ODP-87)] – Lava setup for ivshmem-odp


  * [[ODP-134](https://projects.linaro.org/browse/ODP-134)] – Accelerated virtio requirement for arm v7 and v8


  * [[ODP-138](https://projects.linaro.org/browse/ODP-138)] – Patches for API-NEXT headerfiles


  * [[ODP-178](https://projects.linaro.org/browse/ODP-178)] – Update validation test to test new time API calls


  * [[ODP-190](https://projects.linaro.org/browse/ODP-190)] – Improve scheduler validation test to check sched time correctly


  * [[ODP-193](https://projects.linaro.org/browse/ODP-193)] – Add spinlock & rwlock tests


  * [[ODP-196](https://projects.linaro.org/browse/ODP-196)] – Use ODP time API instead of Posix API in performance test for scheduler


  * [[ODP-199](https://projects.linaro.org/browse/ODP-199)] – Port single DPDK driver for LAB NIC to PKTIO in ODP


  * [[ODP-234](https://projects.linaro.org/browse/ODP-234)] – Unbind CPU cycles from Time API implementation in linux-generic


  * [[ODP-237](https://projects.linaro.org/browse/ODP-237)] – Add resolution and delay calls to time API


  * [[ODP-238](https://projects.linaro.org/browse/ODP-238)] – Add global time API


  * [[ODP-239](https://projects.linaro.org/browse/ODP-239)] – Use same aproaches for operating with local and global time API


  * [[ODP-268](https://projects.linaro.org/browse/ODP-268)] – Decide on Proper Abstraction Level for CPU Isolation Support


  * [[ODP-270](https://projects.linaro.org/browse/ODP-270)] – CoS create function to take params


  * [[ODP-297](https://projects.linaro.org/browse/ODP-297)] – Add validation test for global time API


## Sub-task

  * [[ODP-263](https://projects.linaro.org/browse/ODP-263)] – Generate new repos


  * [[ODP-264](https://projects.linaro.org/browse/ODP-264)] – Attach new ODP repos to CI


[OpenDataPlane v1.6.0.0](https://git.linaro.org/lng/odp.git/tag/refs/tags/v1.6.0.0)
* API:

– api: atomic: clean atomic API documentation

– api: clib: added standard c library api

– api: hash: Added crc32 and crc32c hash functions

– api/linux-generic: classification: rename odp_drop_e to odp_cls_drop_t

– api/validation/linux-generic: classification: implement class of service create api

– api: time: add global time API

– api: time: add resolution and wait API calls

– api: time: make odp_local_time to be monotonic wall time

– api: init: allow implementation to use private ways for its own configuration

– api: classification: add odp_cls_cos_pool_set() api

– api: doc: re-organize doxygen doc for synchronizer

– api: rwlock_recursive: added recursive rwlock

– api: spinlock_recursive: added recursive spinlock

– api: crypto: Add AES128-GCM support

– api: thread: added THREAD_COUNT_MAX define

– api: thrmask: correct specification error

– api: pktio: add odp_pktio_print() API

– api: version: added implementation name str

– api: sync: removed odp_sync_stores

– api: barrier: added memory barriers
* ODP docs:

– doc/users-guide: add time API section

– doc/users-guide: add cryptographic services section

– doc: userguide: add application programming section

– doc: process-guide: add release process

– doc: images: replace overview with editable svg src

– doc: guides: embed icons and images in html

– doc: re-organize doxygen doc for synchronizer
* Validation

– api/validation/linux-generic: classification: implement class of service create api

– api: hash: Added crc32 and crc32c hash functions

– classification: add odp_cls_cos_pool_set() api

– classification: adds additional ASSERTS for stability

– classification: check return value of pktio stop

– classification: start pktio after setting inq and stop it before removing it

– classification: stronger checks to avoid SEGV on pktio failure

– crypto: add test for AES128-GCM

– crypto: allow custom auth/cipher range

– crypto: support validating both cipher and auth at the same time

– performance: pktio_perf: use odp_time_wait_ns() function instead of looping

– performance: sched: use ODP time API instead of clock_gettime

– performance: set a packet rate pass threshold for l2fwd

– pktio : Fix UDP checksum computation

– pktio: ability to wait for external network

– pktio: add customizable out mode for pktios

– pktio: add test for start when started and stop when stopped()

– pktio: add tests for rrecv() on WONLY, and send on RONLY pktios

– pktio: initialize mac addresses for all packets

– pktio: refactor error handling during sequence check

– pktio: remove unneeded stop as interface is stopped after open()

– pktio: stop interfaces before removing the default inq

– pktio: test odp_pktio_print()

– queue: refactor test to avoid coverity issues

– sched: improve scheduler validation test to check sched time correctly

– scheduler: use fail timeout when waiting on events in chaos

– std_clib: added validation tests

– synchronizers: add missing rwlock read lock functional test

– synchronizers: add recursive lock tests

– test/example: use local time API as wall time

– test: performance: pktio: don’t use direct arithmetic operations with odp_time_t

– time: add test convertsion on 0

– time: add test for odp_time_local_res() and use resolution

– time: add test for odp_time_wait_ns() and odp_time_wait_until()

– time: don’t assign int directly to odp_time_t

– time: test time constants in ns

– time: update to tes global time API

– validation: time: align tests with current time API
* General:

– align with new wall time API

– classification: add null check for pool assigned to CoS

– classification: define pkt_addr as const

– classification: implement class of service create api

– classification: implements odp_cls_cos_pool_set() api

– classification: rename odp_drop_e to odp_cls_drop_t

– clib: added standard c library api

– crypto: Add AES128-GCM support

– fix tap compilation

– hash: Added crc32 and crc32c hash functions

– include netmap headers with -isystem

– odp_time: don’t use cpu cycle API to get time

– packet: _odp_parse_common: arm build fix

– pktio: add odp_pktio_print() API

– pktio: add tap pktio type

– pktio: add test for tap pktio

– pktio: check for pktio_start when started and pktio_stop when stopped

– pktio: check interface mode is compatible before receiving or sending

– pktio: configuration functions check that interface is stopped

– queue: fix memory corruption in reorder_enq()

– rwlock_recursive: added recursive rwlock

– schedule: set sched_local.pool correctly

– schedule: use schedule time in ns

– socket: set up __odp_errno on ioctl failures

– spinlock_recursive: added recursive spinlock

– thread: added THREAD_COUNT_MAX define

– thread: removed internal max threads define

– time: add global time API

– time: add resolution and wait API calls

– time: remove posix bleed through on odp_time_t

– timer: include event_types instead of buffer_types

– validation: pktio: report test as skipped when setup fails

– validation: run config tests
