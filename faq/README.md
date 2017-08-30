---
title: FAQ
layout: default-plain
permalink: /faq/
specific_js:
- /assets/js/app/faq.js
- /assets/js/vendor/lightbox.min.js
---
<h4>FAQ</h4>
<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingOne">
      <h4 class="panel-title">
        <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseOne" aria-expanded="false" aria-controls="collapseOne">
          What is ODP?
        </a>
      </h4>
    </div>
    <div id="collapseOne" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingOne">
      <div class="panel-body">
      <p id="P_18">
          OpenDataPlane (ODP) is an open source API defined for networking data plane applications programming. The primary goal of ODP is to provide a common set of APIs for application portability across a diverse range of networking platforms (SoCs and servers) that offer various types of hardware acceleration. As an abstract API specification, ODP permits applications to run on and exploit the hardware offload capabilities of various platforms without requiring expertise in the nuances of any target platform.
      </p>
      <p id="P_19">
          At the same time, ODP is also a set of implementations of these APIs that are optimized for each platform that supports ODP. Implementations of ODP currently exist for a wide range of platforms spanning diverse instruction set architectures including ARM, MIPS, Power, x86, as well as proprietary SoC architectures, and include both general-purpose servers as well as specialized networking SoCs.
      </p>
      <p id="P_20">
          By decoupling the API definition from its implementation, ODP achieves two goals:
      </p>
      <ol id="OL_21" markdown="1">

          <li id="LI_22">
