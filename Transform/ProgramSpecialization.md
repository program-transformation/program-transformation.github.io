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
    Page](http://www.program-transformation.org/edit/Transform/ProgramSpecialization?t=1536825741)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ProgramSpecialization)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ProgramSpecialization)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ProgramSpecialization?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ProgramSpecialization?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/ProgramSpecialization?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/ProgramSpecialization?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/ProgramSpecialization?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ProgramSpecialization)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ProgramSpecialization?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/ProgramSpecialization?template=oopsmore&param1=1.2&param2=1.2)
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
Program Specialization {#program-specialization .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[ProgramSpecialization](ProgramSpecialization){.twikiLink} is used where
a variable is known to often hold one particular value. In this case, it
is possible to generate code taking advantage of this constant value,
e.g. not passing a parameter, using immediate addressing modes,
eliminating the evaulation of an if-then-else statement and one of the
clauses, (either the *then* or *else* clauses) etc. For example, if you
have code like

      if (extendedBehavior)
        doExtended();
      else
        x = 11;

and extendedBehavior is often false, then you can *specialize* the above
code to just \"x=11;\". Usually, the assumption can\'t be proved (e.g.
that extendedBehavior is false), so the specialized code has to be
protected by a guard, which essentially says \"if extendedBehavior is
true, branch to the non specialized code; else branch to the specialized
code\".

Under appropriate circumstances, the performance gain from
specialization can be quite considerable.

See also [PartialEvaluation](PartialEvaluation){.twikiLink},
[ProgramSpecialization](ProgramSpecialization){.twikiLink} (a synonym
for [PartialEvaluation](PartialEvaluation){.twikiLink}).

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 03 Dec 2001\

(Specialization is not a [WikiName](../TWiki/WikiName){.twikiLink};
renamed the topic to
[ProgramSpecialization](ProgramSpecialization){.twikiLink} \--
[EelcoVisser](../Main/EelcoVisser){.twikiLink} - 04 Dec 2001)

------------------------------------------------------------------------

[CategoryOptimization](CategoryOptimization){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.ProgramSpecialization moved from Transform.Specialization on
04 Dec 2001 - 10:50 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}* -
[put it
back](http://www.program-transformation.org/rename/Transform/ProgramSpecialization?newweb=Transform&newtopic=Specialization&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
