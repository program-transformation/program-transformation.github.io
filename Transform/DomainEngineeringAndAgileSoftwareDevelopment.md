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
    Page](http://www.program-transformation.org/edit/Transform/DomainEngineeringAndAgileSoftwareDevelopment?t=1536826302)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DomainEngineeringAndAgileSoftwareDevelopment)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DomainEngineeringAndAgileSoftwareDevelopment)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DomainEngineeringAndAgileSoftwareDevelopment?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DomainEngineeringAndAgileSoftwareDevelopment?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/DomainEngineeringAndAgileSoftwareDevelopment?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DomainEngineeringAndAgileSoftwareDevelopment?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/DomainEngineeringAndAgileSoftwareDevelopment?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DomainEngineeringAndAgileSoftwareDevelopment?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DomainEngineeringAndAgileSoftwareDevelopment?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DomainEngineeringAndAgileSoftwareDevelopment)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DomainEngineeringAndAgileSoftwareDevelopment?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/DomainEngineeringAndAgileSoftwareDevelopment?template=oopsmore&param1=1.3&param2=1.3)
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
Domain Engineering And Agile Software Development {#domain-engineering-and-agile-software-development .twikiTopicTitle}
=================================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

This page is intended to discuss the question

***Is Domain Engineering compatible with Agile Software Development?***

Given the current popularity of agile methodologies in the general
software development community it is worthwhile to position
[DomainEngineering](DomainEngineering){.twikiLink} appropriately in
order to avoid being dismissed as an unworkable, high-ceremony approach.
Highly automated software development and the principles of the agile
alliance don\'t have to be exclusice. In practice I found that using
model-driven generators naturally leads to agile
[ApplicationEngineering[^?^](http://www.program-transformation.org/edit/Transform/ApplicationEngineering?topicparent=Transform.DomainEngineeringAndAgileSoftwareDevelopment)]{.twikiNewLink
style="background : #FFFFCE;"}, opening up possibilities of domain
exploration to application engineers that would be completely
impractical in traditional, manually driven software development. Using
advanced model-driven generators allows to react to most user
requirements changes within hours and days rather than weeks or months,
allows to shorten iteration times, and speeds up the user feedback
cycle.

The mainstream attitude to generation is reflected in the otherwise
excellent book
[SurvivingObjectOrientedProjects[^?^](http://www.program-transformation.org/edit/Transform/SurvivingObjectOrientedProjects?topicparent=Transform.DomainEngineeringAndAgileSoftwareDevelopment)]{.twikiNewLink
style="background : #FFFFCE;"} by
[AlistairCockburn[^?^](http://www.program-transformation.org/edit/Transform/AlistairCockburn?topicparent=Transform.DomainEngineeringAndAgileSoftwareDevelopment)]{.twikiNewLink
style="background : #FFFFCE;"}:

*\... my colleages and I estimated that perhaps 5 percent of the total
system code could have been generated from the business object model.
\... The problem comes when you must add some computation that cannot be
generated automatically. At that moment, the drawing of the object
model, which moments before was an asset, becomes a liability \...*

In short, the state-of-the-art of generative techniques is often judged
by what is provided in the better known [UML](UML){.twikiLink} tools
such as Rose, Together, and others. Needless to say that this makes it
harder to convince traditional development teams that there is something
to be gained by [DomainEngineering](DomainEngineering){.twikiLink} and
domain-specific techniques. To counter the simplistic arguments against
generative techniques I have compared manual development,
\"traditional\" development with a [UML](UML){.twikiLink} tool, and
model-driven development with a modern generator in
<http://www.softmetaware.com/mda-implementationandmetrics.pdf>. The
comparison concentrates on the gains achievable by generation, and
consciously relies largely on [UML](UML){.twikiLink}-based notations,
with only a few domain-specific elements.

[DomainEngineering](DomainEngineering){.twikiLink} leads to agile
[ApplicationEngineering[^?^](http://www.program-transformation.org/edit/Transform/ApplicationEngineering?topicparent=Transform.DomainEngineeringAndAgileSoftwareDevelopment)]{.twikiNewLink
style="background : #FFFFCE;"}, but what about
[DomainEngineering](DomainEngineering){.twikiLink} itself? Does it make
sense to talk about agile
[DomainEngineering](DomainEngineering){.twikiLink}?

[JornBettin](JornBettin){.twikiLink}

------------------------------------------------------------------------

Agile [DomainEngineering](DomainEngineering){.twikiLink} requires a lot
of flexibility from the tools that are used to build generators. I am
aware of a few papers that address this issue, albeit in different
terminology:

-   [LittleLanguagesLittleMaintenance](LittleLanguagesLittleMaintenance){.twikiLink}
-   [CostEffectiveMaintenanceToolsForProprietaryLanguages](CostEffectiveMaintenanceToolsForProprietaryLanguages){.twikiLink}

[JoostVisser](JoostVisser){.twikiLink}

------------------------------------------------------------------------

In my feeling, [DomainEngineering](DomainEngineering){.twikiLink} has a
strong big-design-upfront feeling, which is at odds with, e.g.,
[ExtremeProgramming](ExtremeProgramming){.twikiLink}. Discussing this
with Howard Goodell, we also observed that

-   The explicit customer involvement of agile methods feels like a good
    combination with end-user programming as made possible by
    [DomainSpecificLanguages](DomainSpecificLanguages){.twikiLink}
-   XP talks about letting end-users do acceptance testing via a
    [DomainSpecificLanguage](DomainSpecificLanguage){.twikiLink}

\-- [ArieVanDeursen](ArieVanDeursen){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