APIs can be defined to address data plane application needs rather than to expose specific platform capabilities. This leads to easy application portability across any platform that supports a conforming ODP implementation. The result is that applications written to the ODP APIs can run on any platform without developers needing expertise in the nuances of that platform:
          </li>
{% include image.html name="aboutODP1.png" alt="aboutODP1" %}
          <li id="LI_26">
              At the same time, by keeping APIs abstract, ODP allows vendors full freedom to implement these APIs in a manner optimized to the capabilities of each platform. This means that platforms can compete for any socket:<br id="BR_27" />
          </li>
{% include image.html name="aboutODP2.png" alt="aboutODP2" %}
      </ol>
      <p id="P_30">
          This freedom is further enhanced by ODP’s use of 3-clause BSD licensing. ODP APIs are fully open source and open contribution, however individual implementors of these APIs may choose to make their code open or closed source as business needs determine. As part of the main ODP distribution, several reference implementations of the ODP APIs are made available and these implementations are themselves open source and open contribution. These reference implementations are designed to offer a good starting point for those wishing to develop their own implementations of ODP tailored to their platform, or to gain experiencing developing ODP applications without needing anything other than a standard Linux platform.<br id="BR_31" /> Also included as part of ODP is a validation test suite that permits applications and vendors to confirm that a given ODP implementation conforms to the ODP API specification, thus ensuring consistency and portability across various implementations of ODP.
      </p>
      </div>
    </div>
  </div>
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingTwo">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
          What is NOT ODP?
        </a>
      </h4>
    </div>
    <div id="collapseTwo" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwo">
      <div class="panel-body">
      <p id="P_37">
          The data plane is the part of a network that carries user traffic. The data plane, the control plane and the management plane are the three basic components of a telecommunications architecture. The control plane and management plane serve the data plane, which bears the traffic that the network exists to carry. ODP is only concerned with the data plane.
      </p>
      </div>
    </div>
  </div>
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingThree">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
          Who is behind ODP?
        </a>
      </h4>
    </div>
    <div id="collapseThree" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingThree">
      <div class="panel-body">
      <p id="P_43">
          ODP is sponsored by the Linaro Networking Group (LNG) and its 13 member companies. These companies include network system vendors, silicon vendors, and software solution providers who are working to promote a truly cross platform solution for data plane applications that is portable across a wide range of network silicon yet can take full advantage of hardware acceleration and offload capabilities offered by these platforms.
      </p>
      </div>
    </div>
  </div>
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingFour">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFour" aria-expanded="false" aria-controls="collapseFour">
          What are the goals of ODP?
        </a>
      </h4>
    </div>
    <div id="collapseFour" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFour">
      <div class="panel-body">
      <ul id="UL_49">
          <li id="LI_50">
              To support Software-defined networking (SDN) in which control is decoupled from the physical infrastructure, allowing network administrators to support a network fabric across multi-vendor equipment.
          </li>
          <li id="LI_51">
              To support Network function virtualization (NFV) which is an initiative to virtualize the network services that are now being carried out by proprietary hardware.
          </li>
          <li id="LI_52">
              To enable a platform agnostic open source community to develop hardware accelerated software that is very portable.
          </li>
      </ul>
      </div>
    </div>
  </div>
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingFive">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFive" aria-expanded="false" aria-controls="collapseFive">
          What is the ODP project history and status?
        </a>
      </h4>
    </div>
    <div id="collapseFive" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFive">
      <div class="panel-body">
      <p id="P_58">
          The ODP project was launched in 2013. The first full-feature release of ODP occurred in March of 2015 and a production-ready release is targeted for year end 2015.
      </p>
      <p id="P_59">
          The history can be seen in the git stats for the the first implementation, the linux-generic reference [2].
      </p>
      </div>
    </div>
  </div>
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingSix">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseSix" aria-expanded="false" aria-controls="collapseSix">
          Where does ODP fit in the solution space?
        </a>
      </h4>
    </div>
    <div id="collapseSix" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingSix">
      <div class="panel-body">
      <p id="P_65" markdown="1">
{% include image.html name="aboutODP3.png" alt="aboutODP3" %}
      </p>
      <p id="P_67">
          Although ODP applications are independent of available network speeds, at present the benefits of ODP are best seen on networks operating at 10Gb/s and above. This allows ODP applications to transition seamlessly from software-based acceleration found on general purpose servers to hardware acceleration found on specialized networking SoCs. At present this spans the “sweet spot” of speeds from 10Gb/s to 100Gb/s. Beyond 100Gb/s ODP abstractions have not matured enough to completely describe full offload processing, although this is a long term goal.
      </p>
      </div>
    </div>
  </div>


  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingSeven">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseSeven" aria-expanded="false" aria-controls="collapseSeven">
          What does a typical application packet flow look like?
        </a>
      </h4>
    </div>
    <div id="collapseSeven" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingSix">
      <div class="panel-body">
          <p id="P_73">
                An application written as a clean room implementation will differ in structure from one ported from a legacy application allowing it to benefit from more of the ODP capabilities, a typical structure for a new application is shown below:
            </p>
            <p id="P_74" markdown="1">
{% include image.html name="aboutODP4.png" alt="aboutODP4" %}
            </p>
            <p id="P_76">
                Using the scheduler and an event driven model, packets are distributed to available workers maximizing the capacity of the cores. Where possible, the function will be performed in hardware (red). Migrating to a device where more of the functionality is in hardware will result in greater throughput without rewriting the application. In addition, migration to a device with more cores will automatically spread the load achieving greater throughput.
            </p>
            <p id="P_77">
                In summary:
            </p>
            <ul id="UL_78">
                <li id="LI_79">
                    The classifier might be fixed-function or programmable (for flexibility as network protocols evolve)
                </li>
                <li id="LI_80">
                    The scheduler is similar to a traffic manager
                </li>
                <li id="LI_81">
                    Processing cores can be added and removed dynamically (elasticity)
                </li>
                <li id="LI_82">
                    The scheduler knows which core is associated with which queue at every moment, which enables hardware synchronisation
                </li>
                <li id="LI_83">
                    Packets and other types of work (e.g. timers) are scheduled together
                </li>
            </ul>
      </div>
    </div>
  </div>

  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingEight">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseEight" aria-expanded="false" aria-controls="collapseEight">
            What does the ODP software stack look like?
        </a>
      </h4>
    </div>
    <div id="collapseEight" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingEight">
      <div class="panel-body">
          <p id="P_89" markdown="1">
{% include image.html name="ODP_Arch_v3.png" alt="ODP_Arch_v3" %}
          </p>
          <p id="P_91">
              An application written to the ODP API will be linked to the ODP implementation for the platform on which it is executing. This implementation will have been optimized for that specific hardware; it will often call the native SDK via an inline call, which also allows the application to simultaneously take advantage of vendor extensions that have not yet been standardized.
          </p>
      </div>
    </div>
  </div>


  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingNine">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseNine" aria-expanded="false" aria-controls="collapseNine">
            What platforms does ODP support?
        </a>
      </h4>
    </div>
    <div id="collapseNine" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingNine">
      <div class="panel-body">
      <p id="P_97">
          To date, ODP is running on seven different network platforms that span five different processing architectures (ARMv7, ARMv8, MIPS64, Power, and x86), offering both application portability and accelerated performance tailored to each platform. Other implementations are under development by both LNG member companies and other companies participating in the project.
      </p>
      </div>
    </div>
  </div>

  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingTen">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTen" aria-expanded="false" aria-controls="collapseTen">
            What OS is typically used with ODP?
        </a>
      </h4>
    </div>
    <div id="collapseTen" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTen">
      <div class="panel-body">
      <p id="P_103">
          ODP applications usually run as Linux user space applications, but there are also a number of “bare metal” environments in use. A typical deployment will be using Linux as the control node on at least one CPU and then using the NO_HZ and isolation features of Linux to essentially run the application’s fast-path packet processing code as if it were using “bare metal” on the remaining cores.
      </p>
      </div>
    </div>
  </div>


  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingEleven">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseEleven" aria-expanded="false" aria-controls="collapseEleven">
            Is ODP open?
        </a>
      </h4>
    </div>
    <div id="collapseEleven" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingEleven">
      <div class="panel-body">
      <p id="P_109">
          ODP is a true open source, open contribution project that is distributed under a 3-clause BSD license, meaning that anyone is free to use, modify and distribute it for commercial or other purposes without restriction.
          <br id="BR_110" /> ODP has a public mailing list (<a href="mailto:lng-odp@lists.linaro.org" id="A_111">lng-odp@lists.linaro.org</a>), and discussion on this list shows the wide base of participation in the ODP project. There are also a number of independent externally hosted ODP implementations [6].
      </p>
      </div>
    </div>
  </div>

  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingTwelve">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwelve" aria-expanded="false" aria-controls="collapseTwelve">
            What is linux-generic?
        </a>
      </h4>
    </div>
    <div id="collapseTwelve" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwelve">
      <div class="panel-body">
      <p id="P_117">
          The ODP linux-generic implementation is a functional reference targeting simplicity over performance if there is marked difference. The higher-performance implementations of ODP come directly from the vendors. Linaro also maintains implementations for some other important platforms that do not yet have direct vendor support [3].
      </p>
      </div>
    </div>
  </div>


  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingThirteen">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseThirteen" aria-expanded="false" aria-controls="collapseThirteen">
            Does ODP really help portability?
        </a>
      </h4>
    </div>
    <div id="collapseThirteen" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingThirteen">
      <div class="panel-body">
      <p id="P_126">
          Yes. ODP abstracts hardware capabilities for dataplane processing so that applications may be written more portably Application developers may make use of important hardware capabilities such as crypto hardware acceleration without needing deep knowledge of the hardware or the vendor-specific SDK associated with it. This will make it much easier for them to write portable applications that work well across multiple hardware implementations.
      </p>
      </div>
    </div>
  </div>

  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingFourteen">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFourteen" aria-expanded="false" aria-controls="collapseFourteen">
            Can ODP interoperate with a native SDK?
        </a>
      </h4>
    </div>
    <div id="collapseFourteen" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFourteen">
      <div class="panel-body">
      <p id="P_126">
          Yes.
      </p>
      </div>
    </div>
  </div>

  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingFifteen">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFifteen" aria-expanded="false" aria-controls="collapseFifteen">
            Does ODP allow software extensions?
        </a>
      </h4>
    </div>
    <div id="collapseFifteen" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFifteen">
      <div class="panel-body">
      <p id="P_138">
          No. the ODP API does not allow for software extensions. However, ODP does not preclude calling a vendor’s SDK in parallel with ODP but the expectation is that over time any features that become common to multiple platforms will be supported in future versions of the portable ODP APIs.
      </p>
      </div>
    </div>
  </div>


  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingSixteen">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseSixteen" aria-expanded="false" aria-controls="collapseSixteen">
            Does ODP work with FPGAs?
        </a>
      </h4>
    </div>
    <div id="collapseSixteen" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingSixteen">
      <div class="panel-body">
      <p id="P_144">
          There is no explicit initialization support for altering the image in an FPGA at boot time, but several major players have looked at ODP and we hope they will help define the support they require.
      </p>
      </div>
    </div>
  </div>


  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingSeventeen">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseSeventeen" aria-expanded="false" aria-controls="collapseSeventeen">
            Does ODP work with NICs?
        </a>
      </h4>
    </div>
    <div id="collapseSeventeen" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingSeventeen">
      <div class="panel-body">
          <p id="P_150">
              So far, ODP has been vigorously taken up by vendors who supply much more functionality in their hardware than a plain NIC can provide. One of those vendors package this capability as a NIC + ODP library. The ODP project also supports its own ODP-DPDK [1] implementation to help ensure that polling mode applications can continue to work even without picking up any of the new capabilities.
          </p>
      </div>
    </div>
  </div>



  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingEighteen">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseEighteen" aria-expanded="false" aria-controls="collapseEighteen">
            Does ODP support polling mode?
        </a>
      </h4>
    </div>
    <div id="collapseEighteen" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingEighteen">
      <div class="panel-body">
          <p id="P_156">
              ODP does not dictate a model, although the majority of current contributors see greater value in an event-driven model which which it is felt will scale better than a polling mode driver.
          </p>
      </div>
    </div>
  </div>



  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingNineteen">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseNineteen" aria-expanded="false" aria-controls="collapseNineteen">
            Does ODP add a lot of overhead vs. the native SDK?
        </a>
      </h4>
    </div>
    <div id="collapseNineteen" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingNineteen">
      <div class="panel-body">
          <p id="P_162">
              No, ODP is just an API designed by the contributors. The implementation is developed by the hardware vendor to be optimal for their platform.
          </p>
      </div>
    </div>
  </div>

  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingTwenty">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwenty" aria-expanded="false" aria-controls="collapseTwenty">
            What is the difference between ODP and DPDK?
        </a>
      </h4>
    </div>
    <div id="collapseTwenty" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwenty">
      <div class="panel-body">
          <p id="P_168">
              ODP is an API, DPDK is a specific implementation of an API.
          </p>
          <p id="P_169">
              ODP is an abstraction that is just at a high-enough level to allow platform abstraction without imposing strict models and overheads.
          </p>
      </div>
    </div>
  </div>

  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingTwentyOne">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwentyOne" aria-expanded="false" aria-controls="collapseTwentyOne">
            Does ODP force the use of specific structures?
        </a>
      </h4>
    </div>
    <div id="collapseTwentyOne" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwentyOne">
      <div class="panel-body">
      <p id="P_175" markdown="1">
{% include image.html name="aboutODP6.png" alt="aboutODP6" %}
      </p>
      <p id="P_177">
          ODP uses abstractions for the structures that are defined by the implementing vendor so that they map closely to the hardware and are very efficient. The application may then access this data though inline functions so that platform specific data is never exposed, for example odp_packet_len() [5] to determine a packet length.
      </p>
      </div>
    </div>
  </div>


  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingTwentyTwo">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwentyTwo" aria-expanded="false" aria-controls="collapseTwentyTwo">
            Does ODP have legacy application support?
        </a>
      </h4>
    </div>
    <div id="collapseTwentyTwo" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwentyTwo">
      <div class="panel-body">
      <p id="P_183">
          ODP can be used to implement hardware acceleration for interfaces for sockets, or polling mode drivers.
      </p>
      </div>
    </div>
  </div>

  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingTwentyThree">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwentyThree" aria-expanded="false" aria-controls="collapseTwentyThree">
            Does ODP provide everything needed for an application?
        </a>
      </h4>
    </div>
    <div id="collapseTwentyThree" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwentyThree">
      <div class="panel-body">
          <p id="P_189">
              No. ODP is defining the lowest level abstractions for hardware acceleration and it is expected that layers of software using these primitives will be able to add deeper application support. In addition ODP does not try to add Operating System abstractions.
          </p>
      </div>
    </div>
  </div>

  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingTwentyFour">
      <h4 class="panel-title">
        <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwentyFour" aria-expanded="false" aria-controls="collapseTwentyFour">
            What are ODP Dataplane Applications?
        </a>
      </h4>
    </div>
    <div id="collapseTwentyFour" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwentyFour">
      <div class="panel-body">
          <p id="P_195">
              They are traditionally the software in routers, switches, gateways, set top boxes, Evolved Node B, etc. Increasingly they are datacenter applications that can make use of the acceleration features available in servers, such as Open vSwitch [4] and SNORT.
          </p>
      </div>
    </div>
  </div>

