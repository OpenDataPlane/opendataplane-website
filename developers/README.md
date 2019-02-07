---
title: Developers
description: |-
    This section of the web site is designed to provide information and resources of interest to platform vendors who wish to provide an implementation of ODP on their platform. Here you’ll learn how ODP can enable you to compete for ODP applications by providing a tailored implementation that leverages the unique capabilities of your hardware to provide attractive price/performance targets for customers deploying ODP applications.
layout: jumbotron-container-left-sidebar
permalink: /developers/
---
Welcome to OpenDataPlane (ODP). This section of the web site is designed to provide information and resources of interest to platform vendors who wish to provide an implementation of ODP on their platform. Here you’ll learn how ODP can enable you to compete for ODP applications by providing a tailored implementation that leverages the unique capabilities of your hardware to provide attractive price/performance targets for customers deploying ODP applications.

## Portability and Performance

The platform vendor’s problem is clear. You have unique hardware that offers powerful advantages, but customers have neither the time nor expertise to rewrite or adapt their applications to your SDK. ODP solves this problem by providing a growing inventory of applications that can be easily ported to your platform without source code changes. At the same time, when these applications run on your platform they will automatically exploit your unique value-added features without customers having to modify their applications.

ODP solves this problem by defining a set of _abstract APIs_ that applications write to, and leaves it entirely up to each ODP implementation as to _how_ those APIs are realized on any given platform. This means that applications are not simply portable between platforms in a least-common-denominator way, but that the implementations of each ODP API can be optimized by the platform vendor however that vendor wishes. This can extend to platform model differences where certain APIs can be implemented in tuned software on one model while being able to exploit hardware features found on other models.  
ODP’s value to the platform writer is best seen in the following packet flow diagram:

{% include image.html name="packet_flow.svg" alt="Packet Flow Diagram" class="lazyload" %}


ODP applications consist of one or more _threads_ (shown in yellow above) that use the ODP framework to perform packet processing. Everything else shown here is provided automatically by the ODP framework for applications and _how_ these features are provided is entirely under the control of each implementation writer. From Receive (RX) to Transmit (TX), ODP provides a range of APIs that encompass every stage of a packet’s processing, and that are designed to enable platforms to showcase their value.

# Getting Started

To jumpstart your ODP implementation, ODP provides a number of _reference implementations_ that you can use immediately. The odp-linux reference implementation is a pure software implementation of ODP that can run on any platform that has a Linux kernel. Compiling and getting this implementation up and running on a new platform can typically be done in an afternoon. From there, platform vendors can start to replace the generic API implementations provided with ones tailored to their specific hardware. Since all ODP source code carries a BSD 3-clause license, vendors are free to reuse this code however they wish and are free to distribute their implementations of ODP in either an open or closed source manner, as determined by business needs.

# Validation Test Suite

An essential component of ODP is the _Validation Test Suite_. This is a comprehensive set of tests that can be run against any ODP implementation to validate that it correctly implements all APIs in the ODP specification. Implementers will make heavy use of this test suite during development to ensure that they are compliant to the ODP specification. Since this same test suite is used by application writers to validate conformance when selecting platforms, ODP relies on self-certification on the part of vendors for API conformance.


<div class="row">
    <div class="col-md-3 col-xs-6 feature">
        <a href="https://github.com/Linaro/odp/">
            <img class="feature-image center-block" src="/assets/images/git-icon.png" alt="Git Icon ODP"/>
        </a>
    </div>
    <div class="col-md-3 col-xs-6 feature">
        <a href="/testing/">
            <img class="feature-image center-block" src="/assets/images/testing-icon.png" alt="ODP Testing Icon"/>
        </a>
    </div>
    <div class="col-md-3 col-xs-6 feature">
        <a href="https://bugs.linaro.org/describecomponents.cgi?product=OpenDataPlane%20-%20linux-%20generic%20reference">
            <img class="feature-image center-block" src="/assets/images/bugs-icon.png" alt="ODP Bugs Icon"/>
        </a>
    </div>
    <div class="col-md-3 col-xs-6 feature">
        <a href="/api-documentation/index.html">
            <img class="feature-image center-block" src="/assets/images/APIS-icon.png" alt="ODP APIs Icon"/>
        </a>
    </div>
</div>
