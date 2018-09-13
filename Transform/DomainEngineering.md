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
    Page](http://www.program-transformation.org/edit/Transform/DomainEngineering?t=1536825728)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DomainEngineering)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DomainEngineering)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DomainEngineering?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DomainEngineering?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    17](http://www.program-transformation.org/view/Transform/DomainEngineering?rev=1.17)
    [(diff 16)](http://www.program-transformation.org/rdiff/Transform/DomainEngineering?rev1=1.17&rev2=1.16)
-   [Rev
    16](http://www.program-transformation.org/view/Transform/DomainEngineering?rev=1.16)
    [(diff 15)](http://www.program-transformation.org/rdiff/Transform/DomainEngineering?rev1=1.16&rev2=1.15)
-   [Rev
    15](http://www.program-transformation.org/view/Transform/DomainEngineering?rev=1.15)
    [(diff 14)](http://www.program-transformation.org/rdiff/Transform/DomainEngineering?rev1=1.15&rev2=1.14)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DomainEngineering)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DomainEngineering?template=oopsmore&param1=1.17&param2=1.17)
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
    \...](http://www.program-transformation.org/oops/Transform/DomainEngineering?template=oopsmore&param1=1.17&param2=1.17)
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
Domain Engineering {#domain-engineering .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Domain Engineering involves creating a set of reusable assets for
building systems in a particular problem domain. These reusable assets
are then assembled to customer-specific systems in the complementary
*application engineering* phase.

Domain engineering originates from research in
[SoftwareReuse](SoftwareReuse){.twikiLink}. The activities of domain
engineering play a role in the design of

-   [DomainSpecificLanguages](DomainSpecificLanguages){.twikiLink}
-   [SoftwareProductLines](SoftwareProductLine){.twikiLink}

------------------------------------------------------------------------

Chapters 2-5 of
[GenerativeProgrammingBook](GenerativeProgrammingBook){.twikiLink} cover
domain engineering in considerable detail. They define it as the
activity of

-   collecting, organizing and storing past experience in building
    systems or parts of system in a particular domain in the form of
    reusable assets (i.e., reusable work products),
-   as well as providing an adequate means for reusing these assets
    (i.e., retrieval, qualification, dissemination, adaptation,
    assembly, and so on) when building new systems.

They consider the notion of a [FeatureModel](FeatureModel){.twikiLink},
resulting from the [DomainAnalysis](DomainAnalysis){.twikiLink} phase,
the most important contribution of domain engineering.

An earlier version of the generative programming survey on domain
engineering is available from
[KrzysztofCzarnecki](KrzysztofCzarnecki){.twikiLink}\'s home page.

------------------------------------------------------------------------

Observe the emphasis in the above definition on *past experience*,
making [ReverseEngineering](ReverseEngineering){.twikiLink} an important
element of [DomainEngineering](DomainEngineering){.twikiLink}. \--
[ArieVanDeursen](ArieVanDeursen){.twikiLink}.

------------------------------------------------------------------------

The [SEI](SEI){.twikiLink} describes domain engineering as

-   *a process for creating a competence in application engineering for
    a family of similar systems. Domain engineering covers all the
    activities for building software core assets. These activities
    include identifying one or more domains, capturing the variation
    within a domain ([DomainAnalysis](DomainAnalysis){.twikiLink}),
    constructing an adaptable design
    ([DomainDesign](DomainDesign){.twikiLink}), and defining the
    mechanisms for translating requirements into systems created from
    reusable components (Domain Implementation). The products (or
    software assets) of these activities are domain model(s), design
    model(s),
    [DomainSpecificLanguages](DomainSpecificLanguages){.twikiLink}, code
    generators, and code components.*

See <http://www.sei.cmu.edu/domain-engineering/domain_engineering.html>

------------------------------------------------------------------------

There is an on line bibliography of domain engineering resources at
<http://liinwww.ira.uka.de/bibliography/SE/domain.html>

------------------------------------------------------------------------

Several domain engineering methodologies have been published. See, for
example,

-   The [DracoSystem](DracoSystem){.twikiLink}
-   [OrganizationDomainModeling](OrganizationDomainModeling){.twikiLink}
-   [FeatureOrientedDomainAnalysis](FeatureOrientedDomainAnalysis){.twikiLink}

------------------------------------------------------------------------

[CategoryDomainEngineering](CategoryDomainEngineering){.twikiLink} \|
[CategoryEntryPoint](CategoryEntryPoint){.twikiLink} \|
[CategoryArchitecture](CategoryArchitecture){.twikiLink} \|
Contributions by [ArieVanDeursen](ArieVanDeursen){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