</div>

<h4>Build</h4>

<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">

    <div class="panel panel-default">
      <div class="panel-heading" role="tab" id="headingTwoOne">
        <h4 class="panel-title">
          <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwoOne" aria-expanded="false" aria-controls="collapseTwoOne">
              How do I compile ODP with modified CFLAGS such as optimization flags zero (0)?
          </a>
        </h4>
      </div>
      <div id="collapseTwoOne" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwoOne">
        <div class="panel-body">
        <p id="P_209">
            Basically you need to pass -O0 to gcc, You can bake this into the generated makefile with the ./configure step, that is probably your simplest step.
        </p>
        <p id="P_210">
            Also see the gcc manual and possibly ask on stackoverflow for more details on using gnu tools.
        </p>
        <p id="P_211">
            To build this change into the makefile at the configure step, do this
        </p>
        <pre id="PRE_212"><code id="CODE_213">./configure CFLAGS="-O0"
make</code>
        </pre>
        <p id="P_214">
            look for the following in the configure output:
        </p>
        <pre id="PRE_215">
        <code id="CODE_216">
cc: gcc
cppflags:
am_cppflags: -I/tmp/check-odp/installed/x86_64/cunit-2.1-3/include
am_cxxflags: -std=c++11
cflags: -O0
                </code>
            </pre>
        </div>
      </div>
    </div>

    <div class="panel panel-default">
      <div class="panel-heading" role="tab" id="headingTwoTwo">
        <h4 class="panel-title">
          <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwoTwo" aria-expanded="false" aria-controls="collapseTwoTwo">
              With valgrind I see “Conditional jump or move depends on uninitialized value”...
          </a>
        </h4>
      </div>
      <div id="collapseTwoTwo" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwoTwo">
        <div class="panel-body">
            <p id="P_222">
                This is a known issue in many cases, it is related to the use of some tricks to get strong typing out of C99 source code.
            </p>
            <pre id="PRE_223">
                <code id="CODE_224">
