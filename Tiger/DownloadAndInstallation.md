::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![Stratego
logo](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)

------------------------------------------------------------------------

***Tiger in Stratego***

------------------------------------------------------------------------

**[WebHome](WebHome){.twikiLink}**\
[Tiger Compiler](TigerCompiler){.twikiLink}\
[Architecture](CompilerArchitecture){.twikiLink}\
[Packages](CompilerPackages){.twikiLink}\
[Components](CompilerComponent){.twikiLink}\
[Glossary](WebGlossary){.twikiLink}

[Download](DownloadAndInstallation){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Tiger/DownloadAndInstallation?t=1536825556)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/DownloadAndInstallation)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/DownloadAndInstallation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/DownloadAndInstallation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/DownloadAndInstallation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    20](http://www.program-transformation.org/view/Tiger/DownloadAndInstallation?rev=1.20)
    [(diff 19)](http://www.program-transformation.org/rdiff/Tiger/DownloadAndInstallation?rev1=1.20&rev2=1.19)
-   [Rev
    19](http://www.program-transformation.org/view/Tiger/DownloadAndInstallation?rev=1.19)
    [(diff 18)](http://www.program-transformation.org/rdiff/Tiger/DownloadAndInstallation?rev1=1.19&rev2=1.18)
-   [Rev
    18](http://www.program-transformation.org/view/Tiger/DownloadAndInstallation?rev=1.18)
    [(diff 17)](http://www.program-transformation.org/rdiff/Tiger/DownloadAndInstallation?rev1=1.18&rev2=1.17)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/DownloadAndInstallation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/DownloadAndInstallation?template=oopsmore&param1=1.20&param2=1.20)
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
    \...](http://www.program-transformation.org/oops/Tiger/DownloadAndInstallation?template=oopsmore&param1=1.20&param2=1.20)
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
Download And Installation {#download-and-installation .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

The distribution of the [Tiger in Stratego](WebHome){.twikiLink}
project.

::: {.twikiToc}
-   [Download](DownloadAndInstallation#Download)
-   [Requirements](DownloadAndInstallation#Requirements)
-   [Installation of Source
    Distribution](DownloadAndInstallation#Installation_of_Source_Distribut)
-   [Installation of Subversion
    Snapshots](DownloadAndInstallation#Installation_of_Subversion_Snaps)
:::

[]{#Download} Download
----------------------

Source (.tar.gz) and RPM distributions are available at:

-   <http://catamaran.labs.cs.uu.nl/dist/stratego/tiger-unstable-latest/>

The latest official release is 1.2, but using this version is strongly
discouraged (it is very old: Jan 2003. Please use the latest unstable
release in at the previous URL)

-   [tiger-1.2.tar.gz](ftp://ftp.stratego-language.org/pub/stratego/tiger/tiger-1.2.tar.gz)

Subversion repository

-   <https://svn.cs.uu.nl:12443/repos/StrategoXT/trunk/tiger/>

To checkout the latest sources:

    svn checkout https://svn.cs.uu.nl:12443/repos/StrategoXT/trunk/tiger/

[]{#Requirements} Requirements
------------------------------

To build and use the tiger package, a complete installation of
[StrategoXT](../Stratego/StrategoXT){.twikiLink}, SDF2, and the ATerm
library is needed. These dependencies can be obtained from the
[StrategoDownload](../Stratego/StrategoDownload){.twikiLink} page.

[]{#Installation_of_Source_Distribut} Installation of Source Distribution
-------------------------------------------------------------------------

The Tiger source distribution is a tar file compressed with gzip. The
source trees are configured using
[AutoMake[^?^](http://www.program-transformation.org/edit/Tools/AutoMake?topicparent=Tiger.DownloadAndInstallation)]{.twikiNewLink
style="background : #FFFFCE;"} and
[AutoConf[^?^](http://www.program-transformation.org/edit/Tools/AutoConf?topicparent=Tiger.DownloadAndInstallation)]{.twikiNewLink
style="background : #FFFFCE;"} and require GNU Make (gmake) for
building.

Installation of the tiger package involves the following steps:

    > gunzip tiger-1.2.tar.gz
    > tar xf tiger-1.2.tar
    > cd tiger-1.2
    > ./configure --prefix=/tmp/tiger --with-xt=/usr
    > gmake
    > gmake install

This assumes that [StrategoXT](../Stratego/StrategoXT){.twikiLink},
aterm, and sdf2 are installed in /usr.

[]{#Installation_of_Subversion_Snaps} Installation of Subversion Snapshots
--------------------------------------------------------------------------

To build and install the subversion snapshot, or a direct checkout of
the repository, it is necessary to create the makefiles and configure
script using the `bootstrap` script.

    > svn checkout <see above>
    > cd tiger
    > ./bootstrap
    > ./configure --prefix=/tmp/tiger --with-xt=/usr
    > gmake install

Note that it is necessary to `gmake install` instead of `gmake`, since
the subpackages depend on each other. This assumes that
[StrategoXT](../Stratego/StrategoXT){.twikiLink}, aterm, and sdf2 are
installed in /usr.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 24 Sep 2003\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
