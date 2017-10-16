---
author: marshall.guillory
comments: false
date: 2015-10-30 16:22:05+00:00
layout: post
link: https://www.opendataplane.org/news/opendataplane-v1-4-0-release-published-to-the-repo/
slug: opendataplane-v1-4-0-release-published-to-the-repo
title: OpenDataPlane v1.4.0 Release published to the repo!
wordpress_id: 1760
categories:
- News Hub
tags:
- ARM
- Linaro Networking Group (LNG)
- networking
- NFV
- ODP
- OpenDataPlane
- release
- SDN
- Software Defined Networking
---

{% include image.html name="ODPv1.4.0tag-151x300.png" alt="ODPv1.4.0tag" url="http://opendataplane.org///wp-content/uploads/2014/01/ODPv1.4.0tag.png" %}

## The OpenDataPlane team is pleased to announce the v.1.4.0.0 release of the OpenDataPlane API's.


# General

  * The odp-netmap performance platform implementation  was merged as a compile time option to the linux generic reference


  * The odp-dpdk  performance platform implementation was updated to the 1.3 version of the ODP-API


  * Multiple classification validation tests added


  * The odp_cpu_cycles API was extended for multiple cores


  * l2fwd performance app fixes


  * pktio fixes

## New APIs

  * int odp_buffer_alloc_multi(odp_pool_t pool, odp_buffer_t buf, int num)


  * void odp_buffer_free_multi(const odp_buffer_t buf, int num)


  * int odp_cpumask_all_available(odp_cpumask_t * mask)


  * const char * odp_cpu_model_str(void)


  * const char * odp_cpu_model_str_id(int id)


  * uint64_t odp_cpu_hz(void)


  * uint64_t odp_cpu_hz_id(int id)


  * uint64_t odp_cpu_hz_max(void)


  * uint64_t odp_cpu_hz_max_id(int id)


  * void odp_pktio_print(odp_pktio_t pktio)


  * int odp_pktio_stats(odp_pktio_t pktio, odp_pktio_stats_t * stats)


  * int odp_pktio_stats_reset(odp_pktio_t pktio)


  * struct odp_pktio_stats_t odp_pktio_stats_t


  * int odp_packet_alloc_multi(odp_pool_t pool, uint32_t len, odp_packet_t pkt, int num)


  * void odp_packet_free_multi(const odp_packet_t pkt, int num)

## Removed APIS

  * uint64_t odp_sys_cpu_hz(void)


  * const char * odp_sys_cpu_model_str(void)