strong_types.h
….
/** Use strong typing for ODP types */
#define odp_handle_t struct { uint8_t unused_dummy_var; } *

                </code>
            </pre>
            <p id="P_225">
                If anyone knows how to inform valgrind that this is in fact correctly initialized it would be most welcome?
            </p>
        </div>
      </div>
    </div>

    <div class="panel panel-default">
      <div class="panel-heading" role="tab" id="headingTwoThree">
        <h4 class="panel-title">
          <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwoThree" aria-expanded="false" aria-controls="collapseTwoThree">
              When I compile I get errors with _CU_TEST_INFO...
          </a>
        </h4>
      </div>
      <div id="collapseTwoThree" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwoThree">
        <div class="panel-body">
        <p id="P_231">
            Question:
            <br id="BR_232" /> When I compile I get errors with _CU_TEST_INFO
            <br id="BR_233" /> make[3]: Entering directory `/home/&lt;me&gt;/odp/test/
            <wbr id="WBR_234" />validation/buffer’
            <br id="BR_235" /> CC buffer.lo
            <br id="BR_236" /> buffer.c:146:2: error: initialization discards ‘const’ qualifier from pointer target type [-Werror]
            <br id="BR_237" /> _CU_TEST_INFO(buffer_test_
            <wbr id="WBR_238" />pool_alloc),
        </p>
        <p id="P_239">
            Answer:
            <br id="BR_240" /> Check the DEPENDENCIES file most likely with any CU macro error you are not using the correct version of cunit.
        </p>
        </div>
      </div>
    </div>

    <div class="panel panel-default">
      <div class="panel-heading" role="tab" id="headingTwoFour">
        <h4 class="panel-title">
          <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwoFour" aria-expanded="false" aria-controls="collapseTwoFour">
              When I compile I get errors with _CU_TEST_INFO...
          </a>
        </h4>
      </div>
      <div id="collapseTwoFour" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwoFour">
        <div class="panel-body">
        <p id="P_231">
            Question:
            <br id="BR_232" /> When I compile I get errors with _CU_TEST_INFO
            <br id="BR_233" /> make[3]: Entering directory `/home/&lt;me&gt;/odp/test/
            <wbr id="WBR_234" />validation/buffer’
            <br id="BR_235" /> CC buffer.lo
            <br id="BR_236" /> buffer.c:146:2: error: initialization discards ‘const’ qualifier from pointer target type [-Werror]
            <br id="BR_237" /> _CU_TEST_INFO(buffer_test_
            <wbr id="WBR_238" />pool_alloc),
        </p>
        <p id="P_239">
            Answer:
            <br id="BR_240" /> Check the DEPENDENCIES file most likely with any CU macro error you are not using the correct version of cunit.
        </p>
        </div>
      </div>
    </div>

