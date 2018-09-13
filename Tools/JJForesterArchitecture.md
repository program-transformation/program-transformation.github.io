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
    Page](http://www.program-transformation.org/edit/Tools/JJForesterArchitecture?t=1536826786)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/JJForesterArchitecture)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/JJForesterArchitecture)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/JJForesterArchitecture?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/JJForesterArchitecture?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Tools/JJForesterArchitecture?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/JJForesterArchitecture?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/JJForesterArchitecture?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/JJForesterArchitecture?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tools/JJForesterArchitecture?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/JJForesterArchitecture?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/JJForesterArchitecture)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/JJForesterArchitecture?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Tools/JJForesterArchitecture?template=oopsmore&param1=1.4&param2=1.4)
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
JJForester Architecture {#jjforester-architecture .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

Global architecture of JJForester: :
![jjf-arch.jpg](http://www.cwi.nl/~jvisser/jjforester/jjf-arch.jpg)
Ellipses are tools. Shaded boxes are generated code.

JJForester takes a grammar defined in SDF as input, and generates Java
code. In parallel, the parse table generator
[PGEN](../Sdf/PGEN){.twikiLink} is called to generate a parse table from
the grammar. The generated code is compiled together with code supplied
by the user. When the resulting byte code is run on a Java Virtual
Machine, invocations of *parse* methods will result in calls to the
parser [SGLR](../Sdf/SGLR){.twikiLink}. From a given input term,
[SGLR](../Sdf/SGLR){.twikiLink} produces a parse tree as output. These
parse trees are passed through the parse tree implosion tool
[ImplodeAsFix[^?^](http://www.program-transformation.org/edit/Tools/ImplodeAsFix?topicparent=Tools.JJForesterArchitecture)]{.twikiNewLink
style="background : #FFFFCE;"} to obtain abstract syntax trees.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
