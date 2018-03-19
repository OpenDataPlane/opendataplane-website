---
author: mike.holmes
comments: false
date: 2016-12-09 15:33:13+00:00
layout: post
link: https://www.opendataplane.org/news/odp-openssl-upto-20x-performance-improvement-large-packets/
slug: odp-openssl-upto-20x-performance-improvement-large-packets
title: ODP with OpenSSL upto 20x performance improvement with large packets
wordpress_id: 2822
categories:
- News Hub
- Performance
image:
    featured: true
    path: /assets/images/posts/odp-thumb-openssl-upto-20x-performance-improvement.png
    name: odp-thumb-openssl-upto-20x-performance-improvement.png
---

OpenSSL is an open source project that provides a robust, commercial-grade, and full-featured toolkit for the Transport Layer Security (TLS) and Secure Sockets Layer (SSL) protocols, however it does not take advantage of SoC hardware acceleration.

The creation of an ODP plugin POC found in [GIT](https://git.linaro.org/people/nikhil.agarwal/ossl-odp.git/), shows what is possible.

{% include image.html name="image-10.png" alt="ODP with OpenSSL Image" %}


On the SoC used for this testing, the small packet performance when utilizing the HW offload was not abel to overcome the overhead of the transfer, this is a common problem that is worse if a PCI bus has to be negotiated.  This SoC has its engines attached more directly to the processor however the ARM CE instructions performance was still much better . By taking a hybrid approach which selects HW offload or on chip operations  the best compromise is reached.

Other SoCs will have a different profile and may find that the CPU is not required, this inflection point will be hidden from OpenSSL and the applications above it with the ODP implimentation / Plugin taking care to provide the best performance on a given platform. This plug in will utilize the ODP implementation linked to on a given system and those implimentation are optimized for the platform ensuring the best performance.

It is important to note that no changes are required to a system other than installing ODP and the OpenSSL plugin for it providing significant portable hardware acceleration.
