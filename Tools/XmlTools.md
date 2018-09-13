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
    Page](http://www.program-transformation.org/edit/Tools/XmlTools?t=1536825767)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/XmlTools)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/XmlTools)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/XmlTools?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/XmlTools?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    23](http://www.program-transformation.org/view/Tools/XmlTools?rev=1.23)
    [(diff 22)](http://www.program-transformation.org/rdiff/Tools/XmlTools?rev1=1.23&rev2=1.22)
-   [Rev
    22](http://www.program-transformation.org/view/Tools/XmlTools?rev=1.22)
    [(diff 21)](http://www.program-transformation.org/rdiff/Tools/XmlTools?rev1=1.22&rev2=1.21)
-   [Rev
    21](http://www.program-transformation.org/view/Tools/XmlTools?rev=1.21)
    [(diff 20)](http://www.program-transformation.org/rdiff/Tools/XmlTools?rev1=1.21&rev2=1.20)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/XmlTools)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/XmlTools?template=oopsmore&param1=1.23&param2=1.23)
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
    \...](http://www.program-transformation.org/oops/Tools/XmlTools?template=oopsmore&param1=1.23&param2=1.23)
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
Xml Tools {#xml-tools .twikiTopicTitle}
=========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

::: {.twikiToc}
-   [Introduction](XmlTools#Introduction)
-   [Components of xml-tools](XmlTools#Components_of_xml_tools)
-   [Resources](XmlTools#Resources)
-   [Download and installation](XmlTools#Download_and_installation)
-   [See also](XmlTools#See_also)
:::

[]{#Introduction} Introduction
------------------------------

This packages is not being maintained at the moment. Some parts of it
have been mvoed to [xml-front](XmlFront){.twikiLink}, which is now part
of StrategoXT. Maybe the remaining tools will be added later.

Although there are many differences in structure and syntax, XML and
ATerms are strongly related. Both formats are used to exchange tree-like
data between components. Because XML and ATerms are used in the exchange
of data between components, it would be useful to have the techniques
and tools to exchange data between components that operate on XML and
tools that operate on ATerms.

The result of such tooling will be that we can use the huge amount of
tools for XML and that we can open our Stratego.ATerm based tools to the
XML world.

xml-tools offers the required tools to make this possible. The package
still has to evolve, but the tools can already be applied for the
described goals.

[]{#Components_of_xml_tools} Components of xml-tools
----------------------------------------------------

-   [Interpretation of XML](XmlInterpretation){.twikiLink} against a
    schema

[]{#Resources} Resources
------------------------

-   The first part of the presentation [xml transformations and
    distributed
    services](http://www.students.cs.uu.nl/~mbravenb/docs/pt-xml.pdf) is
    devoted to xml-tools and in particular introduces the structuring of
    xml documents by interpreting them against a schema.

[]{#Download_and_installation} Download and installation
--------------------------------------------------------

The latest sources can be checked out using:

    svn checkout https://svn.strategoxt.org/repos/StrategoXT/obsolete/xml-tools/

Configure the package:

-   `--with-strategoxt`
-   `--with-sdf`
-   `--with-aterm`
-   `--with-netx` (optional) : If you want to use the schema conversion
    tools you need [Netx](http://jnlp.sourceforge.net/netx/). Netx is a
    JNLP client. You have to be connected to the Internet the first time
    you run a schema conversion tool.

[]{#See_also} See also
----------------------

-   [samples-net-xml](../Stratego/SamplesNetXml){.twikiLink} \-- a
    samples package using [XmlTools](XmlTools){.twikiLink} for
    [StrategoNetworking](../Stratego/StrategoNetworking){.twikiLink}.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.XmlTools moved from Stratego.XmlTools on 27 Jun 2004 - 19:47 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tools/XmlTools?newweb=Stratego&newtopic=XmlTools&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