</div>

<h4>Quality Control - Testing, Verification and Validation</h4>

<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">

<div class="panel panel-default">
  <div class="panel-heading" role="tab" id="headingThreeOne">
    <h4 class="panel-title">
      <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseThreeOne" aria-expanded="false" aria-controls="collapseThreeOne">
          How do we measure ODP implementation code coverage?
      </a>
    </h4>
  </div>
  <div id="collapseThreeOne" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingThreeOne">
    <div class="panel-body">
    <p id="P_252">
        OpenDataPlane testing information from GCOV (using <a href="http://ltp.sourceforge.net/coverage/lcov.php" id="A_253">LCOV</a> extension). Includes performance results from <a href="https://gcc.gnu.org/onlinedocs/gcc/Gcov-Intro.html#Gcov-Intro" id="A_254">gcov</a> using code test suites.
    </p>
    <ul id="UL_255">
        <li id="LI_256">
            how often each line of code executes
        </li>
        <li id="LI_257">
            what lines of code are actually executed
        </li>
        <li id="LI_258">
            how much computing time each section of code uses
        </li>
    </ul>
    <h3 id="H3_259">
                    How to replicate:
                </h3>
    <pre id="PRE_260">./bootstrap
./configure --enable-cunit
make check CFLAGS="-fprofile-arcs -ftest-coverage"
lcov -c -d ${TOPDIR}/odp/platform/${PLATFORM} --output-file ${TOPDIR}/${PLATFORM}-coverage.info
genhtml ${TOPDIR}/${PLATFORM}-coverage.info --output-directory ${TOPDIR}/${PLATFORM}-gcov-html
                </pre>
    </div>
  </div>
