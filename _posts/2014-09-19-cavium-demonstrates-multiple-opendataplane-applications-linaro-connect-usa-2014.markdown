---
author: marshall.guillory
comments: false
date: 2014-09-19 18:43:35+00:00
layout: post
link: https://www.opendataplane.org/news/cavium-demonstrates-multiple-opendataplane-applications-linaro-connect-usa-2014/
slug: cavium-demonstrates-multiple-opendataplane-applications-linaro-connect-usa-2014
title: Cavium Demonstrates Multiple OpenDataPlane Applications at Linaro Connect USA
  2014
wordpress_id: 689
categories:
- News Hub
post_format:
- Image
---

On Thursday this week at Linaro Connect 2014 Cavium demonstrated a high performance implementation of ODP-IPSec packet processing on a Cavium MIPS SoC on both Linux-Userspace and Bare Metal runtime environments. The demo was able to produce 40GB/s IPSec ESP processing.

{% include image.html name="15096546938_9538f84d19_c.jpg" alt="ODP Event Image" %}

{% include media.html media_url="https://www.youtube.com/embed/tUwE1-IRdIQ" %}

Video courtesy of [armdevices.net](http://armdevices.net/)

### Objective

Demonstrate the performance effective implementation of ODP-IPSec packet processing
on Cavium SoC on Linux-Userspace and Bare Metal runtime environments.

**Features:**

  * IPSec ESP Processing (Authentication and Cipher)


  * 40G Line rate


  * Linux User Mode environment support


  * Bare metal environment support


  * Tunnel Mode


  * AES-CBC Cypher ( RFC 3602)


  * HMAC-SHA1-96 Authentication (RFC 2404)


  * Policy Management


  * Multiple SA support




### Test setup


Following diagram depicts the test setup. Following topology has been chosen to demonstrate the maximum throughput capability of CN68XX IPsec processing(40Gbps).


##### Hardware Description:



{% include image.html name="caviumipsecdemo.png" alt="Cavium IP Sec Image" %}


Device Under Test (ODP-IPSEC App) receives clear UDP packets and does the ESP IPSec packet processing (AES Ciphering and SHA1 authentication) in Tunnel mode and sends the packets back on the same interface at 40G line rate.

{% include image.html name="cavdemo1.png" alt="Cavium Demo 1 Image" %}

{% include image.html name="cavdemo2.png" alt="Cavium Demo 2 Image" %}

{% include image.html name="cavdemo3.png" alt="Cavium Demo 3 Image" %}

Related news:

[Cavium to Demonstrate Multiple OpenDataPlane™ (ODP) Applications at Linaro Connect USA 2014](http://www.marketwatch.com/story/cavium-to-demonstrate-multiple-opendataplane-odp-applications-at-linaro-connect-usa-2014-2014-09-17)
