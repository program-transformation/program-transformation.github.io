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
    Page](http://www.program-transformation.org/edit/Tools/KoalaGraph?t=1536826791)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/KoalaGraph)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/KoalaGraph)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/KoalaGraph?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/KoalaGraph?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Tools/KoalaGraph?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/KoalaGraph?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tools/KoalaGraph?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/KoalaGraph?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/KoalaGraph?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/KoalaGraph)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/KoalaGraph?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Tools/KoalaGraph?template=oopsmore&param1=1.3&param2=1.3)
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
Koala Graph {#koala-graph .twikiTopicTitle}
===========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Description**

The tool `koala-graph` generates a graphical representation of a Koala
specification as a Dot graph. The generated output is an abstract syntax
tree of Dot. It can be pretty-printed and passed to `dot` to obtain a
graphical representation of a Koala composition.

**Example**

The picture showed at [KoalaWire](KoalaWire){.twikiLink} is produces as
follows:

       pack-koala -I ./koala-pb -i koala-tools-bundle \
       | implode-asfix \
       | koala-wire \
       | koala-graph \
       | pp-dot \
       | dot -NHelvetica -Tgif -Gsize=8,8

The tool `pp-dot` is used to pretty-print (i.e., transform to plain
text) the Dot abstract syntax tree. The tool `dot` is then used to
produce a gif picture.

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 17 Feb 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
