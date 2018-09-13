::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
  ----------------------------------------------------------------------------------
  [![](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)](WebHome)
  ----------------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

-   [Documentation](StrategoDocumentation){.twikiLink}
-   [Language](StrategoLanguage){.twikiLink}
-   [Research Papers](StrategoPublications){.twikiLink}
-   [Applications](StrategoApplication){.twikiLink}

**[Download](StrategoDownload){.twikiLink}**

-   [Continuous build](ContinuousBuild){.twikiLink}
-   [Extensions](AdditionalPackageDownload){.twikiLink}

**[Support](StrategoSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Users Days](StrategoUsersDay){.twikiLink}
-   [Bug Reports](http://yellowgrass.org/project/StrategoXT)

**[Developers](StrategoDev){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/StrategoXT/strategoxt/trunk)
-   [Buildfarm
    results](http://hydra.nixos.org/jobset/strategoxt/strategoxt-release/all)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Stratego/StrategoDownload?t=1536825358)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoDownload)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoDownload)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoDownload?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoDownload?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    47](http://www.program-transformation.org/view/Stratego/StrategoDownload?rev=1.47)
    [(diff 46)](http://www.program-transformation.org/rdiff/Stratego/StrategoDownload?rev1=1.47&rev2=1.46)
-   [Rev
    46](http://www.program-transformation.org/view/Stratego/StrategoDownload?rev=1.46)
    [(diff 45)](http://www.program-transformation.org/rdiff/Stratego/StrategoDownload?rev1=1.46&rev2=1.45)
-   [Rev
    45](http://www.program-transformation.org/view/Stratego/StrategoDownload?rev=1.45)
    [(diff 44)](http://www.program-transformation.org/rdiff/Stratego/StrategoDownload?rev1=1.45&rev2=1.44)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoDownload)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoDownload?template=oopsmore&param1=1.47&param2=1.47)
:::
:::

::: {.flexMenu onmouseover="return showMenu(event, 102);" onmouseout="return hideMenu(event, 102);"}
Web

::: {#flexMenuContent102 .flexMenuContent}
-   [Recent Changes](WebChanges){.twikiLink}
-   [Notify Service](WebNotify){.twikiLink}
-   [News](WebNews){.twikiLink}

<!-- -->

-   [Page Index](WebIndex){.twikiLink}
-   [Search](WebSearch){.twikiLink}

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoDownload?template=oopsmore&param1=1.47&param2=1.47)
:::
:::

::: {.flexMenu onmouseover="return showMenu(event, 103);" onmouseout="return hideMenu(event, 103);"}
Wiki

::: {#flexMenuContent103 .flexMenuContent}
-   [About
    TWiki](http://www.program-transformation.org/view/TWiki/WebHome)
-   [Text
    Formatting](http://www.program-transformation.org/view/TWiki/TextFormattingRules)

<!-- -->

-   [Registration](http://www.program-transformation.org/view/TWiki/TWikiRegistration)
-   [Change
    Password](http://www.program-transformation.org/view/TWiki/ChangePassword)
-   [Reset
    Password](http://www.program-transformation.org/view/TWiki/ResetPassword)

<!-- -->

-   [Users](http://www.program-transformation.org/view/Main/TWikiUsers)
-   [Groups](http://www.program-transformation.org/view/Main/TWikiGroups)
:::
:::
:::
:::

::: {.twikiTopic}
Download Stratego/XT {#download-strategoxt .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

------------------------------------------------------------------------

[Note that Stratego is now part of the [Spoofax Language
Workbench](http://metaborg.org/spoofax), which provides an Eclipse
plugin for developing SDF and Stratego, and creating Eclipse IDE plugins
for your own language. See the Spoofax website for information and
downloads: <http://metaborg.org>. This website is still available for
historical purposes. Refer the new site for up-to-date documentation.
]{style="color:red;font-size:24px"}

------------------------------------------------------------------------

\-- [EelcoVisser](EelcoVisser){.twikiLink}, 23 November 2011

------------------------------------------------------------------------

Stratego/XT is available in several ways:

-   *Users* of Stratego/XT or packages based on Stratego/XT typically
    just want to download the latest release.
-   *Developers* of software based on Stratego/XT might want to use the
    latest [continuous build](ContinuousBuild){.twikiLink}.
-   *Stratego/XT developers*, working on Stratego/XT itself, need to
    checkout the latest sources.

The integration builds are currently most up-to-date and are advised for
end-users and developers. Using the [Nix](http://nixos.org) package
management system provides the easiest way to easily install the latest
binary releases.

To get the latest stable release of Stratego/XT using nix, perform the
following steps:

    $ nix-channel --add  http://nixos.org/releases/nixpkgs/channels/nixpkgs-unstable
    $ nix-channel --update
    $ nix-env -i aterm-2.5 sdf2-bundle strategoxt-0.17

[]{#Latest_stable_release_StrategoRe} Latest stable release \-- [StrategoXT 0.17](StrategoRelease017){.twikiLink}
-----------------------------------------------------------------------------------------------------------------

The latest stable release of Stratego/XT is 0.17. For more information
go [here](StrategoRelease017){.twikiLink}.

See the [installation
instructions](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/installation.html)
if you are not familiar with the standard installation procedure of
tarballs or RPMs.

![](http://buildfarm.info/images/src-pkg.png) Source tar.gz

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/aterm-2.5.tar.gz)
    (use [this
    patch](https://svn.nixos.org/repos/nix/nixpkgs/trunk/pkgs/development/libraries/aterm/max-long.patch))
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/sdf2-bundle-2.4.tar.gz)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/strategoxt-0.17.tar.gz)

![](http://buildfarm.info/images/suse.png) SuSE Linux RPM

SuSE 11.0:

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/opensuse103i386/aterm-2.5-1.i586.rpm)
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/opensuse103i386/sdf2-bundle-2.4-1.i586.rpm)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/opensuse103i386/strategoxt-0.17-1.i586.rpm)

SuSE 10.3:

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/opensuse110i386/aterm-2.5-1.i586.rpm)
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/opensuse110i386/sdf2-bundle-2.4-1.i586.rpm)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/opensuse110i386/strategoxt-0.17-1.i586.rpm)

![](http://buildfarm.info/images/fedora.png)Fedora Core RPM

Fedora Core 11:

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora11i386/aterm-2.5-1.i386.rpm)
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora11i386/sdf2-bundle-2.4-1.i386.rpm)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora11i386/strategoxt-0.17-1.i386.rpm)

Fedora Core 10:

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora10i386/aterm-2.5-1.i386.rpm)
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora10i386/sdf2-bundle-2.4-1.i386.rpm)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora10i386/strategoxt-0.17-1.i386.rpm)

Fedora Core 9:

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora9i386/aterm-2.5-1.i386.rpm)
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora9i386/sdf2-bundle-2.4-1.i386.rpm)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora9i386/strategoxt-0.17-1.i386.rpm)

Fedora Core 5:

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora5i386/aterm-2.5-1.i386.rpm)
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora5i386/sdf2-bundle-2.4-1.i386.rpm)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/fedora5i386/strategoxt-0.17-1.i386.rpm)

![](http://buildfarm.info/images/debian.png)Debian DEB

Debian 5.0:

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/debian50i386/aterm_2.5-1_i386.deb)
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/debian50i386/sdf2-bundle_2.4-1_i386.deb)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/debian50i386/strategoxt_0.17-1_i386.deb)

Debian 4.0:

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/debian40i386/aterm_2.5-1_i386.deb)
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/debian40i386/sdf2-bundle_2.4-1_i386.deb)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/debian40i386/strategoxt_0.17-1_i386.deb)

