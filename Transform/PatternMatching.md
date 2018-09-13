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
    Page](http://www.program-transformation.org/edit/Transform/PatternMatching?t=1536826532)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/PatternMatching)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/PatternMatching)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/PatternMatching?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/PatternMatching?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/PatternMatching?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/PatternMatching)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/PatternMatching?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/PatternMatching?template=oopsmore&param1=1.1&param2=1.1)
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
Pattern Matching {#pattern-matching .twikiTopicTitle}
================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Resources**

-   *Pattern Matching Pointers*:
    <http://www.cs.purdue.edu/homes/stelo/pattern.html>

**Definition**

Term pattern matching comes in many variations. The basic problem is
that of matching a term pattern (term with variables) against a ground
subject term (without variables), producing a substition mapping the
variables to the corresponding subterms in the subject term.

More often a subject term is matched against a set of patterns and the
matching pattern or patterns has to be found.

**Variations**

The matching problem problem comes in many different guises. The basic
problem considers matching a term at the root

-   match term against pattern

<!-- -->

-   match term against set of patterns; at most one pattern can match

<!-- -->

-   match term against set of patterns; more than one pattern can match

<!-- -->

-   match term against ordered sequence of patterns; find the first
    pattern in the sequence that matches

<!-- -->

-   for each subterm find out which pattern from a set of patterns
    matches it

Properties of the patterns

-   linear: variable occurs once in pattern

<!-- -->

-   [NonLinearPatternMatching[^?^](http://www.program-transformation.org/edit/Transform/NonLinearPatternMatching?topicparent=Transform.PatternMatching)]{.twikiNewLink
    style="background : #FFFFCE;"}: variable may occur mor than once

<!-- -->

-   [LazyPatternMatching[^?^](http://www.program-transformation.org/edit/Transform/LazyPatternMatching?topicparent=Transform.PatternMatching)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   [FirstOrderPatternMatching[^?^](http://www.program-transformation.org/edit/Transform/FirstOrderPatternMatching?topicparent=Transform.PatternMatching)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   [HigherOrderPatternMatching[^?^](http://www.program-transformation.org/edit/Transform/HigherOrderPatternMatching?topicparent=Transform.PatternMatching)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   [SecondOrderPatternMatching[^?^](http://www.program-transformation.org/edit/Transform/SecondOrderPatternMatching?topicparent=Transform.PatternMatching)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   [PatternMatchingModuloEquations[^?^](http://www.program-transformation.org/edit/Transform/PatternMatchingModuloEquations?topicparent=Transform.PatternMatching)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   [StrategicPatternMatching[^?^](http://www.program-transformation.org/edit/Transform/StrategicPatternMatching?topicparent=Transform.PatternMatching)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   [PatternMatchingAndAbstraction[^?^](http://www.program-transformation.org/edit/Transform/PatternMatchingAndAbstraction?topicparent=Transform.PatternMatching)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   [AdaptivePatternMatching](AdaptivePatternMatching){.twikiLink}

**Implementation**

Efficient implementations of pattern matching pre-process the pattern
into an efficient automaton that walks the subject tree only once.

**References**

Here are some references to papers on the subject:

-   aTermPatternMatchCompilerInspiredByFiniteAutomataTheory
-   [AdaptivePatternMatching](AdaptivePatternMatching){.twikiLink}
-   [ATypedPatternCalculus](ATypedPatternCalculus){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
