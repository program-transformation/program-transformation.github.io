::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[Home](WebHome){.twikiLink}**\
[News](WebNews){.twikiLink}\
[Recent Changes](WebChanges){.twikiLink}

[WebContents[^?^](http://www.program-transformation.org/edit/Variability/WebContents?topicparent=Variability.MVCDC2004MappingOfDomainSpaceToSolutionSpace)]{.twikiNewLink
style="background : #FFFFCE;"}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Variability/MVCDC2004MappingOfDomainSpaceToSolutionSpace?t=1536829015)
-   [Rename
    Page](http://www.program-transformation.org/rename/Variability/MVCDC2004MappingOfDomainSpaceToSolutionSpace)
-   [Attach
    File](http://www.program-transformation.org/attach/Variability/MVCDC2004MappingOfDomainSpaceToSolutionSpace)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Variability/MVCDC2004MappingOfDomainSpaceToSolutionSpace?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Variability/MVCDC2004MappingOfDomainSpaceToSolutionSpace?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Variability/MVCDC2004MappingOfDomainSpaceToSolutionSpace?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Variability/MVCDC2004MappingOfDomainSpaceToSolutionSpace)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Variability/MVCDC2004MappingOfDomainSpaceToSolutionSpace?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Variability/MVCDC2004MappingOfDomainSpaceToSolutionSpace?template=oopsmore&param1=1.1&param2=1.1)
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
MVCDC2004 Mapping Of Domain Space To Solution Space {#mvcdc2004-mapping-of-domain-space-to-solution-space .twikiTopicTitle}
===================================================

::: {.twikiWebTitle}
\*Software Variability Management\*
:::

For now we have only the raw discussion protocol here.

### []{#Type_and_Mechanism_of_Variation} Type and Mechanism of Variation

solution vs. problem space

types of variation in problem space:

offerted by feature models: optional mandatory alternatives set
selection

other dimension features that go into code into process into

in general: everything that can be decided on

features lack semantics

types of variation in the solution space = Operations: substitutive
variation (replace) additive variation remove

other dimension: functionality and non functional things

mechanisms for variation in solution space: ifdef aspects templates \...

We want to have: Patterns for doing variations

If you have this kind of variation with this kind of feature and are
restricted to this set of mechanisms implement it like this.

[]{#Semantic_Interfaces} Semantic Interfaces
--------------------------------------------

exposing variation points

[]{#On_Demand_Variation} On Demand Variation
--------------------------------------------

runtime variation on demand requirments changed during runtime (for high
availability systems) change the code during runtime, not only
configurate it

ways to do this: AO : offers runtime weaving/hot deployment flexible
component systems: replace, add, remove components patching at runtim
\...

what is missing?

same problem as evolution

[]{#Crosscutting_Feature_Models} Crosscutting Feature Models
------------------------------------------------------------

mapping several feature models on each other? crosscutting feature over
one feature model?

[]{#Valid_Variations_in_Problem_Solu} Valid Variations in Problem/Solution space
--------------------------------------------------------------------------------

\-- [DaniloBeuche](../Main/DaniloBeuche){.twikiLink} - 10 Nov 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
