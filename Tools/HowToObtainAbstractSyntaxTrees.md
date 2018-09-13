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
    Page](http://www.program-transformation.org/edit/Tools/HowToObtainAbstractSyntaxTrees?t=1536826785)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/HowToObtainAbstractSyntaxTrees)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/HowToObtainAbstractSyntaxTrees)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/HowToObtainAbstractSyntaxTrees?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/HowToObtainAbstractSyntaxTrees?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Tools/HowToObtainAbstractSyntaxTrees?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Tools/HowToObtainAbstractSyntaxTrees?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Tools/HowToObtainAbstractSyntaxTrees?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/HowToObtainAbstractSyntaxTrees?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/HowToObtainAbstractSyntaxTrees?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/HowToObtainAbstractSyntaxTrees?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/HowToObtainAbstractSyntaxTrees)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/HowToObtainAbstractSyntaxTrees?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Tools/HowToObtainAbstractSyntaxTrees?template=oopsmore&param1=1.5&param2=1.5)
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
How To Obtain Abstract Syntax Trees {#how-to-obtain-abstract-syntax-trees .twikiTopicTitle}
===================================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Task**

How to obtain abstract syntax trees

**Description**

Given a concrete term over some language L, an abstract syntax tree for
that term is obtained by:

1.  generating a parse table from the grammar of L
2.  parsing the concrete term using this parse table
3.  imploding the parse tree to an abstract syntax tree

In order for the parse tree implosion to work properly, the grammar of L
should be annotated with cons(\...) attributes.

**Examples**

Assuming L.def is a grammar for L, and term.l is a concrete term over
language L, an abstract syntax tree is obtained as follows: \# sdf2table
-i L.def -o L.tbl \# sglr -p L.tbl -i term.l -o term.l.asfix \#
implode-asfix -i term.l.asfix -o term.l.ast

**See also**

[ImplodeAsFix[^?^](http://www.program-transformation.org/edit/Tools/ImplodeAsFix?topicparent=Tools.HowToObtainAbstractSyntaxTrees)]{.twikiNewLink
style="background : #FFFFCE;"}, sglrSGLR,
[SdfToTable](../Sdf/SdfToTable){.twikiLink}.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
