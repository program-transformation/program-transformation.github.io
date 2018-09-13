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
    Page](http://www.program-transformation.org/edit/Tools/KoalaTools?t=1536826791)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/KoalaTools)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/KoalaTools)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/KoalaTools?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/KoalaTools?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/Tools/KoalaTools?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Tools/KoalaTools?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Tools/KoalaTools?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Tools/KoalaTools?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Tools/KoalaTools?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Tools/KoalaTools?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/KoalaTools)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/KoalaTools?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/Tools/KoalaTools?template=oopsmore&param1=1.8&param2=1.8)
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
Koala Tools {#koala-tools .twikiTopicTitle}
===========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[]{#This_project_is_obolete_please_c} This project is obolete, please checkout: [KoalaCompiler](KoalaCompiler){.twikiLink}
--------------------------------------------------------------------------------------------------------------------------

+-----------------------------------+-----------------------------------+
| **Description**                   | [![](../pub/Tools/KoalaTools/koal |
|                                   | a-composition-small.gif)](../pub/ |
| The Koala-tools package is a      | Tools/KoalaTools/koala-compositio |
| collection of tools operating on  | n.gif)                            |
| the Koala component definition    |                                   |
| language as developed by Philips  |                                   |
| Research.                         |                                   |
|                                   |                                   |
| Koala is a component definition   |                                   |
| language used by Philips consumer |                                   |
| electroniccs to model components  |                                   |
| (as C modules), composition (as C |                                   |
| compilation and linking), and     |                                   |
| variability (as CPP macros and    |                                   |
| partial evaluation).              |                                   |
|                                   |                                   |
| The Koala component model         |                                   |
| consists of a component language, |                                   |
| which supports definition of:     |                                   |
|                                   |                                   |
| -   interfaces (both required and |                                   |
|     provided)                     |                                   |
| -   data types                    |                                   |
| -   components                    |                                   |
| -   diversity (by means of a      |                                   |
|     diversity interfaces)         |                                   |
| -   component compositions        |                                   |
|                                   |                                   |
| Component compositions consist of |                                   |
| collections of components and     |                                   |
| wires that connect provides and   |                                   |
| requires interfaces (see picture  |                                   |
| below).                           |                                   |
|                                   |                                   |
| **Contents**                      |                                   |
|                                   |                                   |
| The koala-tools package includes: |                                   |
|                                   |                                   |
| -   The Koala language definition |                                   |
|     in SDF                        |                                   |
| -   A Koala component flattener   |                                   |
|     (`pack-koala`)                |                                   |
| -   An automatic wiring tool      |                                   |
|     (`koala-wire`)                |                                   |
| -   A Koala composition           |                                   |
|     visualizer (`koala-graph`)    |                                   |
| -   A Koala analyzer              |                                   |
|     (`koala-analyze`)             |                                   |
| -   A generic [koala              |                                   |
|     compiler](KoalaToolsCompiler) |                                   |
| {.twikiLink}                      |                                   |
|     toolkit (`koala-compiler`)    |                                   |
| -   A [Composition                |                                   |
|     tool](KoalaToolsCompiler){.tw |                                   |
| ikiLink}                          |                                   |
|     for [Source Tree              |                                   |
|     Composition](http://www.cs.uu |                                   |
| .nl/groups/ST/Merijn/PaperSourceT |                                   |
| reeComposition)                   |                                   |
|     (`koala-tred`,                |                                   |
|     `koala-buildorder` +          |                                   |
|     `koala-build-composer` +      |                                   |
|     `koala-tree-composer`)        |                                   |
|                                   |                                   |
| **Contact**                       |                                   |
|                                   |                                   |
| -   [Rob van                      |                                   |
|     Ommering](../Main/RobVanOmmer |                                   |
| ing){.twikiLink}                  |                                   |
|     about mainstream Koala        |                                   |
|     development                   |                                   |
| -   [Merijn de                    |                                   |
|     Jonge](http://www.cs.uu.nl/~m |                                   |
| dejonge)                          |                                   |
|     About koala-tools package     |                                   |
|                                   |                                   |
| **Documentation**                 |                                   |
|                                   |                                   |
| Official publications about Koala |                                   |
| include:                          |                                   |
|                                   |                                   |
| -   [Rob van                      |                                   |
|     Ommering](../Main/RobVanOmmer |                                   |
| ing){.twikiLink}                  |                                   |
|     and Frank van der Linden and  |                                   |
|     Jeff Kramer and Jeff Magee.   |                                   |
|     ***The Koala Component Model  |                                   |
|     for Consumer Electronics***.  |                                   |
|     *IEEE Software Computer*,     |                                   |
|     33(3), pp. 78-85, March 2000. |                                   |
|                                   |                                   |
| Below are some slides about       |                                   |
| Koala-tools:                      |                                   |
|                                   |                                   |
| -   <http://www.cs.uu.nl/groups/S |                                   |
| T/Merijn/SlidesKoalaToolDevelopme |                                   |
| nt>                               |                                   |
| -   <http://www.cs.uu.nl/groups/S |                                   |
| T/Merijn/SlidesLanguageCenteredSo |                                   |
| ftwareEngineering>                |                                   |
+-----------------------------------+-----------------------------------+

**Availability**

The koala-tools package is distributed under the GNU Lesser General
Public License It is available in source from:

-   <http://www.cs.uu.nl/~mdejonge/downloads/koala-tools-0.2.tar.gz>\
    This is the source distribution of the koala-tools package.
-   <http://www.cs.uu.nl/~mdejonge/downloads/koala-demo-0.2.tar.gz>\
    This package demonstrates [Source Tree
    Composition](http://www.cs.uu.nl/groups/ST/Merijn/PaperSourceTreeComposition)
    with Koala (see [KoalaCompiler](KoalaCompiler){.twikiLink}). It
    demonstrates building the koala-tools package as a Koala
    composition.

**Dependencies**

The koala-tools package has the following dependencies:

-   [StrategoXT](../Stratego/StrategoDownload){.twikiLink}
-   [GraphViz](GraphViz){.twikiLink}

These packages need to be installed before building koala-tools

**Installation**

        tar zxvf koala-tools-0.2.tar.gz
        tar zxvf koala-demo-0.2.tar.g
        cd koala-tools-0.2
        ./configure --with-xt=<location of stratgoxt> --prefix=<installation prefix>
        make
        make install

        cd ../koala-demo-0.2
        ./configure
        make

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 17 Feb 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
