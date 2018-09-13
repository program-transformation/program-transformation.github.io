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
    Page](http://www.program-transformation.org/edit/Transform/RealisticCompilationByProgramTransformation?t=1536826541)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/RealisticCompilationByProgramTransformation)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/RealisticCompilationByProgramTransformation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/RealisticCompilationByProgramTransformation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/RealisticCompilationByProgramTransformation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/RealisticCompilationByProgramTransformation?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/RealisticCompilationByProgramTransformation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/RealisticCompilationByProgramTransformation?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/RealisticCompilationByProgramTransformation?template=oopsmore&param1=1.1&param2=1.1)
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
Realistic Compilation By Program Transformation {#realistic-compilation-by-program-transformation .twikiTopicTitle}
===============================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

by
[RichardKelsey[^?^](http://www.program-transformation.org/edit/Transform/RichardKelsey?topicparent=Transform.RealisticCompilationByProgramTransformation)]{.twikiNewLink
style="background : #FFFFCE;"} and
[PaulHudak[^?^](http://www.program-transformation.org/edit/Transform/PaulHudak?topicparent=Transform.RealisticCompilationByProgramTransformation)]{.twikiNewLink
style="background : #FFFFCE;"}

*Conference Record of the Sixteenth Annual [ACM](ACM){.twikiLink}
Symposium on Principles of Programming Languages
([POPL](POPL){.twikiLink}\'89)*. 281\--292, 1989,
<http://citeseer.nj.nec.com/kelsey89realistic.html>

------------------------------------------------------------------------

**Summary**

The paper describes the process of compiling high-level programs to
machine language programs by means of a chain of simple program
transformations. A high-level program is first translated into an
intermediate language, the call-by-value lambda calculus with an
implicit store. An intermediate language program is then simplified
during several stages. The end result is an intermediate language
program that can be interpreted as a machine language program.

The stages of compilation are

-   Making the program linear: each subexpression is given an explicit
    name

<!-- -->

-   Adding explicit continuations: functions are transformed to
    [ContinuationPassingStyle[^?^](http://www.program-transformation.org/edit/Transform/ContinuationPassingStyle?topicparent=Transform.RealisticCompilationByProgramTransformation)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   Simplifying the program: local transformations such as
    [BetaReduction[^?^](http://www.program-transformation.org/edit/Transform/BetaReduction?topicparent=Transform.RealisticCompilationByProgramTransformation)]{.twikiNewLink
    style="background : #FFFFCE;"} and global transformations such as
    [ConstantPropagation[^?^](http://www.program-transformation.org/edit/Transform/ConstantPropagation?topicparent=Transform.RealisticCompilationByProgramTransformation)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   Adding explicit environments: free variables are turned into bound
    variables that are passed around explicitly

<!-- -->

-   Identifier renaming /
    [RegisterAllocation[^?^](http://www.program-transformation.org/edit/Transform/RegisterAllocation?topicparent=Transform.RealisticCompilationByProgramTransformation)]{.twikiNewLink
    style="background : #FFFFCE;"}: the set of variables used to name
    expressions are reduced to match the set of machine registers.

------------------------------------------------------------------------

[CategoryReview](CategoryReview){.twikiLink},
[CategoryTransformation](CategoryTransformation){.twikiLink} \| \--
[EelcoVisser](../Main/EelcoVisser){.twikiLink} - 04 Jun 2001\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
