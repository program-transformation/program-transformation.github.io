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
    Page](http://www.program-transformation.org/edit/Transform/DSLBibliographyTerminology?t=1536826450)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DSLBibliographyTerminology)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DSLBibliographyTerminology)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DSLBibliographyTerminology?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DSLBibliographyTerminology?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/DSLBibliographyTerminology?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/DSLBibliographyTerminology?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/DSLBibliographyTerminology?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DSLBibliographyTerminology?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/DSLBibliographyTerminology?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DSLBibliographyTerminology?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DSLBibliographyTerminology)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DSLBibliographyTerminology?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/DSLBibliographyTerminology?template=oopsmore&param1=1.4&param2=1.4)
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
DSLBibliography Terminology {#dslbibliography-terminology .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

The [DSLAnnotatedBibliography](DSLAnnotatedBibliography){.twikiLink}
starts by definining the terminology used in the paper. This page
collects comments, extensions, or additional references concerning
[DomainSpecificLanguages](DomainSpecificLanguages){.twikiLink}
terminology.

------------------------------------------------------------------------

[KonstantinosTourlas[^?^](http://www.program-transformation.org/edit/Transform/KonstantinosTourlas?topicparent=Transform.DSLBibliographyTerminology)]{.twikiNewLink
style="background : #FFFFCE;"} reported on
[VisualLanguages](VisualLanguage){.twikiLink} (or *diagrammatic*
languages), well-known examples being [UML](UML){.twikiLink} or
[SDL](SDL){.twikiLink}.

He particularly mentions IEC 1131-3, a family of languages designed by
control engineers for developing programmable logic controller (PLC)
software. Two of the four languages in this standard are diagrammatic,
the diagrams being direct derivations from circuit-like and
Petri-net-like notations which existed in the domain long before the
introduction of programmable controllers.
[LabView[^?^](http://www.program-transformation.org/edit/Transform/LabView?topicparent=Transform.DSLBibliographyTerminology)]{.twikiNewLink
style="background : #FFFFCE;"}, geared towards domains in electronic
engineering, could be taken as a further example, as could be the
diagrammatic versions of Lustre and Signal.

All these languages enjoy widespread use in industry but have so far
attracted only very limited interest within computing. As far as IEC
1131-3 goes, known to few computer scientists interested in safety, the
focus is usually on applying formal methods around it rather than
studying it as a programming language per se.

As regards the relation of [DSLs](DSLs){.twikiLink} to end-user
programming, I believe Nardi\'s book, \"A small matter of
programming:perspectives on end-user computing\", which addresses
exactly this relation, to be of some interest to you. It is published by
MIT press.

\-- Excerpted from email by [ArieVanDeursen](ArieVanDeursen){.twikiLink}

------------------------------------------------------------------------

[KonstantinosTourlas[^?^](http://www.program-transformation.org/edit/Transform/KonstantinosTourlas?topicparent=Transform.DSLBibliographyTerminology)]{.twikiNewLink
style="background : #FFFFCE;"}\'s remarks made me realize that the
annual [IEEE](IEEE){.twikiLink}
[VisualLanguages](VisualLanguage){.twikiLink} Conferences could be
strongly related to
[DomainSpecificLanguages](DomainSpecificLanguages){.twikiLink}.

Susan Uskudarli while at the University Of Amsterdam worked in the area
of visual langauges: she has developed some techniques on specifying
visual grammars (visually) in order to derive parsers and editors. (see,
e.g., <http://citeseer.nj.nec.com/87050.html> ).

Most of her work was published in the [IEEE](IEEE){.twikiLink}
conferences on [VisualLanguages](VisualLanguage){.twikiLink}. We did not
refer to those conferences in our survey, which, in retrospect and after
reading your comments, strikes me as a bit odd.

\-- [ArieVanDeursen](ArieVanDeursen){.twikiLink}

------------------------------------------------------------------------

[CategoryDSL](CategoryDSL){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
