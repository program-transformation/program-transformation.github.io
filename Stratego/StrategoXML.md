::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
  ----------------------------------------------------------------------------------
  [![](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)](WebHome)
  ----------------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

-   [Documentation](StrategoDocumentation){.twikiLink}
-   [Language](StrategoLanguage){.twikiLink}
-   [Research Papers](StrategoPublications){.twikiLink}
-   [Applications](StrategoApplication){.twikiLink}

**[Download](StrategoDownload){.twikiLink}**

-   [Continuous build](ContinuousBuild){.twikiLink}
-   [Extensions](AdditionalPackageDownload){.twikiLink}

**[Support](StrategoSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Users Days](StrategoUsersDay){.twikiLink}
-   [Bug Reports](http://yellowgrass.org/project/StrategoXT)

**[Developers](StrategoDev){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/StrategoXT/strategoxt/trunk)
-   [Buildfarm
    results](http://hydra.nixos.org/jobset/strategoxt/strategoxt-release/all)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Stratego/StrategoXML?t=1536825684)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoXML)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoXML)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoXML?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoXML?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    11](http://www.program-transformation.org/view/Stratego/StrategoXML?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/Stratego/StrategoXML?rev1=1.11&rev2=1.10)
-   [Rev
    10](http://www.program-transformation.org/view/Stratego/StrategoXML?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Stratego/StrategoXML?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Stratego/StrategoXML?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Stratego/StrategoXML?rev1=1.9&rev2=1.8)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoXML)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoXML?template=oopsmore&param1=1.11&param2=1.11)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoXML?template=oopsmore&param1=1.11&param2=1.11)
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
Stratego XML {#stratego-xml .twikiTopicTitle}
============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[StrategoLanguage](StrategoLanguage){.twikiLink} is designed for
transformation of tree or term structures. Stratego has support for the
definition of generic traversals over trees, which makes the
specification of transformations of trees very convenient. This model is
very well suited for manipulation of [XML](../Transform/XML){.twikiLink}
documents.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 20 Mar 2001\

See [XmlTools](../Tools/XmlTools){.twikiLink} for an implementation of
the expressed ideas.

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 27 Feb
2003

Well not an [XML](../Transform/XML){.twikiLink}
[SourceToSource[^?^](http://www.program-transformation.org/edit/Stratego/SourceToSource?topicparent=Stratego.StrategoXML)]{.twikiNewLink
style="background : #FFFFCE;"} transformation but
[GraphXML2Dot[^?^](http://www.program-transformation.org/edit/Stratego/GraphXML2Dot?topicparent=Stratego.StrategoXML)]{.twikiNewLink
style="background : #FFFFCE;"} is a good example of an
[XML](../Transform/XML){.twikiLink} transformation in Stratego. The tool
is contained in XT.

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} \-- 24 Mar 2001\

A set of components to transform XML documents to XHTML would be a
valuable addition to XT. With these tools Stratego can be used to
perform transformations from XML to XHTML (on the serverside for
example) and in this way offer an attractive and powerful alternative to
XSLT, which is relatively weak compared to Stratego.

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 08 Dec
2001\

The authors of the paper [XML transformation flow
processing](http://transmorpher.inrialpes.fr/wpaper/) think that
Stratego could be applied profitably to the transformation of XML
documents. The paper describes the
[Transmorpher](http://transmorpher.inrialpes.fr/) system for XML
transformation.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 15 Mar 2002

At: <http://www.mbravenboer.org/docs/xml-pem-2002.pdf> you can find a
presentation on the integration of XML in XT. This presentation
discusses some tools which will make
[StrategoXML](StrategoXML){.twikiLink} a fact in the near future.

This tool-set will use existing XML parsers to translate XML into
ATerms. This is an efficient solution because the processing of XML
requires the handling of XMLNamespaces, entities,
[DocumentTypeDefinitions](../Transform/DocumentTypeDefinition){.twikiLink},
processing instructions and comments, which are all completely
irrelevant to the data we are interested in. This component is called
the SAXBridge because it uses the
[SimpleAPIforXML](../Transform/SimpleAPIforXML){.twikiLink}.

Although XML and ATerms are both regular tree languages and instances
can be described by
[RegularTreeGrammars[^?^](http://www.program-transformation.org/edit/Transform/RegularTreeGrammars?topicparent=Stratego.StrategoXML)]{.twikiNewLink
style="background : #FFFFCE;"}, they are used in quite different ways.
Therefore the result of the will be transformed into a more ATerm-like
structure by an ATermfication. This ATermification must be written by
hand right now (see the presentation for a small example), but we are
working on tool that generates this ATermification from a schema in a
certain
[SchemaLanguageForXML](../Transform/SchemaLanguageForXML){.twikiLink}.
An [AlgebraicSignature](AlgebraicSignature){.twikiLink} for Stratego
will also be generated by this tool.

Possible applications of [StrategoXML](StrategoXML){.twikiLink} include:

-   transforming or analysing XSLT
-   XSLT Compiler in Stratego with concrete syntax for the target
    language.
-   XML schema tools: verifiers, converters
-   server-side applications in Stratego: transformation to XHTML

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 30 May
2002

------------------------------------------------------------------------

[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.StrategoXML)]{.twikiNewLink
style="background : #FFFFCE;"}, [ToDo](ToDo){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
