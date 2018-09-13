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
    Page](http://www.program-transformation.org/edit/Tools/KoalaDot?t=1536825806)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/KoalaDot)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/KoalaDot)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/KoalaDot?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/KoalaDot?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Tools/KoalaDot?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/KoalaDot?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/KoalaDot?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/KoalaDot?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tools/KoalaDot?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/KoalaDot?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/KoalaDot)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/KoalaDot?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Tools/KoalaDot?template=oopsmore&param1=1.4&param2=1.4)
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
Koala Dot {#koala-dot .twikiTopicTitle}
=========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

+-----------------------------------+-----------------------------------+
| A picture of a Koala              | [![](../pub/Tools/KoalaDot/plain- |
| specification can be generated    | small.jpg)](../pub/Tools/KoalaDot |
| with the `koala-dot` tool. This   | /plain.jpg)                       |
| tool reads a Koala composition,   |                                   |
| normalizes it and transforms a    |                                   |
| grapg in DOT format. For          |                                   |
| vizualization you need to heva    |                                   |
| ethe                              |                                   |
| [GraphViz](GraphViz){.twikiLink}  |                                   |
| package installed.                |                                   |
|                                   |                                   |
|        koala-dot -I <directory wi |                                   |
| th Koala components> \            |                                   |
|                   -i <top-level c |                                   |
| omponent> \                       |                                   |
|                   -n \            |                                   |
|                   -o graph.dot    |                                   |
|                                   |                                   |
| With the `dot` program that is    |                                   |
| part of                           |                                   |
| [GraphViz](GraphViz){.twikiLink}, |                                   |
| you can turn this graph into      |                                   |
| different output formats. E.g.,   |                                   |
|                                   |                                   |
|        dot -Tps graph.dot > graph |                                   |
| .ps                               |                                   |
|                                   |                                   |
| The elements in the graphs (like  |                                   |
| the one on the right) have to     |                                   |
| following meaning:                |                                   |
|                                   |                                   |
|   ------------- ----------------- |                                   |
| ------ -------------------------- |                                   |
| --------------------------------- |                                   |
| --------------------------------- |                                   |
| -------                           |                                   |
|   *module*      *present* module  |                                   |
|        yellow box                 |                                   |
|                 *normal* module   |                                   |
|        green box                  |                                   |
|   *component*                     |                                   |
|        pink/orange box            |                                   |
|                 *reachable* compo |                                   |
| nent   asterix (\*) attached to n |                                   |
| ame                               |                                   |
|   *interface*   *provides* interf |                                   |
| ace    blue triangle              |                                   |
|                                   |                                   |
|        a *connected* provides int |                                   |
| erfaces has an asterix (\*) attac |                                   |
| hed to its name                   |                                   |
|                 *requires* interf |                                   |
| ace    blue triangle              |                                   |
|                 *private* interfa |                                   |
| ce     blue diamond               |                                   |
|                 *optional* interf |                                   |
| ace    Dashed triangle            |                                   |
|   *switch*                        |                                   |
|        red box                    |                                   |
|                                   |                                   |
|        outgoing *red* arrows corr |                                   |
| espond to interface references fr |                                   |
| om switch expression.             |                                   |
|                                   |                                   |
|        The incomming edges corres |                                   |
| pond to the *in* cables, the outg |                                   |
| oing edges correspond to *out* ed |                                   |
| ges.                              |                                   |
|                                   |                                   |
|        The top label indicates th |                                   |
| e switch expression, the bottom l |                                   |
| abels correspond to switch condit |                                   |
| ions.                             |                                   |
|   *cable*       *normal*          |                                   |
|        arrow                      |                                   |
|                 *transitive*      |                                   |
|        dashed arrow               |                                   |
|   ------------- ----------------- |                                   |
| ------ -------------------------- |                                   |
| --------------------------------- |                                   |
| --------------------------------- |                                   |
| -------                           |                                   |
+-----------------------------------+-----------------------------------+

Normalization steps can be turned on by omitting the \'-n\' switch (see
below).

[![](../pub/Tools/KoalaDot/normalized-small.jpg)](../pub/Tools/KoalaDot/normalized.jpg)

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 22 Dec 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.KoalaDot moved from Tools.HowToVizualizeAKoalaSpecification on 22
Dec 2004 - 12:21 by [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink}*
- [put it
back](http://www.program-transformation.org/rename/Tools/KoalaDot?newweb=Tools&newtopic=HowToVizualizeAKoalaSpecification&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
