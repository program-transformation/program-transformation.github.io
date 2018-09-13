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
    Page](http://www.program-transformation.org/edit/Tools/XmlInfo?t=1536826732)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/XmlInfo)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/XmlInfo)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/XmlInfo?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/XmlInfo?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Tools/XmlInfo?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Tools/XmlInfo?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Tools/XmlInfo?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/XmlInfo?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/XmlInfo?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/XmlInfo?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/XmlInfo)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/XmlInfo?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Tools/XmlInfo?template=oopsmore&param1=1.5&param2=1.5)
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
Xml Info {#xml-info .twikiTopicTitle}
========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

\[Under construction \--
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 12 Jul 2003\]

[]{#Introduction} Introduction
------------------------------

The [xml-info](XmlInfo){.twikiLink} language is a representation of an
XML document in the
[Stratego.ATerm[^?^](http://www.program-transformation.org/edit/Stratego/ATerm?topicparent=Tools.XmlInfo)]{.twikiNewLink
style="background : #FFFFCE;"} format. The
[xml-info](XmlInfo){.twikiLink} language feels like a DOM representation
of an XML document, but it is just data, not an API. The -info part in
the name of this language indicates that it limits the representation of
an XML document to the information present in the document.

There is only an [abstract
syntax](../Stratego/AbstractSyntax){.twikiLink} for the xml-info
language (not a [concrete
syntax](../Stratego/ConcreteSyntax){.twikiLink}). The abstract syntax
for the xml-info language is defined by an RTG in the
[xml-front](XmlFront){.twikiLink} package.

Syntactical details like entities, comments, whitespace and empty
elements are not available in the xml-info language. The xml-info
language has constructs to represent XML namespaces. There is no
syntactic sugar in xml-info: every element and attribute has for example
the complete namespace URI in its name and as another example there is
no distinction between empty-elements and elements without children.

[]{#Definition_in_RTG} Definition in RTG
----------------------------------------

     __Note:__  Included topic [[https:..svn.cs.uu.nl:12443.repos.StrategoXT.trunk.StrategoXT.xml-front.sig.xml-info.xml-info.rtg]] does not exist yet

[]{#Related_topics} Related topics
----------------------------------

-   [parse-xml-info](XmlInfoParser){.twikiLink}
-   [pp-xml-info](XmlInfoPrettyPrinter){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.XmlInfo moved from Stratego.XmlInfo on 27 Jun 2004 - 19:46 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tools/XmlInfo?newweb=Stratego&newtopic=XmlInfo&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