![](http://buildfarm.info/images/debian.png)Ubuntu DEB

Ubuntu 9.04:

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu904i386/aterm_2.5-1_i386.deb)
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu904i386/sdf2-bundle_2.4-1_i386.deb)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu904i386/strategoxt_0.17-1_i386.deb)

Ubuntu 8.10:

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu810i386/aterm_2.5-1_i386.deb)
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu810i386/sdf2-bundle_2.4-1_i386.deb)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu810i386/strategoxt_0.17-1_i386.deb)

Ubuntu 8.04:

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu804i386/aterm_2.5-1_i386.deb)
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu804i386/sdf2-bundle_2.4-1_i386.deb)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/ubuntu804i386/strategoxt_0.17-1_i386.deb)

![](http://buildfarm.info/images/win32.png)
![](http://buildfarm.info/images/cygwin.gif) Microsoft Windows Cygwin
binaries

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/cygwin/aterm-2.5-cygwin.tar.gz)
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/cygwin/sdf2-bundle-2.4-cygwin.tar.gz)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/cygwin/strategoxt-0.17-cygwin.tar.gz)
-   [aterm-2.5 + sdf2-bundle-2.4 +
    strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/cygwin/strategoxt-superbundle-0.17-cygwin.tar.gz)

<!-- -->

