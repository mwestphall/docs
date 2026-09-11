title: OSG 26 News

OSG 26 News
===========

**Supported OS Versions:** EL8, EL9, EL10 (see [this document](supported_platforms.md) for details)

OSG 26 is the third release series following our [annual release schedule](release_series.md) and includes support for
EL10. The initial release includes GlideinWMS 3.11.4, HTCondor 26.0.1, HTCondor 26.1.0, HTCondor-CE 26.0.1, and XRootD 6.1.1.

OSG 26 will be supported for [approximately two years total](release_series.md#series-life-cycle).


!!! info "OSG 24 end-of-life"
    Following our [release series support policy](release_series.md#series-life-cycle),
    OSG 24 has reached its end-of-life and will no longer be supported with the release of OSG 26.

Enterprise Linux 10
-------------------

### Microarchitecture ###

The x86-64 architecture contains multiple subversions with different CPU feature sets, referred to as
[microarchitectures](https://en.wikipedia.org/wiki/X86-64#Microarchitecture_levels)
Support for x86-64-v2, released in 2008, [has been dropped from RHEL 10](https://access.redhat.com/solutions/7066628), 
Centos Stream 10, and Rocky Linux 10. Almalinux 10 continues support for v2 and has dedicated
[Yum repositories](https://almalinux.org/blog/2025-06-26-epel-v2-now-covers-almalinux-10-stable/) for these packages.

Before EL10, all OSG Software `x86_64` packages were built against the v2 microarchitecture.
Starting in EL10, OSG Software `x86_64` architecture packages are built against the v3 microarchitecture,
while a separate `x86_64_v2` architecture is maintained to support v2 Almalinux 10. 
`yum` will automatically select the correct `$basearch` for your host when 
[installing the OSG yum repos](../common/yum.md).

### EPEL ###

In EL10, the EPEL repositories have minor versions that correspond to your operating system's minor versions
(see [this presentation](https://archive.fosdem.org/2025/events/attachments/fosdem-2025-6844-the-road-to-epel-10/slides/238616/the-road-_Ny3Et4L.pdf) for details).
As a result, there are packages missing from EPEL 10.0 that are availabe in EPEL 10.1 or EPEL 10.2.
CentOS Stream 10 installations will point at the latest EPEL sub-version but other EL variants will need to upgrade OS
minor versions to access packages in newer EPEL sub-versions.

Note that at the time of this writing, Alma Linux, RHEL, and Rocky Linux have not released 10.1 or above.

Announcements
-------------

Updates to critical packages are also announced by email and are sent to the following recipients and lists:

-   [Registered administrative contacts](../common/registration.md#registering-resources)
-   [site-announce@osg-htc.org](https://groups.google.com/u/1/a/osg-htc.org/g/site-announce)
-   [software-discuss@osg-htc.org](https://groups.google.com/a/osg-htc.org/g/software-discuss)

Latest News
-----------

**TODO:** Initial Release
-------------------------------------

This initial release contains the following notable changes compared to the current OSG 25 release in [main](../common/yum.md):

# TODO
