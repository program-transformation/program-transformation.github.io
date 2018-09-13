::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

[![](../pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Transform/SimpleAPIforXML?t=1536826228)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/SimpleAPIforXML)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/SimpleAPIforXML)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/SimpleAPIforXML?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/SimpleAPIforXML?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/SimpleAPIforXML?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/SimpleAPIforXML?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/SimpleAPIforXML?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/SimpleAPIforXML)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/SimpleAPIforXML?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/SimpleAPIforXML?template=oopsmore&param1=1.2&param2=1.2)
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
Simple APIfor [XML](XML){.twikiLink} {#simple-apifor-xml .twikiTopicTitle}
====================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Homepage**: <http://www.saxproject.org/>

The Simple [API](API){.twikiLink} for [XML](XML){.twikiLink}
([SAX](SAX){.twikiLink}) is a standard interface for event-based
[XML](XML){.twikiLink} parsing. Because of the event-based approach the
interface is very efficient and in special good at handling large
[XML](XML){.twikiLink} documents.

[SAX](SAX){.twikiLink} has quickly become a \'de facto\' standard.
Nowadays almost any [XML](XML){.twikiLink} based applications accepts
content from a [SAX](SAX){.twikiLink} ContentHandler. Alternative
[DOM](DOM){.twikiLink} implementations like JDOM use a
[SAX](SAX){.twikiLink} interface to [XML](XML){.twikiLink} parsers to
create a [DOM](DOM){.twikiLink}.

[SAX](SAX){.twikiLink} provides attractive possibilities to create
chains of components where the events flow through. Each components
(also called filters) can make changes to the events or just pass them
to next component. [XSL](XSL){.twikiLink} transformation can be included
in such a processing chain with the standard [XML](XML){.twikiLink}
transformation [API](API){.twikiLink}
([TraX[^?^](http://www.program-transformation.org/edit/Transform/TraX?topicparent=Transform.SimpleAPIforXML)]{.twikiNewLink
style="background : #FFFFCE;"}) of Java.

Verifiers (also known validators) can also be used as a component of
such a chain. They check whether the [XML](XML){.twikiLink} content of
the events satisfies a given schema in a certain
[SchemaLanguageForXML](SchemaLanguageForXML){.twikiLink}.

A generic set of interface for verification called JARV is available at:
<http://iso-relax.sourceforge.net/JARV/>

Several libraries for [RelaxNG](RelaxNG){.twikiLink} can be used as a
concrete implementation of JARV. There is also an implementation for
[XMLSchema](XMLSchema){.twikiLink}, which uses the Xerces2 of Apache:
<http://www.kohsuke.org/jarv/xerces/>\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
