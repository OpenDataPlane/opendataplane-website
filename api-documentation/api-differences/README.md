---
title: API/ABI Differences
description: |-
    The branch api-next is used to stage proposed APIs for inclusion ODP. The difference between these proposed APIs and the master branch of the validation model for ODP in linux-generic and other open performance implementations built by LNG CI are listed below.
layout: default-plain
permalink: /api-differences/
---
## API/ABI Differences

The branch api-next is used to stage proposed APIs for inclusion ODP. The difference between these proposed APIs and the master branch of the validation model for ODP in linux-generic and other open performance implementations built by LNG CI are listed below.

Additionally the difference in the API/ABI between the two common x86 implementations is shown with odp-linux vs. odp-dpdk


### odp-linux master vs. api-next ABI & API differences

<div class="responsive-table">

<table id="TABLE_14">

<thead id="THEAD_15">

<tr id="TR_16">

<th id="TH_17">Output/Platform</th>

<th id="TH_18">odp-linux, api-next: With pktio types  
(Socket, Netmap, DPDK)</th>

</tr>

</thead>

<tbody id="TBODY_20">

<tr id="TR_21">

<td id="TD_22">ABI difference: odp-linux, master</td>

<td id="TD_23"  markdown="1">
[![Leaf Icon](/assets/images/leaf.png)](http://docs.opendataplane.org/snapshots/odp-diff-abi-publish/generic/latest/diff-abi/libodp-compat_report.html)
</td>

</tr>

<tr id="TR_28">

<td id="TD_29">API difference: odp-linux, master</td>

<td id="TD_30"  markdown="1">
[![Leaf Icon](/assets/images/leaf.png)](http://docs.opendataplane.org/snapshots/odp-diff-api-publish/generic/latest/diff-api/odp.git-master_VS_odp.git-api-next-api-diff.txt)
</td>

</tr>

<tr id="TR_35">

<td id="TD_36">Helper ABI difference: odp-linux, master</td>

<td id="TD_37"  markdown="1">
[![Leaf Icon](/assets/images/leaf.png)](http://docs.opendataplane.org/snapshots/odp-diff-abi-publish/generic/latest/diff-abi/libodphelper-compat_report.html)
</td>

</tr>
</tbody>
</table>
</div>

### odp-linux vs. odp-dpdk ABI & API differences

<div class="responsive-table">
<table id="TABLE_45">

<tbody id="TBODY_46">

<tr id="TR_47">

<th id="TH_48" markdown="1">
**Output/Platform**
</th>

<th id="TH_50" markdown="1">
**odp-dpdk, master**
</th>

</tr>

<tr id="TR_52">

<td id="TD_53">ABI difference: odp-linux, master</td>

<td id="TD_54" markdown="1">
[![Leaf Icon](/assets/images/leaf.png)](http://docs.opendataplane.org/snapshots/odp-diff-abi-publish/dpdk/latest/diff-abi/libodp-compat_report.html)
</td>

</tr>

<tr id="TR_59">

<td id="TD_60">API difference: odp-linux, master</td>

<td id="TD_61" markdown="1">
[![Leaf Icon](/assets/images/leaf.png)](http://docs.opendataplane.org/snapshots/odp-diff-api-publish/dpdk/latest/diff-api/odp.git-master_VS_odp-dpdk.git-master-api-diff.txt)
</td>
</tr>

<tr id="TR_66">

<td id="TD_67">Helper ABI difference: odp-linux, master</td>

<td id="TD_68" markdown="1">
[![Leaf Icon](/assets/images/leaf.png)](http://docs.opendataplane.org/snapshots/odp-diff-abi-publish/dpdk/latest/diff-abi/libodphelper-compat_report.html)
</td>

</tr>

</tbody>

</table>
