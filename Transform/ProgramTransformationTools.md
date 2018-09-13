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
    Page](http://www.program-transformation.org/edit/Transform/ProgramTransformationTools?t=1536826538)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ProgramTransformationTools)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ProgramTransformationTools)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ProgramTransformationTools?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ProgramTransformationTools?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/ProgramTransformationTools?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ProgramTransformationTools)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ProgramTransformationTools?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/ProgramTransformationTools?template=oopsmore&param1=1.1&param2=1.1)
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
Program Transformation Tools {#program-transformation-tools .twikiTopicTitle}
============================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Description**

This page discusses terminology, principles, and issues concerning tools
for [ProgramTransformation](ProgramTransformation){.twikiLink}.

**Principles**

[ProgramTransformationTools](ProgramTransformationTools){.twikiLink}
have much in common. Here is a list of features that are supported by
all or some tools:

-   [TransformationRules](TransformationRules){.twikiLink}
-   [TransformationStrategies](TransformationStrategies){.twikiLink}
-   [TreeTraversals[^?^](http://www.program-transformation.org/edit/Transform/TreeTraversals?topicparent=Transform.ProgramTransformationTools)]{.twikiNewLink
    style="background : #FFFFCE;"}

**Components**

A
[ProgramTransformationSystem[^?^](http://www.program-transformation.org/edit/Transform/ProgramTransformationSystem?topicparent=Transform.ProgramTransformationTools)]{.twikiNewLink
style="background : #FFFFCE;"} is usually composed of a number of
components. Typical components are

-   [ProgramParser[^?^](http://www.program-transformation.org/edit/Transform/ProgramParser?topicparent=Transform.ProgramTransformationTools)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [PrettyPrinter[^?^](http://www.program-transformation.org/edit/Transform/PrettyPrinter?topicparent=Transform.ProgramTransformationTools)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [ProgramTransformer[^?^](http://www.program-transformation.org/edit/Transform/ProgramTransformer?topicparent=Transform.ProgramTransformationTools)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [ProgramAnalyzer[^?^](http://www.program-transformation.org/edit/Transform/ProgramAnalyzer?topicparent=Transform.ProgramTransformationTools)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [FormatChecker[^?^](http://www.program-transformation.org/edit/Transform/FormatChecker?topicparent=Transform.ProgramTransformationTools)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [ProgramTypeChecker[^?^](http://www.program-transformation.org/edit/Transform/ProgramTypeChecker?topicparent=Transform.ProgramTransformationTools)]{.twikiNewLink
    style="background : #FFFFCE;"}

A collection of such components for a language is called a
[TransformationFramework](TransformationFramework){.twikiLink}.

**Issues**

-   [ProgramRepresentation](ProgramRepresentation){.twikiLink}
-   [VariableBinding[^?^](http://www.program-transformation.org/edit/Transform/VariableBinding?topicparent=Transform.ProgramTransformationTools)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [ToolInterface[^?^](http://www.program-transformation.org/edit/Transform/ToolInterface?topicparent=Transform.ProgramTransformationTools)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [ToolComposition[^?^](http://www.program-transformation.org/edit/Transform/ToolComposition?topicparent=Transform.ProgramTransformationTools)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [ExchangeFormats](ExchangeFormat){.twikiLink}

**See also**

-   [TransformationSystems](TransformationSystems){.twikiLink}: a list
    of tools for program transformation
-   XT: a bundle of
    [ProgramTransformationTools](ProgramTransformationTools){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
