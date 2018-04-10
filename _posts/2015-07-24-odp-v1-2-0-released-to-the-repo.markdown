---
author: marshall.guillory
comments: false
date: 2015-07-24 13:17:02+00:00
layout: post
link: https://www.opendataplane.org/blog/odp-v1-2-0-released-to-the-repo/
slug: odp-v1-2-0-released-to-the-repo
title: ODP v1.2.0 Released to the repo!
wordpress_id: 1496
categories:
- News Hub
tags:
- Linaro Networking Group (LNG)
- networking
- Open source
- OpenDataPlane
- release
- SDN
- Software Defined Networking
---
{% include image.html  name="ODPv1.2.0tag-532x1024.png" alt="ODPv1.2.0tag" url="https://git.linaro.org/lng/odp.git/tag/?h=v1.2.0.0" %}

[ODP v1.2.0 tag](https://git.linaro.org/lng/odp.git/tag/?h=v1.2.0.0). was released. Re-planned v1.2.0 due to delays and re-prioritization from San Jose Engineering Sprint. Features released:
API:

– docs: doxygen grouping clean up and remove excess references to ODP

– pool: remove shm parameter from odp_pool_create()

– packet_io: clarify what happens when not all packets are sent

– cpumask: added default masks and cpumask_setall

– thrmask: added thread mask

– thread: added thread type
ODP helper:

– helper: convert to a library

– remove helper dependence on ODP internals

– helper: linux: check pthread_join return code

– test checksum

– helpers: fix udp checksum computation

– test: helper: add process and thread tests

– deleted odph_linux_cpumask_default
Test:
Validation:

– tests execution moved to platfrom side

– test: pktio_perf: add missing atomic init

– test: synchronizers: use thread_id instead of cpu_id to detect slow threa

– validation: pktio: do not dequeue from scheduled queue

– test: pktio_perf: fix pthread_t offset for tx threads

– packet_io: release unsent packets after odp_pktio_send()

– validation: new module errno

– test: pktio_perf: add missing ns to cycle conversion for busy loop

– validation: classification: fix ODP_PMR_IPPROTO capability check

– validation: scheduler: fix race condition in pause test

– test: do not use negative array index

– thread and cpumask validation suites

– example:ipsec: Fix for Polled queues

– scheduler: use number of workers

– example: classifier: fix string overflow
General:

– linux-generic: put pktio types to separate files with common interface.

– configure: use stricter warnings

– linux-generic: timer: use timer handles as buffer handles

– linux-generic: buffer: remove unneeded division/module when mapping within the first segment

– linux-generic: pool: use ODP_CONFIG_PACKET_SEG_LEN_MIN correctly

– queue: handle return value of odp_queue_enq()

– linux-generic: classification: add support for ODP_PMR_IPSEC_SPI

– add {EXEEXT} suffix to binaries

– event: implement odp_event_free()

– packet_socket: do not release packets in odp_pktio_send

– linux-generic: packet: fix byte order in IPv6 header parsing

– linux-generic: schedule: fix double free

– linux-generic: buffers: correct segment length calculation for packets

– linux-generic: timer: set timer queue to ODP_QUEUE_INVALID on init

– linux-generic: buffer: reduce field size and reorder for better packing

– linux-generic: crypto: eliminate buffer type hack for completions

– linux-generic: pool: remove double init

– linux-generic: pool: group and document pool statistics

– platform: Makefile.inc: use “ instead of != for compatibility with older versions of Make

– linux-generic: packet: Add lazy parsing support

– linux-generic: buffer: init all the odp_buffer_bits_t struct to avoid valgrind warnings
