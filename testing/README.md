---
title: Testing
description: |-
    ODP has a Jenkins build server testing ODP on ARM and X86 platforms, and reflecting the different ODP implementations supported by LNG. The build service performs various build, static analysis, cross compile and execution tests summarized below.
layout: default-plain
permalink: /testing/
---
## Testing

ODP has a Jenkins build server testing ODP on ARM and X86 platforms, and reflecting the different ODP implementations supported by LNG. The build service performs various build, static analysis, cross compile and execution tests summarized below.

#### Quality Control - Test Outputs

<div class="responsive-table">

<table id="TABLE_15">
<thead id="THEAD_16">

<tr id="TR_17">

<th colspan="1" id="TH_18">Output/Platform</th>

<th colspan="3" id="TH_19">
odp-linux
pktio types (Socket, Netmap, DPDK)
</th>

</tr>

</thead>

<tbody id="TBODY_21">

<tr id="TR_22">

<td id="TD_24" markdown="1">
**master**
</td>

<td id="TD_26" markdown="1">
**next**
</td>

<td id="TD_28" markdown="1">
**api-next**
</td>

</tr>

<tr id="TR_30">

<td id="TD_31">ODP API Doxygen Generation</td>

<td id="TD_32" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=master,build_type=dox_html,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/dox_html/latest/master/linux-generic-doxygen-html/index.html)
</td>

<td id="TD_35" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=master,build_type=dox_html,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/dox_html/latest/next/linux-generic-doxygen-html/index.html)
</td>

<td id="TD_38" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=api-next,build_type=dox_html,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/dox_html/latest/api-next/linux-generic-doxygen-html/index.html/index.html)
</td>

</tr>

<tr id="TR_41">

<td id="TD_42">Static Analysis (Coverity)</td>

<td id="TD_43" markdown="1">
[![Coverity Scan Build Status](https://scan.coverity.com/projects/2925/badge.svg)](https://scan.coverity.com/projects/2925)
</td>

</tr>

<tr id="TR_46">

<td id="TD_47">Clang Scan Results</td>

<td id="TD_48" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=master,build_type=scan_build,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/scan_build/latest/master/linux-generic-scan-build/index.html)
</td>

<td id="TD_51" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=next,build_type=scan_build,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/scan_build/latest/next/linux-generic-scan-build/index.html)
</td>

<td id="TD_54" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=api-next,build_type=scan_build,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/scan_build/latest/api-next/linux-generic-scan-build/index.html)
</td>

</tr>

<tr id="TR_57">

<td colspan="5" rowspan="1" id="TD_58">Code Coverage – LCOV</td>

</tr>

<tr id="TR_59">

<td id="TD_60">-Implementations</td>

<td id="TD_61" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=master,build_type=lcov,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/lcov/latest/master/linux-generic-lcov-html/index.html)
</td>

<td id="TD_64" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=next,build_type=lcov,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/lcov/latest/next/linux-generic-lcov-html/index.html)
</td>

<td id="TD_67" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=api-next,build_type=lcov,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/lcov/latest/api-next/linux-generic-lcov-html/index.html)
</td>

</tr>

<tr id="TR_70">

<td id="TD_71">-Tests</td>

<td id="TD_72" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=master,build_type=lcov,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/lcov/latest/master/linux-generic-validation-lcov-html/index.html)
</td>

<td id="TD_75" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=next,build_type=lcov,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/lcov/latest/next/linux-generic-validation-lcov-html/index.html)
</td>

<td id="TD_78" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=api-next,build_type=lcov,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/lcov/latest/api-next/linux-generic-validation-lcov-html/index.html)
</td>

</tr>

<tr id="TR_81">

<td id="TD_82">-Helpers</td>

<td id="TD_83" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=master,build_type=lcov,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/lcov/latest/master/linux-generic-helper-lcov-html/index.html)
</td>

<td id="TD_86" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=master,build_type=lcov,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/lcov/latest/next/linux-generic-helper-lcov-html/index.html)
</td>