## JIRA issues in this release:
## Epic

  * [[ODP-11](https://projects.linaro.org/browse/ODP-11)] – ODP-NETMAP


  * [[ODP-12](https://projects.linaro.org/browse/ODP-12)] – Refine Role of CPI ID vs. Thread ID


  * [[ODP-164](https://projects.linaro.org/browse/ODP-164)] – ODP configuration limits should be exposed as APIs rather than #defines

## Story

  * [[ODP-20](https://projects.linaro.org/browse/ODP-20)] – odp_pmr_create() to also use odp_pmr_match_t type


  * [[ODP-73](https://projects.linaro.org/browse/ODP-73)] – odp_system_info_t cpu_hz Is not core specific


  * [[ODP-153](https://projects.linaro.org/browse/ODP-153)] – Generate multiple flows :- capability to generate multiple traffic profiles (flows of different packet size, rate, priority)


  * [[ODP-155](https://projects.linaro.org/browse/ODP-155)] – pcap capture:- use pcap capture to send to DUT for validation testing


  * [[ODP-157](https://projects.linaro.org/browse/ODP-157)] – transmit invalid packets :- Sending packets with incorrect fields and see if they are filtered by DUT


  * [[ODP-158](https://projects.linaro.org/browse/ODP-158)] – Offline analysis :- Investigate if we can generate traffic analysis on the fly or do it separately with different offline tool after saving the traffic to pcap.


  * [[ODP-177](https://projects.linaro.org/browse/ODP-177)] – ODP-DPDK needs to bump to full v2.1.0 from v2.1.0-rc3


  * [[ODP-182](https://projects.linaro.org/browse/ODP-182)] – Fix ODP scheduler validation scheduler_test_wait_time()


  * [[ODP-184](https://projects.linaro.org/browse/ODP-184)] – Update ODP-DPDK to ODP 1.3 API


  * [[ODP-187](https://projects.linaro.org/browse/ODP-187)] – Create test plan


  * [[ODP-194](https://projects.linaro.org/browse/ODP-194)] – Fix tick lost while timer counter or cycle counter overflow (time API and cpu API)


  * [[ODP-208](https://projects.linaro.org/browse/ODP-208)] – Getting right LNG x86_64 build for x86 traffic generator in Lava using OE rootfs

## Sub-task

  * [[ODP-181](https://projects.linaro.org/browse/ODP-181)] – Fix ODP odp_pktio_perf_test from time overflows


  * [[ODP-183](https://projects.linaro.org/browse/ODP-183)] – Fix linux-generic time API to return 0 when t2 = t1 for diff function

## GIT Repo tag information:

[ODP v1.4.0 tag](https://git.linaro.org/lng/odp.git/tag/?h=v1.4.0.0). Released. Features included in this release:
* API:

– **Classification**

– odp_cos_set_queue() renamed to odp_cos_queue_set()

– int odp_cos_set_drop renamed to odp_cos_drop_set()

– new: odp_queue_t odp_cos_queue(odp_cos_t cos_id)

– new: odp_drop_e odp_cos_drop(odp_cos_t cos_id)

– ODP_PMR_CUSTOM_FRAME support in classification

– odp_pmr_create() arguments passing change to use struct

– odp_pmr_match_set_create() added id argument

– **Config**

– new: odp_config_…() API introduced instead of ODP_CONFIG_ defines

– **Cpu, Threads and Scheduler**

– new: uint64_t odp_cpu_cycles(void)

– new: uint64_t odp_cpu_cycles_diff(uint64_t c1, uint64_t c2);

– new: uint64_t odp_cpu_cycles_max(void);

– new: uint64_t odp_cpu_cycles_resolution(void);

– odp_cpumask_def_worker() renamed to odp_cpumask_default_worker()

– odp_cpumask_def_control() renamed to odp_cpumask_default_control()

– odp init extended with num worker and control threads

– new: int odp_queue_lock_count(odp_queue_t queue);

– refine api doc for scheduler and schedule orderd locks

– argument of odp_schedule_order_lock() and odp_schedule_order_unlock changed to unsigned

– new: int odp_thread_count_max(void)

– **Packet**

– new: uint32_t odp_packet_flow_hash(odp_packet_t pkt)

– new: void odp_packet_flow_hash_set(odp_packet_t pkt, uint32_t flow_hash)

– new: int odp_packet_has_flow_hash(odp_packet_t pkt);

– new: void odp_packet_has_flow_hash_clr(odp_packet_t pkt);

– **Pktio**

– pktio can be configuread as receive or transmit only

– pktio: refined api doc for start() and stop()

– new: void odp_pktio_param_init(odp_pktio_param_t *param)
* ODP docs:

– implementers-guide: update names of test module libraries

– implementers-guide: update section on skipping tests
* Test framework

– update README files

– renaming module libs

– add odp_cunit_update() to modify registered tests

– add ability to mark tests inactive
* Validation

– **Classification**

– Add fix for classification tests

– remove redundant pool lookup function

– remove redundant sequence number check

– use tcp data offset field to calculate data offset

– move destroy_inq() to common file

– add odp_pktio_param_init() API

– added additional suite to test individual PMRs

– use a structure instead of many args for odp_pmr_create

– Add init calls for queue parameters

– syntax correction for CU_ASSERT

– Add init calls for pool parameters

– queue and drop policy API name change

– Queue parameter init calls

– **Cpu, Threads and Scheduler**

– rename odp_cpumask_def to _default

– schedule: revise definition of ordered locks

– schedule: remove odp_schedule_order_lock_init() API

– schedule: don’t check schedule time on 0

– synchronizers: support a single worker

– init: fix test when debug-print is disabled

– **Packet**

– packet: test flow hash

– packet: test now handles pool that do not support segmentation

– **Pktio**

– pktio: don’t call APIs with an invalid pktio handle

– **Config**

– config: removed ODP_CONFIG_MAX_THREADS

– config: add CUnit tests for config APIs
* Performance

– l2fwd: add missing braces

– l2fwd: add option to disable filling eth addresses

– l2fwd: add support for using odd number of ports

– l2fwd: fix crash when accuracy is set to 0

– l2fwd: add option to select scheduler queue type

– l2fwd: add option to change destination eth addresses

– l2fwd: obey -t in queue mode

– l2fwd: fill correct source ethernet address

– sched: update scheduling test to use cycle counts

– odp_pktio_perf: fix potential overflow for burst_gap

– odp_pktio_perf: fix potential overflow for send_duration
* general:

– classification: implement ODP_PMR_CUSTOM_FRAME matching

– classification: queue and drop policy API name change

– cpu: created arch dependent cpu_cycles files

– cpu: fix cycle lost while cycle counter overflow

– cpu: implementation for cycle count API

– cpu: rename time_cycles to cpu_cycles

– pktio: implemented pcap pktio

– pktio: implemented netmap pktio

– pktio: close all pktio when term is called

– pktio: enable classifier only when needed

– pktio: factor state management into packet_io

– pktio: fill in L2 parse results by default

– pktio: implement odp_pktio_param_init() API

– packet: implement flow hash support

– schedule: fix odp_schdule_wait_time

– queue: change lock_index from uint32_t to unsigned to match API

– queue: direct internal enqueues to target queue

– queue: fix pktout_enqueue() logic

– queue: remove obsolete prototypes

– use cycles_diff for time API also
