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
    Page](http://www.program-transformation.org/edit/Tools/XmlFront?t=1536825767)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/XmlFront)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/XmlFront)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/XmlFront?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/XmlFront?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tools/XmlFront?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/XmlFront?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/XmlFront?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/XmlFront)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/XmlFront?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tools/XmlFront?template=oopsmore&param1=1.2&param2=1.2)
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
Xml Front {#xml-front .twikiTopicTitle}
=========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[]{#Components_of_xml_front} Components of xml-front
----------------------------------------------------

-   [XML syntax definition](XmlSyntaxDefinition){.twikiLink} in
    [SDF](http://www.syntax-definition.org)
-   [concrete syntax for XML in
    Stratego](../Stratego/XmlConcreteSyntaxInStratego){.twikiLink}
-   [xml-info](XmlInfo){.twikiLink} language for the representation of
    XML documents in ATerms

<!-- -->

-   [aterm2xml](ATermToXml){.twikiLink} \-- convert an ATerm to an XML
    document.
-   [xml2aterm](XmlToATerm){.twikiLink} \-- convert an XML document to
    an ATerm.

<!-- -->

-   [parse-xml-doc[^?^](http://www.program-transformation.org/edit/Tools/XmlDocParser?topicparent=Tools.XmlFront)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- parses an XML document to xml-doc
-   [pp-xml-doc[^?^](http://www.program-transformation.org/edit/Tools/XmlDocPrettyPrinter?topicparent=Tools.XmlFront)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- pretty-prints xml-doc to an XML
    document
-   [parse-xml-info](XmlInfoParser){.twikiLink} \-- parses an XML
    document to [xml-info](XmlInfo){.twikiLink}
-   [pp-xml-info](XmlInfoPrettyPrinter){.twikiLink} \-- pretty-prints
    [xml-info](XmlInfo){.twikiLink} to an XML document
-   [data2xml-doc[^?^](http://www.program-transformation.org/edit/Tools/DataToXmlDoc?topicparent=Tools.XmlFront)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- transforms an ATerm to a
    comparable XML document represented in xml-doc.
-   [xml-info2data[^?^](http://www.program-transformation.org/edit/Tools/XmlInfoToData?topicparent=Tools.XmlFront)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- transforms
    [xml-info](XmlInfo){.twikiLink} to a somewhat comparable ATerm

[]{#Download_and_installation} Download and installation
--------------------------------------------------------

From [version 0.11](../Stratego/StrategoRelease011){.twikiLink}
xml-front is part of StrategoXT.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
