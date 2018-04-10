---
author: marshall.guillory
comments: false
date: 2015-10-02 15:00:39+00:00
layout: post
link: https://www.opendataplane.org/blog/initial-ovs-odp-dpdk-performance-to-native-sdk-overhead-comparison/
slug: initial-ovs-odp-dpdk-performance-to-native-sdk-overhead-comparison
title: Initial OVS ODP-DPDK Performance to Native SDK Overhead Comparison
wordpress_id: 1713
categories:
- Demo
- News Hub
tags:
- Connect
- Demo
- Linaro Connect
- Linaro Networking Group (LNG)
- Linux on Arm
- LNG
- networking
- NFV
- ODP
- OpenDataPlane
- OpenVSwitch
- SDN
- SFO15
- Software Defined Networking
---
OpenDataPlane performance demonstrations were held at Linaro Connect San Francisco 2015 in Burlingame, CA on Thursday, September 24, 2015. There were eight demos from ODP members focusing on the breadth of the API's showcasing ODP's capabilities for dataplane performance enhancement.

The ODP API specification is nothing if it cannot efficiently abstract a platforms native SDK. The x86 case is interesting due to its incumbent legacy use case and that it attempts to offload only a minimal set of capability leaving a lot of the functionally to the CPU cluster. To begin to quantify the overhead of this worst case the most basic test case was run and results presented at Linaro connect San Francisco 2015.

## Current ODP OVS Performance Metrics (1.44% overhead)
{% include progress.html text="14.2 - 10 Gbps Theory" value="100.0" %}
{% include progress.html text="13.9 - OVS-DPDK " value="97.8" %}
{% include progress.html text="0.04 - OVS-ODP linux-generic" value="1" %}
{% include progress.html text="12 - OVS-ODP-DPDK @ HKG2015" value="84.5" %}
{% include progress.html text="13.8 - OVS-ODP-DPDK @ SFO2015" value="97.2" %}
* units are in Mpps as a percentage of theoretical maximum
