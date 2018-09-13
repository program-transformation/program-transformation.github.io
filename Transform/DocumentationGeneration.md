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
    Page](http://www.program-transformation.org/edit/Transform/DocumentationGeneration?t=1536825467)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DocumentationGeneration)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DocumentationGeneration)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DocumentationGeneration?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DocumentationGeneration?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/DocumentationGeneration?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/DocumentationGeneration?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/DocumentationGeneration?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DocumentationGeneration?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/DocumentationGeneration?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DocumentationGeneration?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DocumentationGeneration)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DocumentationGeneration?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/DocumentationGeneration?template=oopsmore&param1=1.4&param2=1.4)
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
Documentation Generation {#documentation-generation .twikiTopicTitle}
========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Deriving (on line) documentation from source code. The purpose is to
help maintainers or developers understand the system they are working
on.

The article
[BuildingDocumentationGenerators](BuildingDocumentationGenerators){.twikiLink}
lists four criteria that technical documentation should adhere to:

1.  Documentation should be available on different levels of
    abstraction.
2.  Documentation users must be able to move smoothly from one level of
    abstraction to another, without loosing their position in the
    documentation (zooming in or zooming out).
3.  The different levels of abstraction must be meaningful for the
    intended documentation users.
4.  The documentation needs to be consistent with the source code at all
    times.

Analyzing sources, finding different levels of abstraction through
[ReverseEngineering](ReverseEngineering){.twikiLink}, and presenting
these using graphs and hypertext is a way to get as close as possible to
meeting these criteria.

See also: [DocGen](DocGen){.twikiLink},
[RigiSystem](RigiSystem){.twikiLink},
[ArchitectureExtraction](ArchitectureExtraction){.twikiLink},
[NDoc](NDoc){.twikiLink},
[JavaDoc[^?^](http://www.program-transformation.org/edit/Transform/JavaDoc?topicparent=Transform.DocumentationGeneration)]{.twikiNewLink
style="background : #FFFFCE;"}, [Imagix 4D](ImagixFourD){.twikiLink}

------------------------------------------------------------------------

The University of Southern California has developed a tool called Media
Doc that generates software explanations to support
[ProgramUnderstanding](ProgramUnderstanding){.twikiLink}. The
explanations combine text, graphics and animation, and should replace
conventional documentation.

Media Doc views the process of explaining software as a series of
software inquiry-explanation cycles with Media Doc providing
explanations on demand to an engineer\'s inquiries. Explanations are
generated based on profiles of the user\'s tasks and expertise. The user
can pose a series of queries either by directly entering a query or by
interacting with Media Doc via the Task Model interface. Media Doc
either generates an explanation that directly answers the query, or
reformulates the query as a new subtask.

Answers to queries are generated from a library of dynamic templates
that combine text and graphics. These templates are authored in Media
Doc\'s presentation authoring language, and may include sections that
are automatically generated from code analysis tools and behavior
traces.

See <http://www.isi.edu/isd/media-doc/media-doc.html>

------------------------------------------------------------------------

[CategoryReverseEngineering](CategoryReverseEngineering){.twikiLink} \|
Contributors: [ArieVanDeursen](ArieVanDeursen){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
