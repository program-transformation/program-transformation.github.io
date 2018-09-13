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
    Page](http://www.program-transformation.org/edit/Tools/KoalaNormalize?t=1536825807)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/KoalaNormalize)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/KoalaNormalize)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/KoalaNormalize?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/KoalaNormalize?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tools/KoalaNormalize?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/KoalaNormalize?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/KoalaNormalize?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/KoalaNormalize)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/KoalaNormalize?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tools/KoalaNormalize?template=oopsmore&param1=1.2&param2=1.2)
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
Koala Normalize {#koala-normalize .twikiTopicTitle}
===============

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

The tool `koala-normalize` performs Koala normalizations without code
generation. It takes a Koala composition as input and produces an
abstract syntax tree (AST) of the normalized Koala composition as
output.

       koala-normalize -I <directory with Koala components> \
                       -i <top-level component> \
                       -o composition.af

The output of `koala-normalize` can be connected to the input of
additional (third-party) backends. This way, support for new languanges
in addition to C can be added, or new levels of composition can be
defined (see
<http://www.cs.uu.nl/wiki/Merijn/PaperMultiLevelComponentComposition>).

As a simple example, the output can be connected to a pretty-printer:

       pp-koala -i composition.af

If certain normalization steps are not needed, they can be turned off
with the \'\--no\' switchs. E.g.,

       koala-normalize -I <directory with Koala components> \
                       -i <top-level component> \
                       -o composition.af \
                       --no koala-pruner

The list of normalization steps can be obtained with the \'\--help\'
switch. Note that disabling arbitrary normalization steps may yield
unpredictable results. Use with care.

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 22 Dec 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
