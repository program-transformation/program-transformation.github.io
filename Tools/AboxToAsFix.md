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
    Page](http://www.program-transformation.org/edit/Tools/AboxToAsFix?t=1536826786)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/AboxToAsFix)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/AboxToAsFix)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/AboxToAsFix?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/AboxToAsFix?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tools/AboxToAsFix?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/AboxToAsFix?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/AboxToAsFix?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/AboxToAsFix)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/AboxToAsFix?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tools/AboxToAsFix?template=oopsmore&param1=1.2&param2=1.2)
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
Abox To As Fix {#abox-to-as-fix .twikiTopicTitle}
==============

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Name**

box2asfix

**Synopsis**

box2asfix \[-i box-term\] \[-o asfix-tree\] \[-w width\] -t asfix-tree

**Description**

The utility box2asfix produces an [AsFix](AsFix){.twikiLink} parse-tree
in which the layout nodes are updated according to the formatting
specified in \`box-tree\'.

The utility takes as input an asfix-term (specified with the \`-t\'
option) in which the layout nodes needs to be updated, and a box-term
(specified with the \`-o\' option) which describes *how* the layout
nodes should be updated.

The -w option can be used to specify the maximal line width.The line
width defaults to 80 columns.

**Options**

-h : display usage information. Use this option to get information on
additional options

-q : run quietly

-v : display version information

**Limitations**

The box2asfix utility only accepts
[AsFix1[^?^](http://www.program-transformation.org/edit/Tools/AsFix1?topicparent=Tools.AboxToAsFix)]{.twikiNewLink
style="background : #FFFFCE;"} parse-trees.

**See also**

[GPP](GPP){.twikiLink},
[HowToPrettyPrintAGrammar](HowToPrettyPrintAGrammar){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.AboxToAsFix moved from Tools.box2asfixGPP on 10 Feb 2004 - 09:09
by [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tools/AboxToAsFix?newweb=Tools&newtopic=box2asfixGPP&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
