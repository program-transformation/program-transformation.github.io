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
    Page](http://www.program-transformation.org/edit/Tools/VisualizeAmbiguities?t=1536825773)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/VisualizeAmbiguities)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/VisualizeAmbiguities)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/VisualizeAmbiguities?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/VisualizeAmbiguities?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Tools/VisualizeAmbiguities?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Tools/VisualizeAmbiguities?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Tools/VisualizeAmbiguities?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/VisualizeAmbiguities?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/VisualizeAmbiguities?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/VisualizeAmbiguities?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/VisualizeAmbiguities)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/VisualizeAmbiguities?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Tools/VisualizeAmbiguities?template=oopsmore&param1=1.5&param2=1.5)
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
Visualize Ambiguities {#visualize-ambiguities .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[]{#Name} Name
--------------

visamb \-- display the ambiguities in a parse tree represented in
[AsFix2[^?^](http://www.program-transformation.org/edit/Tools/AsFix2?topicparent=Tools.VisualizeAmbiguities)]{.twikiNewLink
style="background : #FFFFCE;"}

[]{#Synopsis} Synopsis
----------------------

[]{#Description} Description
----------------------------

The SDF2 implementation caters for arbitrary context-free grammars. That
is, even for ambiguous grammars the parser will produce a parse trees
containing a concise encoding of allpossible parses. Ambiguities are
represented by means of amb nodes that contain a list of possible parse
trees at that point. For most applications, however, it is desirable to
develop unambiguous grammars. To aid the grammar writer in detecting and
solving the ambiguities, the visamb tool extracts the ambiguities from a
parse tree and displays them in a readable format.

Ambiguities are displayed by printing the non-terminals of the nodes of
the parse trees in the ambiguities. For instance, consider the syntax
definition

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

      echo "id id id" | sglr -2 -p Exp.tbl | visamb

the output of this command is:

      # ambiguities = 1
      + * id id id
        <Exp-CF>
          <Exp-CF>
            <Exp-CF>
              id
            <LAYOUT?-CF>
              <LAYOUT-CF>

            <Exp-CF>
              id
          <LAYOUT?-CF>
            <LAYOUT-CF>

          <Exp-CF>
            id
        <Exp-CF>
          <Exp-CF>
            id
          <LAYOUT?-CF>
            <LAYOUT-CF>

          <Exp-CF>
            <Exp-CF>
              id
            <LAYOUT?-CF>
              <LAYOUT-CF>

            <Exp-CF>
              id

Only the inner ambiguities are displayed, i.e., if a phrase **and** one
of its sub-phrases are ambiguous, only the ambiguities of the sub-phrase
is displayed.

[]{#See_Also} See Also
----------------------

-   [ambtracker](AmbTracker){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.VisualizeAmbiguities moved from Tools.visambGT on 17 Feb 2004 -
11:40 by [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* -
[put it
back](http://www.program-transformation.org/rename/Tools/VisualizeAmbiguities?newweb=Tools&newtopic=visambGT&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
