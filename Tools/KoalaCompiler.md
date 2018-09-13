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
    Page](http://www.program-transformation.org/edit/Tools/KoalaCompiler?t=1536825465)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/KoalaCompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/KoalaCompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/KoalaCompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/KoalaCompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/Tools/KoalaCompiler?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Tools/KoalaCompiler?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Tools/KoalaCompiler?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Tools/KoalaCompiler?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Tools/KoalaCompiler?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Tools/KoalaCompiler?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/KoalaCompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/KoalaCompiler?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/Tools/KoalaCompiler?template=oopsmore&param1=1.8&param2=1.8)
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
Koala Compiler {#koala-compiler .twikiTopicTitle}
==============

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

+-----------------------------------+-----------------------------------+
| **News**                          | ![](../pub/Tools/KoalaCompiler/ko |
|                                   | ala.jpg)                          |
| -   *May-2-2007.* Version 0.3 of  |                                   |
|     the koala compiler has been   |                                   |
|     released. Checkout            |                                   |
|     [HowToObtainKoalaCompiler](ht |                                   |
| tp://www.program-transformation.o |                                   |
| rg/Tools/HowToObtainKoalaCompiler |                                   |
| ){.twikiLink}                     |                                   |
|                                   |                                   |
| **Description**                   |                                   |
|                                   |                                   |
| The Koala-compiler package forms  |                                   |
| an Open Source implementation of  |                                   |
| Koala. It is independent of the   |                                   |
| official Koala compiler as        |                                   |
| developed by [Philips             |                                   |
| Research](http://www.extra.resear |                                   |
| ch.philips.com/SAE/koala/).       |                                   |
| The package provides an open      |                                   |
| compiler implementation that can  |                                   |
| be used for research and for      |                                   |
| education purposes.               |                                   |
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
| The koala-compiler package        |                                   |
| includes:                         |                                   |
|                                   |                                   |
| -   The Koala language definition |                                   |
|     in SDF                        |                                   |
| -   A Koala parser                |                                   |
| -   A Koala normalizer            |                                   |
| -   A Koala pretty-printer        |                                   |
| -   A Koala vizualization tool    |                                   |
| -   A backend for C (+Makefile    |                                   |
|     generation). This provides    |                                   |
|     the functionality of the      |                                   |
|     original Philips Koala        |                                   |
|     compiler                      |                                   |
| -   A backend for [Source Tree    |                                   |
|     Composition](http://www.cs.uu |                                   |
| .nl/groups/ST/Merijn/PaperSourceT |                                   |
| reeComposition)                   |                                   |
+-----------------------------------+-----------------------------------+

**Contact**

-   [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} About
    koala-compiler package
-   [RobVanOmmering](../Main/RobVanOmmering){.twikiLink} about
    mainstream Koala development

**Publications**

-   [RobVanOmmering](../Main/RobVanOmmering){.twikiLink} and Frank van
    der Linden and Jeff Kramer and Jeff Magee. ***The Koala Component
    Model for Consumer Electronics***. *IEEE Software Computer*, 33(3),
    pp. 78-85, March 2000.

<!-- -->

-   [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink}. ***[Multi-level
    Component
    Composition](http://www.cs.uu.nl/groups/ST/Merijn/PaperMultiLevelComponentComposition)***.
    Bosch, Jan, Ed. 2nd Groningen Workshop on Software Variability
    Modeling (SVM\'04).

**Documentation**

-   [How to obtain
    KoalaCompiler](http://www.program-transformation.org/Tools/HowToObtainKoalaCompiler){.twikiLink}
-   [How to install
    KoalaCompiler](HowToInstallKoalaCompiler){.twikiLink}

<!-- -->

-   [How to options](HowToOptions){.twikiLink}

<!-- -->

-   [How to pretty-print a Koala specification](KoalaText){.twikiLink}
-   [How to vizualize a Koala specification](KoalaDot){.twikiLink}
-   [How to generate C code](KoalaC){.twikiLink}
-   [How to generate software bundles](KoalaSTC){.twikiLink}

<!-- -->

-   [How to extend](KoalaNormalize){.twikiLink}
-   [How to KoalaCompiler
    framework](HowToKoalaCompilerFramework){.twikiLink}

**Daily builds**

-   Daily builds of the Koala compiler are available at:
    <http://buildfarm.st.ewi.tudelft.nl/releases/strategoxt/full-status-koala-compiler.html>.
    Note that these distributions are under development and may not work
    at all.

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 22 Dec 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
