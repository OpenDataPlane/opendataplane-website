---
author: mike.holmes
comments: false
date: 2016-08-15 17:05:36+00:00
layout: post
link: https://www.opendataplane.org/news/odp-pcie-nic-performance-ofp-fpm_burstmode/
slug: odp-pcie-nic-performance-ofp-fpm_burstmode
title: ODP PCIe NIC Performance with OFP fpm_burstmode
wordpress_id: 2498
categories:
- News Hub
- Performance
image:
    featured: true
    path: /assets/images/posts/odp-thumb-pcie-nic-performance-ofp-fpm_burstmode.png
    name: odp-thumb-pcie-nic-performance-ofp-fpm_burstmode.png
---

When looking at PCIe NIC based systems performance can be assessed using the ODP PCIe optimised implementation (odp-dpdk, or the generic reference implementation odp-linux can be used, this implementation is not optimised for a specific platform.

Some representative numbers that use the OpenFastPath TCP stack and the fpm_burstmode test are shown here for a 40Gbps NIC.

  * with odp-dpdk scaling can be seen to be quite liner out to twelve cores


  * with the odp-linux reference implementation scaling is again good with  a lower overall throughput


The full [results](https://docs.google.com/spreadsheets/d/12KCE7ZYow_8Qq6Rd5NQmEnc9TQ5M_PfKx3X4mghgLds/edit?usp=sharing)

{% include image.html name="pubchart-burst-mode.png" alt="Burst Mode Chart" %}