</div>

</div>



<h4>Upstream</h4>

<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
<div class="panel panel-default">
  <div class="panel-heading" role="tab" id="headingFourOne">
    <h4 class="panel-title">
      <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFourOne" aria-expanded="false" aria-controls="collapseFourOne">
          How do I send a patch to ODP?
      </a>
    </h4>
  </div>
  <div id="collapseFourOne" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFourOne">
    <div class="panel-body">
    <p id="P_272">
        Read the odp/CONTRIBUTING file as a starting point, and then google for the many write ups about contributing to the linux kernel, ODP attempts to follow that kernel style as closely as reasonable.
    </p>
    <p id="P_273">
        This write up may be usefull: <a href="http://www.tuxradar.com/content/newbies-guide-hacking-linux-kernel" id="A_274">http://www.tuxradar.com/content/newbies-guide-hacking-linux-kernel</a>
    </p>
    <p id="P_275">
        To check your patches will not be immediately rejected see the FAQ “How do I check my local patches are ready to be submitted “
    </p>
    <p id="P_276">
        And dont forget you can ask on the mailing list lng-odp@lists.linaro.org
    </p>
    </div>
  </div>
</div>

<div class="panel panel-default">
  <div class="panel-heading" role="tab" id="headingFourTwo">
    <h4 class="panel-title">
      <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFourTwo" aria-expanded="false" aria-controls="collapseFourTwo">
          How do I check my local patches are ready to be submitted?
      </a>
    </h4>
  </div>
  <div id="collapseFourTwo" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFourTwo">
    <div class="panel-body">
    <p id="P_282">
        You can re-use the CI scripts that run all ODP [regression testing] -&gt; http://opendataplane.org///testing/
        <br id="BR_283" /> Assuming that you have your odp repo at ~/git/odp and it contains your committed changes that you then created patches for with git format-patch
    </p>
    <pre id="PRE_284"><code id="CODE_285">
git clone http://git.linaro.org/lng/check-odp.git
cd check-odp/
#point at the repo to test, not you can also specify a branch, see the help
PATCH_DIR=~/git/odp ./apply-and-build.sh
</code>
                    </pre>
    <p id="P_286">
        You can get information on many more checks via:
    </p>
    <pre id="PRE_287"><code id="CODE_288">
./apply-and-build.sh -h
</code>
                        </pre>
    <p id="P_289">
        At the time of writing:
    </p>
    <pre id="PRE_290"><code id="CODE_291">
./apply-and-build.sh makes use of the following environment variables,
GIT_ODP:	which ODP git repo to use, default: git://git.linaro.org/lng/odp.git
GIT_BRANCH:	which branch to checkout and test, default: master
PATCH_DIR:	where to look for patches, default: /home/mike/incoming
CLEANUP:	set to 0 to save *.log files, default: 1
CHECKPATCH:	set to 0 to disable checkpatch test, default: 1
CHECKFORMAT:	set to 0 to not verify that patch is ASCII-encoded, default: 1
ENABLE_CUNIT:	set to 0 to disable cunit test, default: 1
PLATFORM:	set platform, default: linux-generic
ENABLE_DRYRUN:	set to 1 to enable a dryrun, default: 0
ENABLE_NETMAP:	set to 1 to enable netmap build, default: 0
NUM_CPUS:	add parallel make, default: _NPROCESSORS_ONLN
FILE_EXT:	supported extensions in patch file names, default: mbox patch
M32_ON_64:	enable 32 bit builds on a 64 bit host, default: 0
CPP_TEST:	enable cpp test, default: 0
TOOLCHAIN_RELEASE: set toolchain release, default: 14.09
Only used when ARCH is given!
Linaros toolchain releases are located here:
http://releases.linaro.org/14.09/components/toolchain/binaries/
CUNIT_VERSION:	 Change version from sourceforge.net, default: 2.1-3
</code>
</pre>
    </div>
  </div>
