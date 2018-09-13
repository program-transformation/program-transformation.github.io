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
    Page](http://www.program-transformation.org/edit/Tools/AsFixToAbox?t=1536826732)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/AsFixToAbox)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/AsFixToAbox)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/AsFixToAbox?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/AsFixToAbox?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Tools/AsFixToAbox?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Tools/AsFixToAbox?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Tools/AsFixToAbox?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Tools/AsFixToAbox?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Tools/AsFixToAbox?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Tools/AsFixToAbox?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/AsFixToAbox)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/AsFixToAbox?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Tools/AsFixToAbox?template=oopsmore&param1=1.7&param2=1.7)
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
As Fix To Abox {#as-fix-to-abox .twikiTopicTitle}
==============

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Name**

asfix2abox

**Synopsis**

asfix2abox \[-c\] \[-i asfix-tree\] \[-o box-term\] \[-p table1\] \[-p
table2\] \...

**Description**

The asfix2abox utility is a generic formatter that maps a parse-tree
represented in [AsFix](AsFix){.twikiLink} to BOX according to the
pretty-print rules specified in the pretty-print tables \<table1\>
\<table2\> \...

The utility accepts an ordered sequence of pretty-print tables which
define mappings from language constructs to BOX expressions (See
[HowToDefinePrettyPrintTables](HowToDefinePrettyPrintTables){.twikiLink}).
The tables are ordered such that the pretty-print rules in \<table1\>
have higher precedence than the entries in \<table2\>.

The BOX term that is produced by asfix2abox can be passed to one of the
available back-ends to obtain a plain text, HTML, or LaTeX
representation of your input term (See
[HowToPrettyPrintAGrammar](HowToPrettyPrintAGrammar){.twikiLink}).

**Options**

 -c
:   Conservative pretty-printing (only format where needed).

<!-- -->

 -h
:   display usage information. Use this option to get information on
    additional options

<!-- -->

 -p \<table\>
:   Use pretty-print rules defined in \<table\>. Multiple tables can be
    specified

<!-- -->

 -v
:   display version information

**See also**

[GenericPrettyPrinter](GenericPrettyPrinter){.twikiLink},
[HowToPrettyPrintAGrammar](HowToPrettyPrintAGrammar){.twikiLink},
[HowToDefinePrettyPrintTables](HowToDefinePrettyPrintTables){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.AsFixToAbox moved from Tools.asfix2boxGPP on 10 Feb 2004 - 09:12
by [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tools/AsFixToAbox?newweb=Tools&newtopic=asfix2boxGPP&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
