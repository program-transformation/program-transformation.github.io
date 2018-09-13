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
    Page](http://www.program-transformation.org/edit/Tools/XmlInfoPrettyPrinter?t=1536826733)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/XmlInfoPrettyPrinter)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/XmlInfoPrettyPrinter)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/XmlInfoPrettyPrinter?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/XmlInfoPrettyPrinter?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tools/XmlInfoPrettyPrinter?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/XmlInfoPrettyPrinter?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/XmlInfoPrettyPrinter?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/XmlInfoPrettyPrinter)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/XmlInfoPrettyPrinter?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tools/XmlInfoPrettyPrinter?template=oopsmore&param1=1.2&param2=1.2)
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
Xml Info Pretty Printer {#xml-info-pretty-printer .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

The `pp-xml-info` tool pretty prints [xml-info](XmlInfo){.twikiLink} to
text. This is a hand-crafted [pretty
printer[^?^](http://www.program-transformation.org/edit/Tools/PrettyPrinter?topicparent=Tools.XmlInfoPrettyPrinter)]{.twikiNewLink
style="background : #FFFFCE;"}. It is written using the
[StrategoBox](../Stratego/StrategoBox){.twikiLink} approach.

In fact the tool `pp-xml-info` is a composition of `xml-info2xml` and
`pp-xml`. This xml format is a representation of the syntax of an XML
document in the Stratego.ATerm format. [xml-info](XmlInfo){.twikiLink}
is a more abstract representation, ignoring syntactical details.

In `share/xml-tools` there is also a [GPP](../Stratego/GPP){.twikiLink}
[pretty print table](PrettyPrintTable){.twikiLink} for XML. The result
will be less attractive then the result of the
[StrategoBox](../Stratego/StrategoBox){.twikiLink}
[PrettyPrinter](../Stratego/PrettyPrinter){.twikiLink}, but it works.
Layout doesn\'t matter a lot for languages like XML after all: you
shouldn\'t read it too often ;) .\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.XmlInfoPrettyPrinter moved from Stratego.XmlInfoPrettyPrinter on
27 Jun 2004 - 19:45 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tools/XmlInfoPrettyPrinter?newweb=Stratego&newtopic=XmlInfoPrettyPrinter&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
