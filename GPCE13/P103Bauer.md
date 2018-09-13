::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![gpce-logo.jpg](../pub/GPCE13/WebLeftBar/gpce-logo.jpg){width="100"
height="120"}

**[GPCE Home](http://program-transformation.org/Gpce)**\
**[GPCE\'13 Home](WebHome){.twikiLink}**\
\
[Keynotes](KeynoteSpeakers){.twikiLink}\
*[Programm](ConferenceProgram){.twikiLink}*\
[Registration](GpceRegistration){.twikiLink}\
\
[Organization](ConferenceOrganization){.twikiLink}\
[Dates](ImportantDates){.twikiLink}\
[GPCE Poster](Poster){.twikiLink}\
[GPCE Button](Banner){.twikiLink}\

[Venue](ConferenceVenue){.twikiLink}\
[Grants](Grants){.twikiLink}\
[Call for Papers](CallForPapers){.twikiLink}\
[Tech Talks](CallForTechTalks){.twikiLink}\
\
[FOSD Workshop](http://fosd.net/2013)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/GPCE13/P103Bauer?t=1536828841)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE13/P103Bauer)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE13/P103Bauer)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE13/P103Bauer?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE13/P103Bauer?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/GPCE13/P103Bauer?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE13/P103Bauer)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE13/P103Bauer?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/GPCE13/P103Bauer?template=oopsmore&param1=1.1&param2=1.1)
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
Faster Program Adaptation Through Reward Attribution Inference {#faster-program-adaptation-through-reward-attribution-inference .twikiTopicTitle}
==============================================================

::: {.twikiWebTitle}
Tim Bauer, Martin Erwig, Alan Fern, and Jervis Pinto
:::

In the adaptation-based programming (ABP) paradigm, programs may contain
variable parts (function calls, parameter values, etc.) that can be take
a number of different values. Programs also contain reward statements
with which a programmer can provide feedback about how well a program is
performing with respect to achieving its goals (for example, achieving a
high score on some scale). By repeatedly running the program, a machine
learning component will, guided by the rewards, gradually adjust the
automatic choices made in the variable program parts so that they
converge toward an optimal strategy.

ABP is a method for semi-automatic program generation in which the
choices and rewards offered by programmers allow standard
machine-learning techniques to explore a design space defined by the
programmer to find an optimal instance of a program template. ABP
effectively provides a DSL that allows non-machine-learning experts to
exploit machine learning to generate self-optimizing programs.

Unfortunately, in many cases the placement and structuring of choices
and rewards can have a detrimental effect on how an optimal solution to
a program-generation problem can be found. To address this problem, we
have developed a dataflow analysis that computes influence tracks of
choices and rewards. This information can be exploited by an augmented
machine-learning technique to ignore misleading rewards and to generally
attribute rewards better to the choices that have actually influenced
them. Moreover, this technique allows us to detect errors in the
adaptive program that might arise out of program maintenance. Our
evaluation shows that the dataflow analysis can lead to improvements in
performance.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
