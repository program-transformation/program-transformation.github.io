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
    Page](http://www.program-transformation.org/edit/Tools/XmlSyntaxDefinition?t=1536826796)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/XmlSyntaxDefinition)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/XmlSyntaxDefinition)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/XmlSyntaxDefinition?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/XmlSyntaxDefinition?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Tools/XmlSyntaxDefinition?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/XmlSyntaxDefinition?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/XmlSyntaxDefinition?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/XmlSyntaxDefinition?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tools/XmlSyntaxDefinition?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/XmlSyntaxDefinition?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/XmlSyntaxDefinition)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/XmlSyntaxDefinition?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Tools/XmlSyntaxDefinition?template=oopsmore&param1=1.4&param2=1.4)
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
Xml Syntax Definition {#xml-syntax-definition .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[xml-tools](XmlTools){.twikiLink} contains a syntax definition in
[SDF](../Stratego/SDF){.twikiLink} for
[XML](../Transform/XML){.twikiLink}. This syntax defintion is *not*
competely compatible with XML, but it tries to do the job as good as
possible in a pure syntax definition.

The syntax definition should *not* be used for parsing XML files. This
might sound odd, but for standard XML parsers do a much better job in
terms of performance and standard compliance. The parse-xml-info tool
supports parsing XML files with the standard XML parser of Java. So what
is the use of the syntax definition? It can be used to embed XML in
programming languages like Stratego and Java.

Besides the obvious constructs, the grammar supports entities, character
references and namespaces.

Known problems:

-   Stratego.ATerm, [SGLR](../Stratego/SGLR){.twikiLink}, and
    [SDF](../Stratego/SDF){.twikiLink} just support ASCII and therefore
    the grammar just supports ASCII. This will not change until
    [SGLR](../Stratego/SGLR){.twikiLink} and
    [SDF](../Stratego/SDF){.twikiLink} supports
    [Unicode](../Transform/UNICODE){.twikiLink}.

<!-- -->

-   DTD declarations in XML files are not supported. The DTD grammar is
    work in progress. Maybe DTD constructs in XML documents will be
    supported when this grammar is stable. External document type
    declarations (DOCTYPE) are supported.

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 30 Oct
2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.XmlSyntaxDefinition moved from Stratego.XmlSyntaxDefinition on 27
Jun 2004 - 19:56 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tools/XmlSyntaxDefinition?newweb=Stratego&newtopic=XmlSyntaxDefinition&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
