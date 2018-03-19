---
author: mike.holmes
comments: false
date: 2016-10-10 15:28:16+00:00
layout: post
link: https://www.opendataplane.org/news/las16-accelerating-applications-ofpodp/
slug: las16-accelerating-applications-ofpodp
title: 'LAS16: Accelerating applications with OFP+ODP'
wordpress_id: 2804
categories:
- News Hub
- Performance
image:
    featured: true
    path: /assets/images/posts/odp-thumb-las16-accelerating-applications-ofpodp.png
    name: odp-thumb-las16-accelerating-applications-ofpodp.png
---

At Linaro [Connect](http://connect.linaro.org/las16/) held recently in Las Vegas where it welcomed over 425 attendees a performance over view for ODP was given.

Discussion was focused on the performance of a current snapshot for ODP applications all  ruining using the [Monarch](http://opendataplane.org/odp-long-term-support-lts-release/) release on various hardware implementations of the ODP API.

Synthetic L3FWD performance was investigated on commodity and accelerated hardware both in the kernel and user space using differing numbers of cores.

For example it can be see than an acellerated platform using one core shows favorably to a simple in kernel solution, and that throughput scales well with the assignment of addtional cores, in this case limited in throughput by the single 20Gbit interface used.

{% include image.html name="odp-l3fwd-on-SoC.png" alt="Accelerating applications with OFP+ODP Image" %}

Additional investigations looked at accelerating Open-SSL, and again it can be seen that once the break even point for this specific implementation is reach the ODP plugin for OpenSSL provides dramatically more throughput using the openSSL benchmark. A small penalty is paid vs the pure on core processing at small packet sizes because the hybrid plugin dynamically determines if the HW offload should be used on a per case basis.

{% include image.html name="OpenSSL-SoC.png" alt="OpenSSL Image" %}


The full presention is avalable [Accelerating applications with OFP+ODP](http://connect.linaro.org/resource/las16/las16-401/)
