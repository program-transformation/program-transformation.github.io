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
    Page](http://www.program-transformation.org/edit/Tools/GenericPrettyPrinter?t=1536825757)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/GenericPrettyPrinter)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/GenericPrettyPrinter)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/GenericPrettyPrinter?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/GenericPrettyPrinter?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    9](http://www.program-transformation.org/view/Tools/GenericPrettyPrinter?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Tools/GenericPrettyPrinter?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Tools/GenericPrettyPrinter?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Tools/GenericPrettyPrinter?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Tools/GenericPrettyPrinter?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Tools/GenericPrettyPrinter?rev1=1.7&rev2=1.6)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/GenericPrettyPrinter)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/GenericPrettyPrinter?template=oopsmore&param1=1.9&param2=1.9)
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
    \...](http://www.program-transformation.org/oops/Tools/GenericPrettyPrinter?template=oopsmore&param1=1.9&param2=1.9)
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
Generic Pretty Printer {#generic-pretty-printer .twikiTopicTitle}
======================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[]{#Introduction} Introduction
------------------------------

The [GPP](GPP){.twikiLink} package is a tool suite for generic
pretty-printing. [GPP](GPP){.twikiLink} supports pretty-printing of
parse-trees in the [AsFix](AsFix){.twikiLink} format with comment
preservation and of abstract syntax trees. [GPP](GPP){.twikiLink}
supports the output formats plain text, LaTeX, and HTML. Formattings are
defined in pretty print tables, which can be generated from SDF syntax
definitions.

[]{#Tools} Tools
----------------

-   [abox2html](AboxToHtml){.twikiLink}
-   [abox2latex](AboxToLaTex){.twikiLink}
-   [abox2text](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-abox2text.html)

<!-- -->

-   [asfix2abox](AsFixToAbox){.twikiLink}
-   [ast2abox](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-ast2abox.html)

<!-- -->

-   [ppgen](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-ppgen.html)
-   [pptable-diff](PrettyPrintTableDiff){.twikiLink}

[]{#Languages} Languages
------------------------

[GPP](GPP){.twikiLink} is based on Box, a language independent markup
language to describe the intended layout of text.

-   [Box language](BoxLanguage){.twikiLink}
-   [Pretty Print Table](PrettyPrintTable){.twikiLink}

[]{#Documentation} Documentation
--------------------------------

-   [How to pretty print a
    grammar](HowToPrettyPrintAGrammar){.twikiLink}
-   [How to use GPP with LaTeX](HowToUseGPPWithLaTeX){.twikiLink}
-   [Pretty print tables](PrettyPrintTable){.twikiLink}
-   [Stratego.StrategoBox](../Stratego/StrategoBox){.twikiLink}

[]{#Links} Links
----------------

The official homepage of [GPP](GPP){.twikiLink}:

-   <http://www.cs.uu.nl/groups/ST/Merijn/GenericPrettyPrinter>

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
