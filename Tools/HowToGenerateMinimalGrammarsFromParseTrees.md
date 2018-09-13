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
    Page](http://www.program-transformation.org/edit/Tools/HowToGenerateMinimalGrammarsFromParseTrees?t=1536826785)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/HowToGenerateMinimalGrammarsFromParseTrees)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/HowToGenerateMinimalGrammarsFromParseTrees)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/HowToGenerateMinimalGrammarsFromParseTrees?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/HowToGenerateMinimalGrammarsFromParseTrees?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Tools/HowToGenerateMinimalGrammarsFromParseTrees?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/HowToGenerateMinimalGrammarsFromParseTrees?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/HowToGenerateMinimalGrammarsFromParseTrees?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/HowToGenerateMinimalGrammarsFromParseTrees?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tools/HowToGenerateMinimalGrammarsFromParseTrees?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/HowToGenerateMinimalGrammarsFromParseTrees?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/HowToGenerateMinimalGrammarsFromParseTrees)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/HowToGenerateMinimalGrammarsFromParseTrees?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Tools/HowToGenerateMinimalGrammarsFromParseTrees?template=oopsmore&param1=1.4&param2=1.4)
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
How To Generate Minimal Grammars From Parse Trees {#how-to-generate-minimal-grammars-from-parse-trees .twikiTopicTitle}
=================================================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Task**

Given a grammar and a parse tree obtained by parsing a term over this
grammar, construct a subgrammar that still parses the same term.

**Description**

Given a grammar *G* and a term *t* over that grammar, a subgrammar that
still parses *t* can be obtained in the following steps.

1.  Parse *t* over *G*, using
    [SdfToTable](../Sdf/SdfToTable){.twikiLink} and sglrSGLR, to obtain
    a parse tree *t.asfix*.
2.  Run the parse tree trough asfix2sdfGT, to obtain your subgrammar, in
    *normalized* Sdf form.
3.  Run the normalized subgrammar through sdfdenormalizeGT, to transfer
    the subgrammar into ordinary Sdf.
4.  Pretty-print the subgrammar.

**Examples**

Assume that L.def is an Sdf grammar for language L, and t is a term over
L.

\# sdf2table -i L.def -o L.tbl \# sglr -p L.tbl -i t -o t.asfix \#
asfix2sdf -i t.asfix \| sdf-de-normalize -o L.sub.def.af \# sdf2text -a
-i L.sub.def.af -o L.sub.def

**See Also**

[SdfToTable](../Sdf/SdfToTable){.twikiLink}, sglrSGLR, asfix2sdfGT,
sdfdenormalizeGT,
[HowToPrettyPrintAGrammar](HowToPrettyPrintAGrammar){.twikiLink}.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
