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
    Page](http://www.program-transformation.org/edit/Tiger/HowToInstallTheTigerCompiler?t=1536826661)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/HowToInstallTheTigerCompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/HowToInstallTheTigerCompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/HowToInstallTheTigerCompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/HowToInstallTheTigerCompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Tiger/HowToInstallTheTigerCompiler?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tiger/HowToInstallTheTigerCompiler?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tiger/HowToInstallTheTigerCompiler?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tiger/HowToInstallTheTigerCompiler?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tiger/HowToInstallTheTigerCompiler?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tiger/HowToInstallTheTigerCompiler?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/HowToInstallTheTigerCompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/HowToInstallTheTigerCompiler?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Tiger/HowToInstallTheTigerCompiler?template=oopsmore&param1=1.4&param2=1.4)
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
How To Install The Tiger Compiler {#how-to-install-the-tiger-compiler .twikiTopicTitle}
=================================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

The [TigerCompiler](TigerCompiler){.twikiLink} consists of four
[CompilerPackages](CompilerPackages){.twikiLink}. Download each of these
packages.

**Installing Tools.XT**

To use the [TigerCompiler](TigerCompiler){.twikiLink} packages you need
an installation of XT-0.8. If you work at Utrecht University, you can
use the installation of Tools.XT in `/projects/stratego/xt`. If you work
at home you\'ll have to do the installation yourself.

Download version 0.8 from [XtDownload](../Tools/XtDownload){.twikiLink}.
Extend your `PATH` with the path to `XT-0.8/bin`.

    > gtar zxf XT-0.8.tar.gz
    > cd XT-0.8
    > ./configure --prefix=`pwd`
    > gmake
    > gmake install

**Installing the Packages**

Create a common directory for installing the compiler components,
suppose `$(tiger)` points to that directory. Then install configure and
build each package as follows:

    > gtar zxf package-version.tar.gz
    > cd package-version
    > ./configure --prefix=${tiger} --with-xt=${xt}
    > gmake
    > gmake install

Build the packages in the following order:

-   [TigerFront](TigerFront){.twikiLink}
-   [ASM](ASM){.twikiLink}
-   [TigerTrans](TigerTrans){.twikiLink}
-   [TigerOpt](TigerOpt){.twikiLink}
-   [TigerXmpl](TigerXmpl){.twikiLink}

See [HowToTestTheTigerCompiler](HowToTestTheTigerCompiler){.twikiLink}
for instructions on using the compiler components.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
