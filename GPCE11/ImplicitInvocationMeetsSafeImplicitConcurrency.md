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
    Page](http://www.program-transformation.org/edit/GPCE11/ImplicitInvocationMeetsSafeImplicitConcurrency?t=1536828818)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE11/ImplicitInvocationMeetsSafeImplicitConcurrency)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE11/ImplicitInvocationMeetsSafeImplicitConcurrency)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE11/ImplicitInvocationMeetsSafeImplicitConcurrency?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE11/ImplicitInvocationMeetsSafeImplicitConcurrency?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/GPCE11/ImplicitInvocationMeetsSafeImplicitConcurrency?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE11/ImplicitInvocationMeetsSafeImplicitConcurrency)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE11/ImplicitInvocationMeetsSafeImplicitConcurrency?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/GPCE11/ImplicitInvocationMeetsSafeImplicitConcurrency?template=oopsmore&param1=1.1&param2=1.1)
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
Implicit Invocation Meets Safe, Implicit Concurrency {#implicit-invocation-meets-safe-implicit-concurrency .twikiTopicTitle}
====================================================

::: {.twikiWebTitle}
Yuheng Long , Sean Mooney, Tyler Sondag and Hridesh Rajan
:::

**Abstract**: Writing correct and efficient concurrent programs still
remains a challenge. Explicit concurrency is difficult, error prone, and
creates code which is hard to maintain and debug. This type of
concurrency also treats modular program design and concurrency as
separate goals, where modularity often suffers.

To solve these problems, we are designing a new language that we call
Panini. In this paper, we focus on Panini\'s asynchronous, typed events,
which reconcile the modularity goal promoted by the implicit invocation
design style with the concurrency goal of exposing potential concurrency
between the execution of subjects and observers.

Since modularity is improved and concurrency is implicit in Panini,
programs are easier to reason about and maintain. Furthermore, races and
deadlocks are avoided entirely, yielding programs with a guaranteed
sequential semantics.

To evaluate our language design and implementation we show several
examples of its usage as well as an empirical study of program
performance.

We found that not only is developing and understanding Panini programs
significantly easier compared to standard concurrent object-oriented
programs, but performance of Panini programs is also comparable to their
equivalent hand-tuned versions written using Java\'s fork-join
framework.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
