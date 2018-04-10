---
author: shovan
comments: false
date: 2014-03-06 02:11:52+00:00
layout: post
link: https://www.opendataplane.org/blog/odp-showcased-lca14/
slug: odp-showcased-lca14
title: OpenDataPlane Project Showcased at Linaro Connect Asia 2014
wordpress_id: 408
categories:
- News Hub
tags:
- odp-showcased-lca14
---

This week the OpenDataPlane project was showcased at the Linaro Connect Asia conference in Macau, China.  In addition to a general project update session, sessions were held to provide a code walk through of an example ODP application as well as a roundtable to discuss early user experiences with using ODP.  This was followed by a technology demonstration showing applications running on ODP across a variety of platforms and processor architectures.


{% include image.html name="LCA14-Demo.png" alt="LCA14-Demo Image" %}

In the first demo, network traffic was passed between two ODP applications running on two different ARM-based SoC platforms while being snooped by an ODP-enhanced version of libpcap running on an x86 middlebox.  The snooped traffic was then forwarded to another x86 for display via Wireshark.


In the second demo, an ODP-enhanced version of OpenVPN was used to pass UDP traffic between an ARM-based Arndale processor and an x86 processor.


These demonstrations illustrated the cross-platform, cross-architecture goals of the ODP project: to provide a common API framework for use by data plane applications running across a variety of platforms and processor architectures.  Over the course of 2014 a number of additional ODP Reference implementations will be added covering more SoCs and architectures to further realize this goal, leading to a formal ODP Release 1.0 for later this year.


[Contact us for more infomation](/contact/)
