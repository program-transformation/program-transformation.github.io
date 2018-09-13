::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
[Home](WebHome){.twikiLink}

**XT Tools**

-   [Reference Docs](ToolReference){.twikiLink}
-   [GPP](GenericPrettyPrinter){.twikiLink}
-   [ATerm](ATermTools){.twikiLink}
-   [SDF](SdfTools){.twikiLink}
-   [AsFix](AsFixTools){.twikiLink}

**Languages**

-   [Stratego](../Stratego/WebHome){.twikiLink}
-   [SDF](../Sdf/WebHome){.twikiLink}
-   [ATerm](ATermFormat){.twikiLink}

**Software**

-   [Stratego/XT](../Stratego/StrategoDownload){.twikiLink}
-   [SDF2 Bundle](../Sdf/SdfBundle){.twikiLink}
-   [KoalaCompiler](KoalaCompiler){.twikiLink}
-   [AutoBundle](AutoBundle){.twikiLink}
-   [AutoBuild](AutoBuild){.twikiLink}
-   [DailyBuildSystem](DailyBuildSystem){.twikiLink}

[![](http://www.program-transformation.org/twiki/pub/rss.gif "RSS 1.0 feed")](http://www.program-transformation.org/twiki/bin/view/Tools/WebRss?skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Tools/AutoBuild?t=1536825758)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/AutoBuild)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/AutoBuild)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/AutoBuild?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/AutoBuild?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    18](http://www.program-transformation.org/view/Tools/AutoBuild?rev=1.18)
    [(diff 17)](http://www.program-transformation.org/rdiff/Tools/AutoBuild?rev1=1.18&rev2=1.17)
-   [Rev
    17](http://www.program-transformation.org/view/Tools/AutoBuild?rev=1.17)
    [(diff 16)](http://www.program-transformation.org/rdiff/Tools/AutoBuild?rev1=1.17&rev2=1.16)
-   [Rev
    16](http://www.program-transformation.org/view/Tools/AutoBuild?rev=1.16)
    [(diff 15)](http://www.program-transformation.org/rdiff/Tools/AutoBuild?rev1=1.16&rev2=1.15)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/AutoBuild)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/AutoBuild?template=oopsmore&param1=1.18&param2=1.18)
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
    \...](http://www.program-transformation.org/oops/Tools/AutoBuild?template=oopsmore&param1=1.18&param2=1.18)
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
Auto Build {#auto-build .twikiTopicTitle}
==========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Description**

Compiling and installing software packages is often a time consuming and
complicated business. You have to read the installation instructions to
determine which steps are required for building and installing the
software, then you have to determine how to configure the system
(indicate where components such as libraries can be found and which
compile flags should be used). Finally, you have to execute configure,
compile, and install tasks manually. When you have to install the same
software on multiple architectures, you might come in the situation
where you have to perform these steps for each platform again. To make
things even worse, this process has to be repeated each time you want to
install a new version of the software package.

The \"autobuild\" software package tries to solve this problem by
introducing the notion of so called \"build files\" in which you can
define how a particular software system should be built on different
platforms. The \"build\" tool reads a build file, and builds the
software package for you on each platform you defined. It can perform
the build processes on multiple platforms in parallel, and it creates
informative [HTML](../Transform/HTML){.twikiLink} and textual log files.

Two typical applications of autobuild are:

1.  Centralized management of software packages for multiple
    architectures. For instance, part of the software installed at the
    Transform.SEN1 research group of the
    [CWI](../Transform/CWI){.twikiLink} is controlled by build files.
    Once a new version of a package needs to be installed (or an
    installation needs to be performed again), a single call to build
    suffices. All build files are under
    [CVS](../Transform/CVS){.twikiLink} control to keep track of changes
    made to the files over time.
2.  [Daily builds](DailyBuildSystem){.twikiLink} where the build tool is
    used to compile software under development on a daily basis. The
    generated [HTML](../Transform/HTML){.twikiLink} documentation gives
    access to the build log and helps locating errors in the daily
    build. (See [DailyBuildSystem](DailyBuildSystem){.twikiLink}).

**Getting the Software**

The autobuild package is open source and distributed as a gzipped tar
file named \`autobuild-\<version\>.tar.gz\', where \<version\> denotes
the version of the package. You can download the package at:

-   <http://www.cs.uu.nl/~mdejonge/downloads/autobuild-0.5.tar.gz>

------------------------------------------------------------------------

**Questions**

-   Is it possible to have localhost as a platform? How do I indicate
    that in the platforms file?

You can simply add an antry like \' `myplatform="localhost"` \' in your
platforms file.

-   The README file has information about setting up the
    [BuildFile[^?^](http://www.program-transformation.org/edit/Tools/BuildFile?topicparent=Tools.AutoBuild)]{.twikiNewLink
    style="background : #FFFFCE;"} for one package, but does not explain
    how to set up a complete dailybuild environment. Would it be
    possible to provide a package with a template or a sample set-up?

[AutoBuild](AutoBuild){.twikiLink} is not a daily-build system by
itself. Checkout [DailyBuildSystem](DailyBuildSystem){.twikiLink} for
setting up a daily-build system with the dbs package.

At this moment you cannot use a template set-up. You can however use the
\'-g\' switch to generate an initial Buildfile for a package and use
[AutoBuild](AutoBuild){.twikiLink}\'s \`include\' mechanism to import
standard (shared) build configuration. See the Buildfiles at
<http://www.cwi.nl/~daybuild/> for examples.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