</div>

<div class="panel panel-default">
  <div class="panel-heading" role="tab" id="headingFourThree">
    <h4 class="panel-title">
      <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFourThree" aria-expanded="false" aria-controls="collapseFourThree">
          How do I check my local commits build across ODP platforms?
      </a>
    </h4>
  </div>
  <div id="collapseFourThree" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFourThree">
    <div class="panel-body">
    <p id="P_297">
        You can re-use the CI scripts that run all ODP [regression testing] -&gt; <a href="http://opendataplane.org///testing/" id="A_298">http://opendataplane.org///testing/</a>
        <br id="BR_299" /> Assuming that you have your odp repo at ~/git/odp and it contains your committed changes.
    </p>
    <pre id="PRE_300"><code id="CODE_301">git clone http://git.linaro.org/lng/check-odp.git
cd check-odp/
#point at the repo to test, not you can also specify a branch, see the help
GIT_ODP=~/git/odp ./build.sh</code>
                                </pre>
    <p id="P_302">
        You can get information on many more checks via:
    </p>
    <pre id="PRE_303"><code id="CODE_304">./build.sh -h</code>
                                    </pre>
    <p id="P_305">
        At the time of writing:
    </p>
    <pre id="PRE_306"><code id="CODE_307">ARCH:		 which arch to build (arm, armeb, arm64, arm64be), default: not set
GIT_ODP:	 which ODP git repo to use, default: git://git.linaro.org/lng/odp.git
GIT_BRANCH:	 which branch to checkout and test, default: master
TOOLCHAIN_RELEASE: set toolchain release, default: 14.09
Only used when ARCH is given!
Linaros toolchain releases are located here:
http://releases.linaro.org/14.09/components/toolchain/binaries/
CUNIT_VERSION:	 Change version from sourceforge.net, default: 2.1-3
OPENSSL_BUILD:	 build custom openssl, default: 0
OPENSSL_GIT:	 git url to OpenSSL, default git://git.openssl.org/openssl.git
OPENSSL_BRANCH:	 git branch to OpenSSL, default OpenSSL_1_0_1h
COV_DIR:	 path to coverty, default: not set
LCOV:		 to genrate lcov set LCOV=1, default: 0
TEST_LIST:	 Overides the test list for 'make check' TEST_LIST=""
NUM_CPUS:	 add parallel make, default: _NPROCESSORS_ONLN
CLEANUP:	 to save workspace set CLEANUP=0, default: 1
M32_ON_64:	 enable 32 bit builds on a 64 bit host, default: 0
DOXYGEN_HTML:	 build doxygen-html, default: 0
CLANG:		 build with clang, default: 0
EXIT_ON_ERROR:	 bail out on error, default: 1
CPP_TEST:	 enable cpp test, default: 0</code>
                                        </pre>
    </div>
  </div>
</div>

<div class="panel panel-default">
  <div class="panel-heading" role="tab" id="headingFourFour">
    <h4 class="panel-title">
      <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFourFour" aria-expanded="false" aria-controls="collapseFourFour">
          With apply-and-build I get “ERROR: Does not appear to be a unified-diff format patch”
      </a>
    </h4>
  </div>
  <div id="collapseFourFour" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFourFour">
    <div class="panel-body">
    <p id="P_313">
        This is often OK, check to see if you created a cover letter with git format-patch in the PATCH_DIR you specified, the cover letter is not a patch. In this case you will probably see something like
    </p>
    <pre id="PRE_314"><code id="CODE_315">
Using patch: 0000-cover-letter.patch
Trying to apply patch
Patch applied
ERROR: Does not appear to be a unified-diff format patch

total: 1 errors, 0 warnings, 0 checks, 0 lines checked

NOTE: Ignored message types: DEPRECATED_VARIABLE NEW_TYPEDEFS

/home/mike/git/odp/0000-cover-letter.patch has style problems, please review.</code>
                                            </pre>
    </div>
  </div>
</div>

<div class="panel panel-default">
  <div class="panel-heading" role="tab" id="headingFourFive">
    <h4 class="panel-title">
      <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFourFive" aria-expanded="false" aria-controls="collapseFourFive">
          With apply-and-build I get “rm: cannot remove … Permission denied”
      </a>
    </h4>
  </div>
  <div id="collapseFourFive" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFourFive">
    <div class="panel-body">
    <p id="P_321">
        There may be many lines indicating a problem deleting files that fit this pattern:
    </p>
    <pre id="PRE_322"><code id="CODE_323">‘./check-odp/build/odp-apply/opendataplane-/’: Permission denied”
