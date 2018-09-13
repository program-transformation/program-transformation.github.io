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
    Page](http://www.program-transformation.org/edit/Tools/AmbTracker?t=1536826730)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/AmbTracker)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/AmbTracker)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/AmbTracker?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/AmbTracker?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tools/AmbTracker?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/AmbTracker?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/AmbTracker?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/AmbTracker)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/AmbTracker?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tools/AmbTracker?template=oopsmore&param1=1.2&param2=1.2)
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
Amb Tracker {#amb-tracker .twikiTopicTitle}
===========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[]{#Name} Name
--------------

ambtracker \-- display the productions in a parse tree causing
ambiguities

[]{#Description} Description
----------------------------

Compared to [visamb](VisualizeAmbiguities){.twikiLink} `ambtracker`
offers an alternative visualization of ambiguities in a parse tree.
`ambtracker` just displays the productions causing the ambiguity and not
how these productions are applied to the actual input. The location (row
and column) in the input where an ambiguity is caused is also displayed
for easy reference.

Consider the syntax definition that is used to illustrate
[visamb](VisualizeAmbiguities){.twikiLink}.

      definition
      module Main
      exports
        sorts Exp
        lexical syntax
          [\ \t\n] -> LAYOUT
        context-free syntax
          "id"    -> Exp
          Exp Exp -> Exp

From this syntax definition an SGLR parse table can be generated:

      sdf2table -i Exp.sdf -o Exp.tbl

The ambiguities of the phrase `id id id` can be shown with:

      echo "id id id" | sglr -2 -p Exp.tbl | ambtracker

the output of this command is:

      1 ambiguity cluster:

      [1/1] at (1:0):
        Exp  Exp -> Exp
        Exp  Exp -> Exp

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
