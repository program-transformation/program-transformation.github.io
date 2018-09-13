::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![gpce-logo.jpg](../pub/GPCE11/WebLeftBar/gpce-logo.jpg){width="100"
height="120"}

**[GPCE Home](http://program-transformation.org/Gpce)**\
**[GPCE\'11 Home](WebHome){.twikiLink}**\
[Keynotes](KeynoteSpeakers){.twikiLink}\
[Schedule](ConferenceProgram){.twikiLink}\
[Accepted Papers](AcceptedPapers){.twikiLink}\
[Tech Talks](TechTalks){.twikiLink}\
[Poster](Poster){.twikiLink}\
[Banner](Banner){.twikiLink}\
[Organization](ConferenceOrganization){.twikiLink}\
[Dates](ImportantDates){.twikiLink}\
[Venue](ConferenceVenue){.twikiLink}\
[Registration](ConferenceRegistration){.twikiLink}\

**Calls for**\
[Papers](CallForPapers){.twikiLink}\
[Tech Talks](CallForTechTalks){.twikiLink}\
[Workshops](Workshops){.twikiLink}

**[Electronic\
Submission](http://www.easychair.org/conferences/?conf=gpce11)**\
(Submission deadline has passed)\
\
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/GPCE11/IncrementalType-CheckingForType-ReflectiveMetaprograms?t=1536828814)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE11/IncrementalType-CheckingForType-ReflectiveMetaprograms)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE11/IncrementalType-CheckingForType-ReflectiveMetaprograms)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE11/IncrementalType-CheckingForType-ReflectiveMetaprograms?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE11/IncrementalType-CheckingForType-ReflectiveMetaprograms?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/GPCE11/IncrementalType-CheckingForType-ReflectiveMetaprograms?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE11/IncrementalType-CheckingForType-ReflectiveMetaprograms)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE11/IncrementalType-CheckingForType-ReflectiveMetaprograms?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/GPCE11/IncrementalType-CheckingForType-ReflectiveMetaprograms?template=oopsmore&param1=1.1&param2=1.1)
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
Incremental Type-Checking for Type-Reflective Metaprograms {#incremental-type-checking-for-type-reflective-metaprograms .twikiTopicTitle}
==========================================================

::: {.twikiWebTitle}
Weiyu Miao and Jeremy Siek
:::

**Abstract**: Garcia introduces a calculus for type-reflective
metaprogramming that provides much of the power and flexibility of C++
templates and solves many of its problems. However, one of the problems
that remains is that the residual program is not type checked until
after meta computation is complete. Ideally, one would like the type
system of the metaprogram to also guarantee that the residual program
will type check, as is the case in MetaML. However, in a language with
type-reflective metaprogramming, type expressions in the residual
program may be the result of meta computation, making the MetaML
guarantee next to impossible to achieve.

In this paper we offer an approach to detecting errors earlier without
sacrificing flexibility: we incrementally type check code fragments as
they are created and spliced together during meta computation. The
incremental type system is a variant of the gradual type system of Siek
and Taha, in which we use type variables to represent type expressions
that are not yet normalized and a new dynamic variation on existential
types to represent residual code fragments. A type error in a code
fragment is treated as a run-time error of the meta computation. We show
that the incremental type checker can be implemented efficiently and we
prove that if a well-typed metaprogram generates a residual program,
then the residual program is also well-typed.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