-   The \*-cygwin.tar.gz files contain a file `README` with installation
    instructions.

![](http://buildfarm.info/images/macosx.gif) Mac OS X binaries

-   [aterm-2.5](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/macosx/aterm-2.5-macosx.tar.gz)
-   [sdf2-bundle-2.4](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/macosx/sdf2-bundle-2.4-macosx.tar.gz)
-   [strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/macosx/strategoxt-0.17-macosx.tar.gz)
-   [aterm-2.5 + sdf2-bundle-2.4 +
    strategoxt-0.17](ftp://ftp.strategoxt.org/pub/stratego/StrategoXT/strategoxt-0.17/macosx/strategoxt-superbundle-0.17-macosx.tar.gz)

<!-- -->

-   The \*-macosx.tar.gz files contain a file `README` with installation
    instructions.

![](http://buildfarm.info/images/package.png) Nix Package

One-click installation using [Nix](http://nixos.org), open with
`nix-install-package`

-   [aterm-2.5](http://hydra.nixos.org/job/nixpkgs/trunk/aterm25)
-   [sdf2-bundle-2.4](http://hydra.nixos.org/job/nixpkgs/trunk/strategoPackages.sdf)
-   [strategoxt-0.17](http://hydra.nixos.org/job/nixpkgs/trunk/strategoPackages.strategoxt)

[]{#Integration_Builds} Integration Builds
------------------------------------------

The Stratego/XT packages integration build provides a heavily tested
release of the latest version of Stratego/XT, its dependencies, and
packages based on Stratego/XT. The packages are guaranteed to work
together without any problems. The latest successful integration build
is available at:

-   <http://releases.strategoxt.org/strategoxt-packages/strategoxt-packages-stable/>

Installing more recent releases of individual packages (see [continuous
build](ContinuousBuild){.twikiLink}) might result in incompatible
combinations of packages, so this is discouraged.

### []{#How_to_install}[]{#How_to_install_} How to install?

**Nix Channel**. We advice to use the [Nix package
manager](http://nixos.org) for installing packages from our release
management system. To keep your installation up to date, we advice to
subscribe to the `strategoxt-packages` Nix channel, as explained on the
[release page of
strategoxt-packages](http://releases.strategoxt.org/strategoxt-packages/strategoxt-packages-stable/).

**Nix Package**. You can use the [Nix package manager](http://nixos.org)
to install packages (without subscribing to the `strategoxt-packages`
Nix channel) by clicking on the link for your platform of the package
that you want to install (see the table at the channel page). If your
browser asks what to do with this file, choose to open it using
`/nix/bin/nix-install-package`.

**Source**. The integration build provides links to the releases that
have been built and tested for this integration build. At the release
pages of the individual packages, you will find source distributions.

**RPM**. Many packages also provide RPMs. Similar to installation from
source, you can find RPMs at the release pages of the individual
packages.

**Binary Windows Archive**. Some packages provide support for native
Microsoft Windows. In this case the release page of the individual
package provides a link to a .zip file that you can extract to any
location in your file system. You don\'t need to install Cygwin.

#### []{#Detailed_instructions} Detailed instructions

See the [installation
instructions](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/installation.html)
if you are not familiar with the standard installation procedure of
source tarballs or RPMs.

[]{#Continuous_Builds} Continuous Builds
----------------------------------------

------------------------------------------------------------------------

[Note that Stratego is now part of the [Spoofax Language
Workbench](http://metaborg.org/spoofax), which provides an Eclipse
plugin for developing SDF and Stratego, and creating Eclipse IDE plugins
for your own language. See the Spoofax website for information and
downloads: <http://metaborg.org>. This website is still available for
historical purposes. Refer the new site for up-to-date documentation.
]{style="color:red;font-size:24px"}

------------------------------------------------------------------------

The [buildfarm](http://releases.strategoxt.org) continuously builds
Stratego/XT and related packages. The distributions contain the latest
of the latest developments. Although the distributions are thoroughly
tested by the buildfarm, such an installation is not guaranteed to be
stable.

Continuous builds are available at:

-   <http://hydra.nixos.org/job/strategoxt/strategoxt-packages/strategoxt>

To get strategoxt and the dependencies using nix, please use the
follwoing commands:

     nix-channel --add http://hydra.nixos.org/jobset/strategoxt/strategoxt-packages/channel/latest
     nix-channel --update
     nix-env -i aterm-2.5 sdf2-bundle strategoxt

[]{#Stratego_XT_extensions} Stratego/XT extensions
--------------------------------------------------

Not all Stratego related packages are in the Stratego/XT distribution.
[Stratego/XT Extensions](AdditionalPackageDownload){.twikiLink} points
you to releases, daily distributions, and the latest sources of these
packages.

[]{#Subversion} Subversion
--------------------------

The most recent sources can be obtained from Subversion. Please note
that doing this is useless if you don\'t actually want to modify the
sources. If you just want to have the latest developments as a user,
using an usstable distribution is the best way to get this hot stuff.

For instructions on how to obtain the latest sources please see the
[manual](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/contribute.html#svn-install).

[]{#Older_Releases} Older Releases
----------------------------------

Older releases of Stratego/XT and Stratego are still available:

-   [Stratego/XT 0.16](StrategoRelease016){.twikiLink}
    -   Warning: This release has known issues with recent GCC 4.x, GNU
        Make 3.81, Mac OS X, and operating systems that have a
        non-executable stack (e.g. some recent Linux distributions). If
        you experience these issues, then we currently advice to install
        the latest successful [integration
        build](IntegrationBuild){.twikiLink}.
-   [Stratego/XT 0.15](StrategoRelease015){.twikiLink}
-   [Stratego/XT 0.14](StrategoRelease014){.twikiLink}
-   [Stratego/XT 0.13](StrategoRelease013){.twikiLink}
-   [Stratego/XT 0.12](StrategoRelease012){.twikiLink}
-   [Stratego/XT 0.11](StrategoRelease011){.twikiLink}
-   [Stratego/XT 0.10](StrategoRelease010){.twikiLink}
-   [Stratego/XT 0.9.5](StrategoRelease095){.twikiLink}
-   [Stratego/XT 0.9.4](StrategoRelease094){.twikiLink}
-   [Stratego/XT 0.9.3](StrategoRelease093){.twikiLink}
-   [Stratego/XT 0.9.2](StrategoRelease092){.twikiLink}
-   [Stratego/XT 0.9.1](StrategoRelease091){.twikiLink}
-   [Stratego/XT 0.9](StrategoRelease09){.twikiLink}
-   [Stratego 0.8.1](StrategoDownload08){.twikiLink}
-   [Stratego download history](StrategoDownloadHistory){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
