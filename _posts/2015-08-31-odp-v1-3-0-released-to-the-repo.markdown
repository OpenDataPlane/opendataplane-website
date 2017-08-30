---
author: marshall.guillory
comments: false
date: 2015-08-31 19:38:24+00:00
layout: post
link: https://www.opendataplane.org/news/odp-v1-3-0-released-to-the-repo/
slug: odp-v1-3-0-released-to-the-repo
title: ODP v1.3.0 released to the repo!
wordpress_id: 1676
categories:
- News Hub
tags:
- Linaro Networking Group (LNG)
- networking
- NFV
- ODP
- OpenDataPlane
- release
- SDN
- Software Defined Networking
---
{% include image.html name="ODPv1.3.0tag-218x300.png" alt="ODPv1.3.0tag"%}

[ODP v1.3.0 tag](https://git.linaro.org/lng/odp.git/tag/refs/tags/v1.3.0.0). Released. Features included in this release:
**API**
– codespell: correct spelling

– event: change to odp_event_type_t

– init: use const pointer types

– packet_io: added odp_pktio_param_t

– packet_io: added start and stop

– packet_io: change word instance to interface

– pktio: added output mode

– pktio: rename pktio_input_mode enum

– pool: add odp_pool_param_init prototype

– pool: standardize description for odp_pool_param_init routine

– queue: add odp_queue_param_init prototype

– queue: clarify odp_queue_context_set() documentation

– queue: rename queue context get/set for consistency

– sched: added ordered context lock

– sched: added release ordered

– sched: added schedule group create and destroy

– sched: added schedule prefetch

– sched: added worker group

– sched: clarified synchronization context

– sched: clarify usage of PRIO_DEFAULT

– sched: moved scheduler types into new file

– sched: removed GROUP_DEFAULT

– sched: removed SYNC_DEFAULT

– sched: schedule param

– schedule: fix comment typo

– spelling fixes

– style: init api: documentation clean up
* ODP docs:

– doc: implementers-guide: add validation description

– doc: publish contributing text
* ODP helper:

– fix installation path for includes

– linux: catch possible undefined

– test: chksum: catch errors in scan_ip
* test:
* validation:

– add test on unused retvals

– use _CU_TEST_INFO() macro

– system: fix uninitialised variable

– test odp_pktio_start and odp_pktio_stop

– fix build from tar source

– kill odp_generator

– removing current dir from -I
* performance:

– Makefile: add scripts to EXTRA_DIST

– l2fwd: fix race condition between thread init and stat counter

– l2fwd: capture test fails

– odp_pktio_perf: use real MAC addresses while packet creation

– odp_scheduling: remove redundant var inits

– use odp_pool_param_init routine

– use odp_queue_param_init routine
* general:

– Makefile.am: fix basename conflicts

– Makefile: add all arch to the tarball

– fix logic for calling pktio init and term functions

– install missing headers

– move default cpumask functions to separate file

– move openssl checks inside linux-generic

– move pthread checks inside linux-generic

– add pktio_start and pktio_stop

– pktio: add global init and term function for pktios

– pktio: always test loop interface

– pktio: handle segmented packet in socket mode

– pktio: remove basic socket implementation

– pktio: store errno correctly in setup

– pool: add odp_pool_type_t enum

– pool: implement odp_pool_param_init

– queue: implement odp_queue_param_init routine

– remove linux-generic makefile generation from common configure.ac

– schedule pktin_poll: account pktio stop state

– Makefile.am: fix aclocal warning when building from tarball

– m4: pthread: fix warning with Wextra

– scripts/git_hash: change repo to CUSTOM_STR

– scripts/git_hash: fix build from tar source

– scripts: Makefile: add odp_version.sh to the tarball
