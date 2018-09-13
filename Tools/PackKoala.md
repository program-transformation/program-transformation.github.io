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
    Page](http://www.program-transformation.org/edit/Tools/PackKoala?t=1536826792)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/PackKoala)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/PackKoala)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/PackKoala?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/PackKoala?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Tools/PackKoala?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/PackKoala?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/PackKoala?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/PackKoala?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tools/PackKoala?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/PackKoala?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/PackKoala)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/PackKoala?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Tools/PackKoala?template=oopsmore&param1=1.4&param2=1.4)
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
Pack Koala {#pack-koala .twikiTopicTitle}
==========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Description**

The tool `pack-koala` packs the Koala component and interface
definitions and produces a parse tree for the complete Koala
specification.

**Example**

/pub/Tools/PackKoala/pack-koala.gif

Suppose that we want to obtain the complete parse tree of a Koala
composition specified in `koala-tools-bundle`:

       component koala-tools-bundle {
          contains
             component ASFIX-TOOLS asfix-tools;
             component ATerm aterm;
             component GPP gpp;
             component GRAPH-TOOLS graph-tools;
             component mySGLR sglr;
             component Stratego stratego;
             component KOALA-TOOLS koala-tools;
       }

If all component, interface, and data type definitions are stored in
`./koala-pb`. Then the following command will yield the desired parse
tree:

       pack-koala -I ./koala-pb -i koala-tools-bundle

This parse tree can be further transformed with `asfix-yield` to obtain
a textual representation of the composition:

       pack-koala -I ./koala-pb -i koala-tools-bundle \
       | asfix-yield

or imploded into an abstract syntax tree with `implode-asfix`:

       pack-koala -I ./koala-pb -i koala-tools-bundle \
       | implode-asfix

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 17 Feb 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
