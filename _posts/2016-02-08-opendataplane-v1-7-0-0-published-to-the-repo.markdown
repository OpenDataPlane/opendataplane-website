---
author: marshall.guillory
comments: false
date: 2016-02-08 15:50:14+00:00
layout: post
link: https://www.opendataplane.org/news/opendataplane-v1-7-0-0-published-to-the-repo/
slug: opendataplane-v1-7-0-0-published-to-the-repo
title: OpenDataPlane v1.7.0.0 published to the repo!
wordpress_id: 1960
categories:
- News Hub
tags:
- ARM
- Connect
- Linaro
- Linaro Connect
- networking
- NFV
- ODP
- Open source
- OpenDataPlane
- Opensource
- release
- SDN
- Software Defined Networking
---
{% include image.html name="ODPv1.7.0.0tag-399x1024.png" alt="ODPv1.7.0.0tag Image"%}

[The OpenDataPlane team is pleased to announce the ODP v1.7.0.0](https://git.linaro.org/lng/odp.git/tag/refs/tags/v1.7.0.0) release of the OpenDataPlane API's. Features delivered:


## Epic


  * [[ODP-54](https://projects.linaro.org/browse/ODP-54)] – Throughput test for scheduler using ordered & atomic queues


  * [[ODP-73](https://projects.linaro.org/browse/ODP-73)] – odp_system_info_t cpu_hz Is not core specific


  * [[ODP-83](https://projects.linaro.org/browse/ODP-83)] – Port Counters and statistics


  * [[ODP-110](https://projects.linaro.org/browse/ODP-110)] – Packet IO interface control APIs


  * [[ODP-201](https://projects.linaro.org/browse/ODP-201)] – Preparing multi-node Lava script to run lava job


  * [[ODP-218](https://projects.linaro.org/browse/ODP-218)] – Improve support for odp_system


  * [[ODP-223](https://projects.linaro.org/browse/ODP-223)] – Add tests for pktin burst receive


  * [[ODP-226](https://projects.linaro.org/browse/ODP-226)] – Do not assume shared memory in tests or use helper


  * [[ODP-269](https://projects.linaro.org/browse/ODP-269)] – Correct termination path in timer example


  * [[ODP-300](https://projects.linaro.org/browse/ODP-300)] – Update ODP-DPDK to ODP 1.6 API level


  * [[ODP-315](https://projects.linaro.org/browse/ODP-315)] – classificatin validation should be more discrete and flexible




## Story






  * [[ODP-75](https://projects.linaro.org/browse/ODP-75)] – odp_pmr_set_t seems redundant handle type, use a list of odp_pmr_match_t instead


  * [[ODP-77](https://projects.linaro.org/browse/ODP-77)] – odp_pktio_t should be visible only on few calls e.g. odp_pktio_default_cos(pktio), use the default cos as synonym for an interface


  * [[ODP-243](https://projects.linaro.org/browse/ODP-243)] – per-CPU interface on PowerPC


  * [[ODP-244](https://projects.linaro.org/browse/ODP-244)] – per-CPU interface on OCTEON


  * [[ODP-245](https://projects.linaro.org/browse/ODP-245)] – Separate platform specific implementation into their own platform file if possible.


  * [[ODP-298](https://projects.linaro.org/browse/ODP-298)] – Develop example for global time API


  * [[ODP-305](https://projects.linaro.org/browse/ODP-305)] – Fix crypto API implementation to work with validation tests


  * [[ODP-306](https://projects.linaro.org/browse/ODP-306)] – Fix illegal instruction while accessing time registers


  * [[ODP-310](https://projects.linaro.org/browse/ODP-310)] – Test PMR creation with supported l3 PMR


  * [[ODP-314](https://projects.linaro.org/browse/ODP-314)] – assign default CoS before creating PMR chain


  * [[ODP-316](https://projects.linaro.org/browse/ODP-316)] – use real MAC addresses while packet creation




## Sub-task






  * [[ODP-307](https://projects.linaro.org/browse/ODP-307)] – Implement local time API


  * [[ODP-319](https://projects.linaro.org/browse/ODP-319)] – fix pktio_test_send_failure


  * [[ODP-321](https://projects.linaro.org/browse/ODP-321)] – Use odp_time_wait_ns() instead own implementation in pktio tests


  * [[ODP-324](https://projects.linaro.org/browse/ODP-324)] – fix MAC address assigment in pktio_test_start_stop validation test when one loop pktion is used


  * [[ODP-328](https://projects.linaro.org/browse/ODP-328)] – add validation tests for odp_cpu_cycles_* API


  * [[ODP-338](https://projects.linaro.org/browse/ODP-338)] – Correct shmem test to show treads nums


[OpenDataPlane v1.7.0.0](https://git.linaro.org/lng/odp.git/tag/refs/tags/v1.7.0.0)

* API:

– api: atomic: add non-relaxed 64bit operations

– api: atomic: added 32 bit acquire and release

– api: atomic: added 32bit cas_rel and cas_acq_rel

– api: atomic: added atomic min and max

– api: atomic: added atomic_lock_free_u64

– api: atomic: added cas operations

– api: atomic: added relaxed exchange operation

– api: atomic: init functions are not atomic

– api: atomic: rename release ordering

– api: classifier: align enum type naming

– api: cpu: add new API to get CPU max frequency

– api: cpu: add new API to get per-CPU current frequency

– api: cpu: add new API to get per-CPU max frequency

– api: cpu: add new API to get per-CPU model string

– api: cpu: added pause call

– api: cpu: make frequency API return 0 on failure

– api: cpumask: add new API odp_cpumask_all_available()

– api: cpumask: documented string format

– api: define pktio statistics api

– api: endian: rename endian types with odp_ prefix

– api: errno: any odp function can set errno

– api: init: align enum type naming

– api: init: removed platform_init struct definition

– api: pktio: added direct queue receive

– api: pktio: added direct send to pktio output queue

– api: pktio: added link status

– api: pktio: added multiple pktio input queues

– api: pktio: added multiple pktio output queues

– api: pktio: added pktio capability struct

– api: pktio: refine multiqueue API spec

– api: pktio: remove unused ODP_PKTIO_ANY

– api: pktio: rename pktio modes

– api: pool: allow per-thread caching

– api: queue: define queue type as enum

– api: queue: moved queue type into queue parameters

– api: queue: rename QUEUE_TYPE_POLL to _PLAIN

– api: sched: rename SCHED_SYNC_NONE to _PARALLEL

– api: schedule: clarify scheduler API documentation

– api: stdlib: added odp_memcmp

– api: sysinfo: move CPU Hz API to cpu.h

– api: sysinfo: move CPU model API to cpu.h

– api: thrmask: documented string format

– api: pktio: rename single_user param

– api: pktio: renames for compact type and func names

– api: queue: add enq and deq mode params
* ODP docs:

– doc/users-guide: add time API section

– doc/users-guide: add cryptographic services section

– doc: userguide: add application programming section

– doc: process-guide: add release process

– doc: images: replace overview with editable svg src

– doc: guides: embed icons and images in html

– doc: re-organize doxygen doc for synchronizer
* Validation

– test/performance: pktio: perform an initial warmup run

– test: change l2fwd pool size

– test: l2fwd: added poll queue mode

– test: l2fwd: re-organize functions

– test: l2fwd: use multi-queue API for scheduled queues

– test: l2fwd: use multi-queue pktio in direct mode

– test: l2fwd: use multiple queues in sched mode

– test: perf: l2fwd detect missing odp_generator

– test: update CPU Hz calling functions

– tests: harmonize posix extensions level defines

– validation: atomic: added cas test

– validation: atomic: added lock free op test

– validation: atomic: added max and min tests

– validation: atomic: added non-relaxed test

– validation: atomic: added xchg test

– validation: classification: add additional PMR term

– validation: classification: adds Test case for ODP_PMR_DIP_ADDR

– validation: classification: remove double frees

– validation: cls: adopt for supported l3 PMR

– validation: cls: assign default CoS before creating chain

– validation: cls: use correct MAC addresses

– validation: define ODP_TEST_INACTIVE and ODP_TEST_ACTIVE

– validation: implement pktio statistics counters

– validation: pktio: don’t continue if packet with > MTU is sent

– validation: pktio: fix check of pktio_stop() called twice

– validation: pktio: fix typo on setting in_mode

– validation: pktio: reduce stdout noise

– validation: pktio: test batch receive

– validation: pktio: use odp_time_ns() instead own function

– validation: pktio check for number of interfaces

– validation: pktio: add test for odp_pktio_recv_queue() and odp_pktio_send_queue()

– validation: pktio: add test for odp_pktout_queue_config()

– validation: pktio: add test for odp_pktin_queue_config()

– validation: possibility to inactive preconded test

– validation: queue: add test for odp_queue_to_u64()

– validation: remove remaining references synchronizers

– validation: removing synchronizers tests

– validation: scheduler: add timing tests for scheduled queue types

– validation: shmem: sync threads with barrier

– validation: stdlib: add odp_memcmp test

– validation: synchro tests split into 3 groups

– validation: system: add validation for new CPU APIs

– validation: system: add validation tests for odp_cpu_cycles_ calls

– validation: system: fix return code for checks

– validation: system: make odp_cpu_hz optional in validation test

– validation: system: make odp_cpu_hz_id conditional

– validation: test odp_pktio_link_status()

– validation: time: increase limit to check to 2 res

– validation: time: round up resolution

– validation: time: store local and global resolution

– validation: timer: fix delay after loop

– validation: timer: handle early exhaustion of pool
* General:

– linux-generic: add packet_io_stats.h to Makefile.am

– linux-generic: arch: renamed cpu arch files

– linux-generic: atomic: 32bit cas_rel and cas_acq_rel

– linux-generic: atomic: implemented exchange

– linux-generic: atomic: non-relaxed 64bit operations

– linux-generic: barrier: use API memory barrier

– linux-generic: classification: implement verify_pmr_dmac

– linux-generic: cpu: implemented pause

– linux-generic: define posix extension level once

– linux-generic: init: handle local/global init/term cleanly

– linux-generic: locks: replace internal atomics

– linux-generic: netmap: add functions for fetching pktio queues

– linux-generic: netmap: add initial multi queue support

– linux-generic: netmap: add netmap_close_descriptors() function

– linux-generic: netmap: add netmap_link_status() function

– linux-generic: netmap: add odp_pktio_capability()

– linux-generic: netmap: add odp_pktio_link_status()

– linux-generic: netmap: add odp_pktio_start()

– linux-generic: netmap: add scheduler multi-queue support

– linux-generic: netmap: add start()/stop() functionality

– linux-generic: netmap: disable debug prints

– linux-generic: netmap: fix MTU size

– linux-generic: netmap: fix netmap_mtu_get()

– linux-generic: netmap: implement pktio statistics

– linux-generic: netmap: map rings in netmap_start

– linux-generic: netmap: odp_pktio_recv() from all pktin queues

– linux-generic: netmap: use select() instead of poll() in recv

– linux-generic: packet: hide frame_len behind accessor

– linux-generic: packet_io: expose pktio_tbl and is_free()

– linux-generic: packet_io: fix array indexing in pktin_deq_multi()

– linux-generic: packet_io: separate locks for RX/TX

– linux-generic: pcap: implement pktio statistics counters

– linux-generic: pktio loop: implement statistics counters

– linux-generic: pktio: add RSS helper functions

– linux-generic: pktio: added poll type input queue

– linux-generic: pktio: added scheduler multi-queue support

– linux-generic: pktio: dummy multi-queue pktio

– linux-generic: pktio: enable using PKTIO_MAX_QUEUES in pktio implementations

– linux-generic: pktio: implement odp_pktio_link_status()

– linux-generic: pktio: print out the name of pktio used

– linux-generic: pktio: re-organize queue config code

– linux-generic: pktio: remove unwanted initialisation

– linux-generic: pktio: use multiqueue recv internally

– linux-generic: pool: accelerate buffer allocation marking

– linux-generic: pool: catch duplicate free errors in debug builds

– linux-generic: queue: check invalid handle in odp_queue_destroy

– linux-generic: remove direct include of endian.h from byteorder.h

– linux-generic: remove direct include of stdint.h by atomic.h

– linux-generic: remove direct include of stdlib.h by timer.h

– linux-generic: removed spin_internal

– linux-generic: scheduler: improve pktio polling

– linux-generic: sockets: implement pktio statistics

– linux-generic: sysinfo: apply per-CPU implementation to MIPS

– linux-generic: sysinfo: apply per-CPU implementation to PowerPC

– linux-generic: sysinfo: make the cpu_hz per-CPU data

– linux-generic: sysinfo: make the model_str per-CPU data

– linux-generic: sysinfo: move ARM system info codes to default arch file

– linux-generic: sysinfo: move MIPS system info codes to its plarform file

– linux-generic: sysinfo: move PowerPC system info codes to its plarform file

– linux-generic: sysinfo: move cpu_arch_str to odp_system_info_t

– linux-generic: sysinfo: move x86 system info codes to its plarform file

– linux-generic: sysinfo: rename odp_cpu_hz_current with odp_ prefix

– linux-generic: sysinfo: rename variable cpu_hz to cpu_hz_max

– linux-generic: sysinfo: revise odp_cpu_hz() to return current frequency

– linux-generic: sysinfo: set values for cpu_arch_str

– linux-generic: sysinfo: update dummy function to pass validation

– linux-generic: sysinfo: use uniform call odp_sysinfo_parser

– linux-generic: timer use SIGEV_THREAD_ID

– linux-generic: timer: limit notification about resolution incorrectness

– linux-generic: timer use SIGEV_THREAD_ID

– linux-generic: update CPU Hz calling functions