</code>
                                                </pre>
    <p id="P_324">
    </p>
    <p id="P_325">
        This occurs is the distcheck part of the regression testing was interrupted and you no longer have permission to clean up the files.
        <br id="BR_326" /> As root you need to delete the //check-odp/build directory.
    </p>
    </div>
  </div>
</div>

<div class="panel panel-default">
  <div class="panel-heading" role="tab" id="headingFourSix">
    <h4 class="panel-title">
      <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFourSix" aria-expanded="false" aria-controls="collapseFourSix">
          Checkpatch has a warning I don’t agree with...
      </a>
    </h4>
  </div>
  <div id="collapseFourSix" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFourSix">
    <div class="panel-body">
    <p id="P_332">
        A checkpatch warning unlike a checkpatch error may be accepted if it can be shown that overall the code would be better by ignoring it.
    </p>
    <p id="P_333">
        A common case is the line length warning in conjunction with printing debug output and a reviewer will ask why the patch was sent containing warnings.
    </p>
    <p id="P_334">
        <strong id="STRONG_335">To possibly save a round of questions, send a note in a cover letter explaining why you think the explanation should be ignored.</strong>
    </p>
    </div>
  </div>
</div>
</div>

<h4>Miscellaneous</h4>


<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
<div class="panel panel-default">
  <div class="panel-heading" role="tab" id="headingFiveOne">
    <h4 class="panel-title">
      <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFiveOne" aria-expanded="false" aria-controls="collapseFiveOne">
          How do I build a standalone app against ODP?
      </a>
    </h4>
  </div>
  <div id="collapseFiveOne" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFiveOne">
    <div class="panel-body">
    <p id="P_347">
        Specifics on a Makefile might be better answered on a forum like stack overflow, but more specifically for ODP you need to do the same things you would for any library starting with installing it, something like this:
    </p>
    <p id="P_348">
        1.) Install locally in your own dir rather than as root in the system
    </p>
    <p id="P_349">
        2.) Move to the ODP root dir
    </p>
    <pre id="PRE_350"><code id="CODE_351">./configure --prefix=/home/&lt;your user&gt;/odp
make install</code>
                                                    </pre>
    <p id="P_352">
        That will provide the installed libraries and header files in the usual places in your home dir
    </p>
    <pre id="PRE_353">/home/&lt;your user&gt;/odp/bin
/home/&lt;your user&gt;/odp/include
/home/&lt;your user&gt;/odp/lib
/home/&lt;your user&gt;/odp/share
                                                        </pre>
    <p id="P_354">
        3.) Now just use -I and LDPATH to point to them as normal from a make file – see <a href="http://www.gnu.org/software/make/manual/make.html" id="A_355">http://www.gnu.org/software/make/manual/make.html</a> or Google gnu makefiles
    </p>
    <p id="P_356">
        But basically it will be like this in your shell
    </p>
    <pre id="PRE_357"><code id="CODE_358">export LD_LIBRARY_PATH=/home/&lt;your user&gt;/odp/lib</code>
                                                            </pre>
    <p id="P_359">
        4.) In your makefile
    </p>
    <pre id="PRE_360"><code id="CODE_361">CFLAGS=-I/home/&lt;your user&gt;/odp/include
LDFLAGS=-L/home/&lt;your user&gt;/odp/lib -lodp
CC=gcc
all: example</code>
                                                                </pre>
    <p id="P_362">
        example:
    </p>
    <pre id="PRE_363"><code id="CODE_364">$(CC) $(CFLAGS) example.c -o $@ $(LDFLAGS)</code>
                                                                    </pre>
    </div>
  </div>
</div>

<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
<div class="panel panel-default">
  <div class="panel-heading" role="tab" id="headingFiveTwo">
    <h4 class="panel-title">
      <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFiveTwo" aria-expanded="false" aria-controls="collapseFiveTwo">
          By going through the code I noticed that there are a *lot* of functions for atomics that do almost the same thing but not exactly?
      </a>
    </h4>
  </div>
  <div id="collapseFiveTwo" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFiveTwo">
    <div class="panel-body">
    <p>
        The differences are quite important here.
    </p>
    <p>
        The public odp/atomic.h uses a relaxed memory model so only suitable for things like statistics and shared sequence numbers etc. The internal atomics support supports a memory ordering parameter which make these functions usable for designing lock-less multithreaded data structures (and the implementation of the locks themselves). As it is not supposed that the user will design their own lock-less data structures, this API is internal to linux-generic (and thus may not exist on all platforms).
    </p>
    </div>
  </div>
</div>

</div>
