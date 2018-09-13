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
    Page](http://www.program-transformation.org/edit/Tools/HowToDefinePrettyPrintTables?t=1536826733)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/HowToDefinePrettyPrintTables)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/HowToDefinePrettyPrintTables)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/HowToDefinePrettyPrintTables?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/HowToDefinePrettyPrintTables?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Tools/HowToDefinePrettyPrintTables?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/HowToDefinePrettyPrintTables?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/HowToDefinePrettyPrintTables?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/HowToDefinePrettyPrintTables?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tools/HowToDefinePrettyPrintTables?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/HowToDefinePrettyPrintTables?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/HowToDefinePrettyPrintTables)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/HowToDefinePrettyPrintTables?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Tools/HowToDefinePrettyPrintTables?template=oopsmore&param1=1.4&param2=1.4)
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
How To Define Pretty Print Tables {#how-to-define-pretty-print-tables .twikiTopicTitle}
=================================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Task**

How to define pretty-print tables for use with [GPP](GPP){.twikiLink}.

**Description**

The utility [AsFixToAbox](AsFixToAbox){.twikiLink} is a
language-independent front-end for the pretty-print system
[GPP](GPP){.twikiLink}. Instantiated with a set of language specific
*formatting rules* it becomes a formatter for a specific language.

These formatting rules (or pretty-print rules) define mappings from
language constructs (specified as SDF productions) to BOX expressions.
BOX is a language independent markup language to describe the intended
layout of text. See [this
paper](http://www.cs.uu.nl/wiki/pub/Merijn/PaperPrettyPrinterForEveryOccasion/APrettyPrinterForEveryOccasion.pdf)
for more information about pretty-print tables and the BOX markup
language.

Pretty-print entries are defined in an ordered sequence of pretty-print
tables. This ordering allows overruling of pretty-print entries by
defining overruling entries in tables with higher precedence.

**Examples**

A pretty-print entry for a language construct S1 S2 \... Sn -\> S looks
like:

S1 S2 \... Sn -\> S \-- H \[ \_1 \_2 \... \_n\]

This entry defines a horizontal formatting (because of the H operator).
The BOX expressions corresponding to the formatted non-terminal symbols
S1 S2 \... Sn are refered to using the numbered place holders \_1 \_2
\... \_n

A more advanced example which defines a formatting for an
\`if-then-else\' construct is depicted below:

\[ \"if\" Cond \"then\" StatSeq \"else\" StatSeq \"fi\" -\> Stat \-- V
\[ V is=3 \[ H\[ KW\[\"if\"\] \_1 KW\[\"then\"\] \_2 \] V is=3 \[
KW\[\"else\]\" \_3 \] KW\[\"fi\"\] \] \]

The following BOX operators are used in this example: \`KW\' to format
keywords, \`H\' to layout boxes horizontally, and \`V\' to format
sub-boxes vertically. Furthermore, the space option \`is\' is used to
specify that the boxes in a vertical context should be indented to the
right. This example defines that if-then-else constructs should be
formatted as:

if Cond then StatSeq else StatSeq fi

**See also**

[GPP](GPP){.twikiLink},
[HowToPrettyPrintAGrammar](HowToPrettyPrintAGrammar){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
