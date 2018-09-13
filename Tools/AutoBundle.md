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
    Page](http://www.program-transformation.org/edit/Tools/AutoBundle?t=1536825470)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/AutoBundle)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/AutoBundle)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/AutoBundle?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/AutoBundle?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    29](http://www.program-transformation.org/view/Tools/AutoBundle?rev=1.29)
    [(diff 28)](http://www.program-transformation.org/rdiff/Tools/AutoBundle?rev1=1.29&rev2=1.28)
-   [Rev
    28](http://www.program-transformation.org/view/Tools/AutoBundle?rev=1.28)
    [(diff 27)](http://www.program-transformation.org/rdiff/Tools/AutoBundle?rev1=1.28&rev2=1.27)
-   [Rev
    27](http://www.program-transformation.org/view/Tools/AutoBundle?rev=1.27)
    [(diff 26)](http://www.program-transformation.org/rdiff/Tools/AutoBundle?rev1=1.27&rev2=1.26)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/AutoBundle)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/AutoBundle?template=oopsmore&param1=1.29&param2=1.29)
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
    \...](http://www.program-transformation.org/oops/Tools/AutoBundle?template=oopsmore&param1=1.29&param2=1.29)
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
Auto Bundle {#auto-bundle .twikiTopicTitle}
===========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Description**

Autobundle is a utility for making software distributions by bundling
multiple (third-party) software packages. Autobundle promotes the
development of reusable components which can be distributed separately,
or as part of larger software systems. Autobundle thus allows you to
easily distribute your software as self-contained packages (by bundling
all required components). This greatly simplifies the installation
process of your software because a user does not need to obtain,
configure, and install these required software packages first.

Two typical applications of autobundle are:

1.  The distribution of the ASF+SDF Meta-Environment
    (www.cwi.nl/projects/MetaEnv), which bundles amongst others the
    [ToolBus[^?^](http://www.program-transformation.org/edit/Tools/ToolBus?topicparent=Tools.AutoBundle)]{.twikiNewLink
    style="background : #FFFFCE;"} software application architecture,
    the ATerms abstract data type and libraries, a parser, and a parser
    generator. All these components are also distributed and used
    separately.
2.  XT, which stands for \`Program Transformations Tools\'
    (www.program-transformation.org/xt). It bundles some of the
    components of the ASF+SDF Meta-Environment (the ATerms abstract data
    type, the parser, and parser generator), but in addition the
    programming language Stratego (www.stratego-language.org), a
    pretty-printer (www.cs.uu.nl/\~mdejonge/gpp),the grammar tools (GT)
    package (www.program-transformation.org/gt), and the grammar bases
    (GB) package (www.program-transformation.org/gb).

Autobundle allows you to easily define such distributions by listing the
components, together with a version number, and the location where the
components can be retrieved. A typical autobundle distribution is thus
simply a collection of components of a particular version.

The autobundle software helps creating an initial framework for the
package and creates the software bundle for you, by downloading the
different components and building a single distribution from them.
Autobundle requires that the components are constructed using
[AutoConf[^?^](http://www.program-transformation.org/edit/Tools/AutoConf?topicparent=Tools.AutoBundle)]{.twikiNewLink
style="background : #FFFFCE;"} and
[AutoMake[^?^](http://www.program-transformation.org/edit/Tools/AutoMake?topicparent=Tools.AutoBundle)]{.twikiNewLink
style="background : #FFFFCE;"}. The use of
[AutoConf[^?^](http://www.program-transformation.org/edit/Tools/AutoConf?topicparent=Tools.AutoBundle)]{.twikiNewLink
style="background : #FFFFCE;"} and
[AutoMake[^?^](http://www.program-transformation.org/edit/Tools/AutoMake?topicparent=Tools.AutoBundle)]{.twikiNewLink
style="background : #FFFFCE;"} is clearly described in the documentation
of both packages and not addressed here.

Available packages are stored in the [Online Package
Base](http://www.program-transformation.org/package-base), from where
you can obtain generated software bundles by making specific packages
selections.

**Publications**

-   [Source Tree
    Composition](http://www.cs.uu.nl/groups/ST/Merijn/PaperSourceTreeComposition)

<!-- -->

-   [Package-Based Software
    Development](http://www.cs.uu.nl/groups/ST/Merijn/PaperPackageBasedSoftwareDevelopment)

<!-- -->

-   [Feature-Based Product Line Instantiation using Source-Level
    Packages](http://www.cs.uu.nl/groups/ST/Merijn/PaperFeatureBasedProductLineInstantiation)

<!-- -->

-   [The Linux Kernel as Flexible Product-Line
    Architecture](http://www.cs.uu.nl/groups/ST/Merijn/PaperTheLinuxKernelAsFlexibleProductLineArchitecture)

**Getting the software**

The autobundle package is open source and the most recent release can be
obtained from:

-   <http://nix.cs.uu.nl/dist/stratego/autobundle-0.14/>

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