<td id="TD_89" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-publish/GIT_BRANCH=master,build_type=lcov,label=docker-jessie-amd64,platform_type=generic)](http://docs.opendataplane.org/snapshots/odp-publish/generic/lcov/latest/api-next/linux-generic-helper-lcov-html/index.html)
</td>

</tr>

<tr id="TR_92">

<td id="TD_93">Cross Compile</td>

<td id="TD_94" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-api-check)](https://ci.linaro.org/jenkins/view/lng-ci/job/odp-api-check/)
</td>

<td id="TD_97" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-api-check)](https://ci.linaro.org/jenkins/view/lng-ci/job/odp-api-check/)
</td>

<td id="TD_100" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-api-check)](https://ci.linaro.org/jenkins/view/lng-ci/job/odp-api-check/)
</td>

</tr>

<tr id="TR_104">

<td id="TD_105">C++ app link test</td>

<td id="TD_106" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-tool-check/GIT_BRANCH=master,build_type=cpp_test,label=docker-utopic)](https://ci.linaro.org/view/odp-ci/job/odp-tool-check/GIT_BRANCH=master,build_type=cpp_test,label=docker-utopic/)
</td>

<td id="TD_109" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-tool-check/GIT_BRANCH=next,build_type=cpp_test,label=docker-utopic)](https://ci.linaro.org/view/odp-ci/job/odp-tool-check/GIT_BRANCH=next,build_type=cpp_test,label=docker-utopic/)
</td>

<td id="TD_112" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-tool-check/GIT_BRANCH=api-next,build_type=cpp_test,label=docker-utopic)](https://ci.linaro.org/view/odp-ci/job/odp-tool-check/GIT_BRANCH=api-next,build_type=cpp_test,label=docker-utopic/)
</td>

</tr>

<tr id="TR_116">

<td id="TD_117">M32 on 64 build</td>

<td id="TD_118" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-tool-check/GIT_BRANCH=master,build_type=m32_on_64,label=docker-jessie-amd64)](https://ci.linaro.org/view/odp-ci/job/odp-tool-check/)
</td>

<td id="TD_121" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-tool-check/GIT_BRANCH=next,build_type=m32_on_64,label=docker-jessie-amd64)](https://ci.linaro.org/view/odp-ci/job/odp-tool-check/)
</td>

<td id="TD_124" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-tool-check/GIT_BRANCH=api-next,build_type=m32_on_64,label=docker-jessie-amd64)](https://ci.linaro.org/view/odp-ci/job/odp-tool-check/)
</td>

</tr>

<tr id="TR_128">

<td id="TD_129">clang and M32 on 64 build</td>

<td id="TD_130" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-tool-check/GIT_BRANCH=master,build_type=clang_and_m32_on_64,label=docker-jessie-amd64)](https://ci.linaro.org/view/odp-ci/job/odp-tool-check/)
</td>

<td id="TD_133" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-tool-check/GIT_BRANCH=next,build_type=clang_and_m32_on_64,label=docker-jessie-amd64)](https://ci.linaro.org/view/odp-ci/job/odp-tool-check/)
</td>

<td id="TD_136" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-tool-check/GIT_BRANCH=api-next,build_type=clang_and_m32_on_64,label=docker-jessie-amd64)](https://ci.linaro.org/view/odp-ci/job/odp-tool-check/)
</td>

</tr>

<tr id="TR_140">

<td id="TD_141">distcheck</td>

<td id="TD_142" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-tool-check/GIT_BRANCH=master,build_type=distcheck,label=docker-utopic)](https://ci.linaro.org/view/odp-ci/job/odp-tool-check/)
</td>

<td id="TD_145" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-tool-check/GIT_BRANCH=next,build_type=distcheck,label=docker-utopic)](https://ci.linaro.org/view/odp-ci/job/odp-tool-check/)
</td>

<td id="TD_148" markdown="1">
[![](https://ci.linaro.org/jenkins/buildStatus/icon?job=odp-tool-check/GIT_BRANCH=api-next,build_type=distcheck,label=docker-utopic)](https://ci.linaro.org/view/odp-ci/job/odp-tool-check/)
</td>

</tr>

<tr id="TR_152">

<td id="TD_153">LAVA</td>

<td id="TD_154" markdown="1">
[make check](https://lng.validation.linaro.org/dashboard/image-charts/odp_make_check)
</td>

</tr>

<tr id="TR_159">

<td id="TD_160">Debian Build</td>

<td id="TD_161" markdown="1">
[![](https://ci.linaro.org/buildStatus/icon?job=build-odp-deb)](https://ci.linaro.org/view/odp-ci/job/build-odp-deb/)
</td>
</tr>
</tbody>
</table>

</div>



**Docker images for testing ODP patches with check-odp**

To replicate these results the CI scripts are available in the repo [check-odp.git](https://git.linaro.org/lng/check-odp.git) these scripts can be run locally on any machine.

To run the check-odp scripts in a docker container, follow the instructions at:  
[ubuntu](https://hub.docker.com/r/roxell/check-odp-ubuntu/)  
[fedora](https://hub.docker.com/r/roxell/check-odp-fedora/)

Additional instructions on executing these scripts in the exact docker image used by CI are given in this [document.](https://docs.google.com/document/d/1wRR3pNYC_V4akmD_dUm66VNpngt48wfPdoA_GLY0Z1Q "Follow link")
