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
    Page](http://www.program-transformation.org/edit/Tools/AboxToLaTex?t=1536826731)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/AboxToLaTex)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/AboxToLaTex)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/AboxToLaTex?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/AboxToLaTex?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Tools/AboxToLaTex?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Tools/AboxToLaTex?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Tools/AboxToLaTex?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/AboxToLaTex?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/AboxToLaTex?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/AboxToLaTex?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/AboxToLaTex)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/AboxToLaTex?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Tools/AboxToLaTex?template=oopsmore&param1=1.5&param2=1.5)
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
Abox To La Tex {#abox-to-la-tex .twikiTopicTitle}
==============

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Name**

abox2latex

**Synopsis**

abox2latex \[\--alltt\] \[\--boxenv\] \[-i box-term\] \[-o html-file\]
\[-w width\] \[-t abbreviations\_file\] **Description**

The utility abox2latex produces
[LaTeX[^?^](http://www.program-transformation.org/edit/Tools/LaTeX?topicparent=Tools.AboxToLaTex)]{.twikiNewLink
style="background : #FFFFCE;"} code according to the formatting defined
in *box-term*. See
[HowToUseGPPWithLaTeX](HowToUseGPPWithLaTeX){.twikiLink} for
instructions about how to use the generated
[LaTeX[^?^](http://www.program-transformation.org/edit/Tools/LaTeX?topicparent=Tools.AboxToLaTex)]{.twikiNewLink
style="background : #FFFFCE;"} code in your
[LaTeX[^?^](http://www.program-transformation.org/edit/Tools/LaTeX?topicparent=Tools.AboxToLaTex)]{.twikiNewLink
style="background : #FFFFCE;"} documents.

**Options**

 \--alltt
:   Instructs abox2latex to produce an alltt environment. See
    [HowToUseGPPWithLaTeX](HowToUseGPPWithLaTeX){.twikiLink} how this
    serves layout-preserving pretty-printing

<!-- -->

 \--boxenv
:   Instructs abox2latex to produce a fully formatted boxenv environment
    (default)

<!-- -->

 -h
:   display usage information. Use this option to get information on
    additional options

<!-- -->

 -t \<table\>
:   With this switch latex abreviations can be specified. The abox2latex
    utility can replace ordinary BOX strings by
    [LaTeX[^?^](http://www.program-transformation.org/edit/Tools/LaTeX?topicparent=Tools.AboxToLaTex)]{.twikiNewLink
    style="background : #FFFFCE;"} commands. These mappings can be
    defined in abbreviation tables. For example, to specify that the
    string \"\\\\//\" should be replaced by abox2latex to the
    [LaTeX[^?^](http://www.program-transformation.org/edit/Tools/LaTeX?topicparent=Tools.AboxToLaTex)]{.twikiNewLink
    style="background : #FFFFCE;"} command \\vee, the abbreviations
    table should look like:

<!-- -->

    [
     ["\\/", "\\ensuremath{\\vee}"]
    ]

Multiple abbreviation tables can be passed to abox2latex.

 -v
:   display version information

<!-- -->

 -w \<width\>
:   Table containing box to latex macro mappings. With this switch the
    maximum line width can be specified. The default line width equals
    80 columns.

**See also**

[GenericPrettyPrinter](GenericPrettyPrinter){.twikiLink},
[AstToAbox[^?^](http://www.program-transformation.org/edit/Tools/AstToAbox?topicparent=Tools.AboxToLaTex)]{.twikiNewLink
style="background : #FFFFCE;"}, [AsFixToAbox](AsFixToAbox){.twikiLink},
[HowToPrettyPrintAGrammar](HowToPrettyPrintAGrammar){.twikiLink},
[HowToUseGPPWithLaTeX](HowToUseGPPWithLaTeX){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.AboxToLaTex moved from Tools.box2latexGPP on 10 Feb 2004 - 09:03
by [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tools/AboxToLaTex?newweb=Tools&newtopic=box2latexGPP&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
