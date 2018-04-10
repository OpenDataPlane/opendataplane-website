---
title: Mailing List
layout: container-breadcrumb
permalink: /mailing-list/
---
### ODP-API and the linux-generic model implementation

Functional API test implementation that requires only a recent Linux kernel. This implementation can form the starting point for a new platform specific high performance implementation, providing hardware acceleration and/or optimized libraries.

### ODP-DPDK

An example of a specific platform implementation intended for high performance of ODP, in this case ODP in implemented using the DPDK libraries and targets X86 processor optimizations.

### ODP-OVS

Discussions on adding hardware acceleration to the popular openVSwitch application using the ODP framework.

### Validation tools

There is a comprehensive suite of validation scripts that build ODP or validate patches intended for ODP at [/lng/check-odp.git](https://git.linaro.org/lng/check-odp.git).

The apply-and-build.sh is particularly useful for testing a suite of patches before posting them for inclusion in ODPt. The help page for apply-and-build can be seen with “./apply-and-build.sh –help” but generally you need just the PATCH_DIR setting to point at the patches to be tested.

#### Check-ODP

This mailing list is used for issues and announcements for the check-odp tool kit used for testing ODP repositories locally before submitting patches. Also by the CI builds for the ODP master and api-next branches.
