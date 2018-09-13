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
    Page](http://www.program-transformation.org/edit/Tools/HowToPrettyPrintAGrammar?t=1536826733)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/HowToPrettyPrintAGrammar)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/HowToPrettyPrintAGrammar)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/HowToPrettyPrintAGrammar?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/HowToPrettyPrintAGrammar?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Tools/HowToPrettyPrintAGrammar?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Tools/HowToPrettyPrintAGrammar?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Tools/HowToPrettyPrintAGrammar?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Tools/HowToPrettyPrintAGrammar?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Tools/HowToPrettyPrintAGrammar?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/HowToPrettyPrintAGrammar?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/HowToPrettyPrintAGrammar)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/HowToPrettyPrintAGrammar?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Tools/HowToPrettyPrintAGrammar?template=oopsmore&param1=1.6&param2=1.6)
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
How To Pretty Print AGrammar {#how-to-pretty-print-agrammar .twikiTopicTitle}
============================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Task**

How to pretty-print a grammar.

**Description**

A grammar can be pretty-printed (to plain text, html, or latex) using
the [GPP](GPP){.twikiLink} package in the following way:

1.  Parse the grammar.
2.  Feed the resulting parse tree to the pretty-print front-end
    [asfix2abox](AsFixToAbox){.twikiLink}.
3.  Feed the resulting [Box](BoxLanguage){.twikiLink} expression to one
    of the pretty-print back-ends:
    [abox2text[^?^](http://www.program-transformation.org/edit/Tools/AboxToText?topicparent=Tools.HowToPrettyPrintAGrammar)]{.twikiNewLink
    style="background : #FFFFCE;"}, [abox2html](AboxToHtml){.twikiLink},
    or [abox2latex](AboxToLaTex){.twikiLink}.

Alternatively, a grammar can be pretty-printed using the
[ast2abox[^?^](http://www.program-transformation.org/edit/Tools/AstToAbox?topicparent=Tools.HowToPrettyPrintAGrammar)]{.twikiNewLink
style="background : #FFFFCE;"} tool:

1.  Parse the grammar.
2.  Implode the resulting parse tree to an AST.
3.  Feed the AST to the pretty-print front-end
    [ast2abox[^?^](http://www.program-transformation.org/edit/Tools/AstToAbox?topicparent=Tools.HowToPrettyPrintAGrammar)]{.twikiNewLink
    style="background : #FFFFCE;"}
4.  Feed the resulting BOX expression to one of the pretty-print
    back-ends:
    [abox2text[^?^](http://www.program-transformation.org/edit/Tools/AboxToText?topicparent=Tools.HowToPrettyPrintAGrammar)]{.twikiNewLink
    style="background : #FFFFCE;"}, [abox2html](AboxToHtml){.twikiLink},
    or [abox2latex](AboxToLaTex){.twikiLink}.

**Examples**

Assuming G.tbl is the parse table for a grammar of language L and G.pp
is the corresponding pretty-print table. A term T.sdf over langauge L
can be pretty-printed to text, html and latex in the following way:

      # sglr -2 -p G.tbl -i T.sdf -o T.asfix
      # implode-asfix -i T.asfix -o T.af
      # ast2abox -p G.pp -i T.af -o T.sdf.abox
      # abox2text -i T.sdf.abox -o T.sdf.text
      # abox2html -i T.sdf.abox -o T.sdf.html
      # abox2latex -i T.sdf.abox -o T.sdf.tex

The file T.sdf.tex can be included in a latex document, which has the
following package statement in its preamble:

      \usepackage{boxenv}

In the file T.sdf.tex you can read where to find the file *boxenv.sty*
(See [HowToUseGPPWithLaTeX](HowToUseGPPWithLaTeX){.twikiLink}).

**See also**

[GenericPrettyPrinter](GenericPrettyPrinter){.twikiLink},
[HowToUseGPPWithLaTeX](HowToUseGPPWithLaTeX){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
