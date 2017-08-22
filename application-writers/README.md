---
title: Application Writers
description: |-
    Welcome to OpenDataPlane (ODP). This section of the web site is designed to provide information and resources of interest to data plane application writers. Here you’ll learn how to use ODP to create portable applications that take advantage of acceleration capabilities found in the diverse platforms that offer ODP implementations.
layout: default-stacked
permalink: /application-writers/
---
<div class="col-md-10" markdown="1">
# Application writers Home Page

Welcome to OpenDataPlane (ODP). This section of the web site is designed to provide information and resources of interest to data plane application writers. Here you’ll learn how to use ODP to create portable applications that take advantage of acceleration capabilities found in the diverse platforms that offer ODP implementations.
</div>
<div class="col-md-2">
    <a href="https://docs.opendataplane.org/snapshots/odp-publish/generic/usr_html/master/latest/linux-generic/output/faq.html">
        <img class="img-responsive center-block" src="/assets/images/faq_icon.png"/>
    </a>
</div>


![](/assets/images/packet_flow.svg){:.img-responsive}

# Programming Model

ODP applications consist of one or more threads (shown in yellow above) that use the ODP framework to perform packet processing. Everything else shown here is provided automatically by the ODP framework for applications. From Receive (RX) to Transmit (TX), ODP provides a range of APIs that encompass every stage of a packet’s processing. These APIs were carefully chosen not only to provide portability across all platforms offering ODP implementations, but to transparently exploit advanced hardware acceleration features found on many platforms. For example, many platforms offer hardware buffer and packet managers or queuing support. By using the ODP APIs this hardware will automatically be used to boost application performance while at the same time offering the same functionality on those platforms that offer optimized software implementations of these APIs.

# Polling and Event Driven Programming

ODP supports both polling and event driven programming models for packet processing, and applications are free to choose whatever model (or combination of the two) that best suits their needs. In a polling model threads poll I/O interfaces and event queues directly to look for work. In an event driven model, by contrast, threads call the ODP scheduler that selects work for them based on programmer-specified criteria. The scheduler offers superior scalability to many-core environments as well as advanced synchronization and context management features that simplify packet processing. These APIs are also implemented in hardware on many platforms, resulting in additional performance gains.

<div class="row">
    <div class="col-md-3 col-xs-6 feature">
        <a href="https://git.linaro.org/lng/odp.git">
            <img class="feature-image center-block" src="/assets/images/odp_linux_icon.png" alt="ODP Linux Git Icon"/>
        </a>
        <h4 class="text-center">odp-linux (Git)</h4>
    </div>
    <div class="col-md-3 col-xs-6 feature">
        <a href="http://docs.opendataplane.org/snapshots/odp-publish/generic/dox_html/master/latest/linux-generic-doxygen-html/index.html">
            <img class="feature-image center-block" src="/assets/images/api_icon.png" alt="API Docs Icon"/>
        </a>
        <h4 class="text-center">API Docs</h4>
    </div>
    <div class="col-md-3 col-xs-6 feature">
        <a href="http://docs.opendataplane.org/snapshots/odp-publish/generic/usr_html/master/latest/linux-generic/output/users-guide.html">
            <img class="feature-image center-block" src="/assets/images/user_guide_icon.png" alt="User Guide Icon"/>
        </a>
        <h4 class="text-center">User Guide</h4>
    </div>
    <div class="col-md-3 col-xs-6 feature">
        <a href="/comercial-support/">
            <img class="feature-image center-block" src="/assets/images/support_icon.png" alt="Support Icon"/>
        </a>
        <h4 class="text-center">Support</h4>
    </div>
</div>
<div class="row">
    <div class="col-md-3 col-xs-6 feature">
        <a href="https://collaborate.linaro.org/display/ODP/OpenDataPlane">
            <img class="feature-image center-block" src="/assets/images/meeting_icon.png" alt="Meeting Icon"/>
        </a>
        <h4 class="text-center">Meeting</h4>
    </div>
    <div class="col-md-3 col-xs-6 feature ">
        <a href="https://lists.linaro.org/mailman/listinfo/lng-odp">
            <img class="feature-image center-block" src="/assets/images/mailing_list_icon.png" alt="Mailing List Icon"/>
        </a>
        <h4 class="text-center">Mailing List</h4>
    </div>
    <div class="col-md-3 col-xs-6 feature">
        <a href="/applications/">
            <img class="feature-image center-block" src="/assets/images/existing_applications_icon.png" alt="Existing Applications Icon"/>
        </a>
        <h4 class="text-center">Existing Applications</h4>
    </div>
    <div class="col-md-3 col-xs-6 feature">
        <a href="/hello-world/">
            <img class="feature-image center-block" src="/assets/images/odp_hello_world_icon.png" alt="ODP Hello World Icon"/>
        </a>
        <h4 class="text-center">ODP Hello World</h4>
    </div>
</div>
