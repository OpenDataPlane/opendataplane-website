---
title: Downloads
description: |-
    Download the latest version of the ODP reference from Git / other Open and Support
    Account Access implementation.
layout: container-breadcrumb
permalink: /downloads/
---
## Downloads
<div class="row">
<div class="col-md-6" markdown="1">
**Download the latest version
of the ODP reference from Git**
<div class="responsive-table">
<table id="TABLE_13">

<thead id="THEAD_14">

<tr id="TR_15">
<th> Repository description </th>
<th colspan="1" id="TH_17"> Git link </th>
</tr>

</thead>

<tbody id="TBODY_19">

<tr id="TR_20">
<td id="TD_21"> ODP API and Linux generic reference implementation </td>
<td id="TD_22" markdown="1">
[odp-linux](https://github.com/OpenDataPlane/odp.git)
</td>
</tr>

<tr id="TR_23">
<td id="TD_24"> ODP implementation utilizing DPDK </td>
<td id="TD_25" markdown="1">
[odp-dpdk](https://github.com/OpenDataPlane/odp-dpdk.git)
</td>
</tr>

</tbody>
</table>

</div>
</div>

<div class="col-md-6" markdown="1">

**Download other open source implementations of ODP**

<div class="responsive-table">

<table id="TABLE_51">

<thead id="THEAD_52">

<tr id="TR_53">

<th colspan="1" id="TH_54">Company</th>

<th colspan="1" id="TH_55">Repo</th>

<th colspan="1" id="TH_56">Supported Platforms</th>

</tr>

</thead>

<tbody id="TBODY_57">

<tr id="TR_58">

<td id="TD_59" markdown="1">
[![cavium](/assets/images/cavium.png)](http://www.cavium.com)
</td>

<td id="TD_62" markdown="1">
[Link](https://github.com/Linaro/odp-thunderx)
</td>

<td id="TD_64">ThunderX CN88xx 24-48 core ARMv8 OCTEON TX CN83/81xx 1-24 core ARMv8</td>

</tr>

<tr id="TR_67">

<td id="TD_68" markdown="1">
[![](/assets/images/kalray.png)](http://kalrayinc.com)
</td>

<td id="TD_71" markdown="1">
[Link](https://github.com/kalray/odp-mppa/)
</td>

<td id="TD_73">MPPA</td>

</tr>

<tr id="TR_74">

<td id="TD_75" markdown="1">
[![free](/assets/images/freescale.png)](http://nxp.com)
</td>

<td id="TD_78" markdown="1">
[Link](http://git.freescale.com/git/cgit.cgi/ppc/sdk/odp.git/?h=fsl_odp_v16.07_qoriq)
</td>

<td id="TD_80">QorIQ – ARM based DPAA2 architecture LS2080, LS2085 QorIQ – ARM & PowerPC based DPAA architecture LS1043</td>

</tr>

<tr id="TR_83">

<td id="TD_84" markdown="1">
[![texas](/assets/images/ti.png)](http://ti.com)
</td>

<td id="TD_87" markdown="1">
[Link](https://git.linaro.org/lng/odp-keystone2.git)
</td>

</tr>

<tr id="TR_90">
<td id="TD_91" markdown="1">
[![Marvell](https://www.marvell.com/assets/images/marvell-logo2.svg)](https://www.marvell.com)
</td>
<td id="TD_94" markdown="1">
[Link](https://github.com/MarvellEmbeddedProcessors/odp-marvell)
</td>
<td id="TD_96">Marvell ARMADA SoC Implementation.</td>
</tr>


</tbody>

</table>
</div>
</div>

<div markdown="1">

# Debian

If you have apt-add-repository you can use it

```bash
sudo apt-add-repository http://deb.opendataplane.org
```

If not you can do it manually

```bash
OS_RELEASE=jessie

wget -O - http://deb.opendataplane.org/odp.key > /tmp/odp.key sudo apt-key add /tmp/odp.key echo "deb http://deb.opendataplane.org ${OS_RELEASE} main"  |sudo tee /etc/apt/sources.list.d/odp.list


```

And then install ODP

```bash
ODPLIB_NAME=odp-linux or odp-dpdk
sudo apt-get update
sudo apt-get install -y git  libodphelper-linux-dev lib${ODPLIB_NAME}-dev
```

You can also try the script [hello world](http://opendataplane.org/hello-world/)


### OpenDataPlane odp-linux vs odp-dpdk

**odp-linux** can interface with DPDK poll mode drivers as an option vs the socket interface. However it retains everything else that is part of the generic Linux implementation, including for example the buffer management implementation.
The advantage is that compared to the default socket interface both the Netmap and DPDK pktios are faster when testing the generic case although no other hardware acceleration support is provided.

**odp-dpdk** is derived from odp-linux, but it is optimized using the full DPDK SDK, and tries to connect as much DPDK API’s to ODP as possible. It uses DPDK buffer management underneath, so it doesn’t need the aforementioned copy.

**odp-“x”** as can be seen various other open and closed implementations exist and they can be downloaded from the vendor for their hardware, the list is not exhaustive
</div>
