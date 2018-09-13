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
    Page](http://www.program-transformation.org/edit/Transform/DracoSystem?t=1536826286)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DracoSystem)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DracoSystem)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DracoSystem?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DracoSystem?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    9](http://www.program-transformation.org/view/Transform/DracoSystem?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Transform/DracoSystem?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Transform/DracoSystem?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Transform/DracoSystem?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Transform/DracoSystem?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/DracoSystem?rev1=1.7&rev2=1.6)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DracoSystem)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DracoSystem?template=oopsmore&param1=1.9&param2=1.9)
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
    \...](http://www.program-transformation.org/oops/Transform/DracoSystem?template=oopsmore&param1=1.9&param2=1.9)
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
Draco System {#draco-system .twikiTopicTitle}
============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

The Draco system was the first to pioneer with
[DomainSpecificLanguages](DomainSpecificLanguages){.twikiLink} employing
[ProgramTransformation](ProgramTransformation){.twikiLink} for their
implementation. The system featured parser and pretty-printer generation
and an interactive system for applying transformation rules and
refinements to programs.

The [DracoUsersManual](DracoUsersManual){.twikiLink} and
[JimNeighbors](JimNeighbors){.twikiLink} PhD thesis can be found at the
website of [BayfrontTechnologies](BayfrontTechnologies){.twikiLink}:
<http://www.bayfronttechnologies.com/l01tech.htm>

Draco is also discussed in Section 9.8.1 of
[GenerativeProgrammingBook](GenerativeProgrammingBook){.twikiLink}.

------------------------------------------------------------------------

**Strategies in Draco**

Draco was the first system to support the transformation of high-level
domain-specific programs to executable code. The system supported the
definition of transformation rules for optimizations and refinements to
transform high-level constructs into lower-level ones.

Transformation rules and refinements are identified by means of names.
Transformation rules also have an application code that specifies their
relative precedence. The application of transformations and refinements
to a domain program is controlled by the user through an interactive
process. In this process the user has to select domain, instance (region
in the abstract syntax tree representing the program), and locale (node
in the abstract syntax tree). Transformations can be applied directly to
the currently selected locale using APPLY. The system can examine the
tree and SUGGEST transformations to apply. Using the TRANSFORM command
all transformation rules in a certain range can be applied
automatically. The TRANSFORM uses a bottom-up traversal over the tree,
applying rules in the provided code range. Rules with higher codes are
applied first. In Neighbors PhD thesis there are also descriptions of a
top-down traversal and of traversals that apply the best rules first.
Refinements can be applied individually using TRY and USE. A certain
amount of automation of the process is possible by means of tactics.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 28 Apr 2001\

------------------------------------------------------------------------

[JimNeighbors](JimNeighbors){.twikiLink}\' Draco papers were also among
the first to describe the notion of
[DomainEngineering](DomainEngineering){.twikiLink} \-- see also

-   Section 2.8.3 of
    [GenerativeProgrammingBook](GenerativeProgrammingBook){.twikiLink}.
-   *The Draco approach to constructing software from reusable
    components*, [IEEE](IEEE){.twikiLink} Transactions on Software
    Engineering SE-10(5):564-574, 1984.

\-- [ArieVanDeursen](ArieVanDeursen){.twikiLink} - 10 May 2001\

------------------------------------------------------------------------

[CategorySystem](CategorySystem){.twikiLink} \| Contributions by
[EelcoVisser](../Main/EelcoVisser){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
