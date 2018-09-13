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
    Page](http://www.program-transformation.org/edit/Tools/ATermService?t=1536826225)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/ATermService)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/ATermService)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/ATermService?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/ATermService?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Tools/ATermService?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/ATermService?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/ATermService?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/ATermService?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tools/ATermService?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/ATermService?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/ATermService)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/ATermService?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Tools/ATermService?template=oopsmore&param1=1.4&param2=1.4)
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
ATerm Service {#aterm-service .twikiTopicTitle}
=============

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

An [ATermService](ATermService){.twikiLink} is a software component
that:

-   is accessible at some URL using HTTP
-   takes an
    [Stratego.ATerm[^?^](http://www.program-transformation.org/edit/Stratego/ATerm?topicparent=Tools.ATermService)]{.twikiNewLink
    style="background : #FFFFCE;"} input in the body of a HTTP POST
    request
-   returns an
    [Stratego.ATerm[^?^](http://www.program-transformation.org/edit/Stratego/ATerm?topicparent=Tools.ATermService)]{.twikiNewLink
    style="background : #FFFFCE;"} output in a HTTP response

### []{#Library_support} Library support

You can implement an [ATermService](ATermService){.twikiLink} using any
language. Packages that support the implementation of
[ATermServices](ATermService){.twikiLink}:

-   [stratego-net](../Stratego/StrategoNetworking){.twikiLink}
-   [Java Stratego.ATerm
    Servlets[^?^](http://www.program-transformation.org/edit/Tools/JavaStrategoATermServlets?topicparent=Tools.ATermService)]{.twikiNewLink
    style="background : #FFFFCE;"}

### []{#Implementations} Implementations

-   [Stratego.ATerm Database
    Interface](ATermDatabaseInterface){.twikiLink} uses [Java
    Stratego.ATerm
    Servlets[^?^](http://www.program-transformation.org/edit/Tools/JavaStrategoATermServlets?topicparent=Tools.ATermService)]{.twikiNewLink
    style="background : #FFFFCE;"}

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 10 Mar
2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.ATermService moved from Stratego.ATermService on 03 Dec 2004 -
01:34 by [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* -
[put it
back](http://www.program-transformation.org/rename/Tools/ATermService?newweb=Stratego&newtopic=ATermService&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
