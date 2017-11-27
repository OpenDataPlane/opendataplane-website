---
title: Downloads
description: |-
    Download the latest version of the ODP reference from Git / other Open and Support
    Account Access implementation.
layout: default-plain
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

<th>
</th>

<th colspan="1" id="TH_17">odp-linux pktio types
(Socket, Netmap, DPDK)</th>

</tr>

</thead>

<tbody id="TBODY_19">

<tr id="TR_20">

<td rowspan="1" id="TD_21">Development Repo</td>

<td id="TD_22" markdown="1">
[![Development Repo Leaf Icon](/assets/images/leaf.png)](https://github.com/Linaro/odp.git)
</td>

</tr>

<tr id="TR_27">

<td rowspan="1" id="TD_28">Git Repo Tags</td>

<td id="TD_29" markdown="1">
[![Git Repo Tags Leaf Icon](/assets/images/leaf.png)](https://github.com/Linaro/odp/releases)
</td>

</tr>

<tr id="TR_34">

<td rowspan="1" id="TD_35">Patchworks</td>

<td id="TD_36" markdown="1">
[![Patchworks Leaf Icon](/assets/images/leaf.png)](http://patches.opendataplane.org/project/lng-odp/list/)
</td>

</tr>

<tr id="TR_41">

<td rowspan="1" id="TD_42">Latest Stable Release</td>

<td id="TD_43" markdown="1">
[![Monarch RC2 v1.10.1.0](/assets/images/leaf.png)](https://github.com/Linaro/odp/releases/tag/v1.11.0.0_monarch)
</td>

</tr>
</tbody>
</table>

</div>
</div>

<div class="col-md-6" markdown="1">

**Download other Open and Support
Account Access implementations**

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
[ODP Monarch](https://github.com/Linaro/odp-thunderx)
</td>

<td id="TD_64">ThunderX CN88xx 24-48 core ARMv8 OCTEON TX CN83/81xx 1-24 core ARMv8</td>

</tr>

<tr id="TR_67">

<td id="TD_68" markdown="1">
[![](/assets/images/kalray.png)](http://kalrayinc.com)
</td>

<td id="TD_71" markdown="1">
[ODP v1.6.0.0](https://github.com/kalray/odp-mppa/)
</td>

<td id="TD_73">MPPA</td>

</tr>

<tr id="TR_74">

<td id="TD_75" markdown="1">
[![free](/assets/images/freescale.png)](http://nxp.com)
</td>

<td id="TD_78" markdown="1">
[ODP Monarch](http://git.freescale.com/git/cgit.cgi/ppc/sdk/odp.git/?h=fsl_odp_v16.07_qoriq)
</td>

<td id="TD_80">QorIQ – ARM based DPAA2 architecture LS2080, LS2085 QorIQ – ARM & PowerPC based DPAA architecture LS1043</td>

</tr>

<tr id="TR_83">

<td id="TD_84" markdown="1">
[![texas](/assets/images/ti.png)](http://ti.com)
</td>

<td id="TD_87" markdown="1">
[ODP v1.6.0.0](https://git.linaro.org/lng/odp-keystone2.git)
</td>

</tr>

<tr id="TR_90">

<td id="TD_91" markdown="1">
[![linaro](/assets/images/linaro.png)](http://linaro.org)
</td>

<td id="TD_94" markdown="1">
[Monarch](https://git.linaro.org/lng/odp-dpdk.git)
</td>

<td id="TD_96">PCIe NIC optimised implementation (odp-dpdk)</td>

</tr>

<tr id="TR_90">
<td id="TD_91" markdown="1">
[![Marvell Armada](https://www.marvell.com/assets/images/marvell-logo2.svg)](https://www.marvell.com)
</td>
<td id="TD_94" markdown="1">
[Marvell Armada](https://github.com/MarvellEmbeddedProcessors/odp-marvell)
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

**odp-linux** can interface with DPDK poll mode drivers as an option vs the socket interface. However it retains everything else that is part of the generic Linux implementation, including for example the buffer management implementation. Therefore it has to copy everything during receive and transmit between its own buffers and DPDK ones.
The advantage is that compared to the default socket interface both the Netmap and DPDK pktios are faster when testing the generic case although no other hardware acceleration support is provided.

**odp-dpdk** is derived from odp-linux, but it is optimized using the full DPDK SDK, and tries to connect as much DPDK API’s to ODP as possible. It uses DPDK buffer management underneath, so it doesn’t need the aforementioned copy.

**odp-nextmap** does not exist, Netmap does not offer any additional acceleration features that need to be optimized for in a dedicated odp implementation.

**odp-“x”** as can be seen various other open and closed implementations exist and they can be downloaded from the vendor for their hardware, the list is not exhaustive
</div>
