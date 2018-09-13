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
    Page](http://www.program-transformation.org/edit/GPCE11/ReflectioninDirectStyle?t=1536828809)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE11/ReflectioninDirectStyle)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE11/ReflectioninDirectStyle)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE11/ReflectioninDirectStyle?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE11/ReflectioninDirectStyle?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/GPCE11/ReflectioninDirectStyle?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE11/ReflectioninDirectStyle)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE11/ReflectioninDirectStyle?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/GPCE11/ReflectioninDirectStyle?template=oopsmore&param1=1.1&param2=1.1)
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
Reflection in Direct Style {#reflection-in-direct-style .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Kenichi Asai
:::

**Abstract**:

A reﬂective language enables us to access, inspect, and/or modify the
language semantics from within the same language framework. Although the
degree of semantics exposure differs from one language to another, the
most powerful approach, referred to as the behavioral reﬂection, exposes
the entire language semantics (or the language interpreter) that deﬁnes
behavior of user programs for user inspection/modiﬁcation. In this
paper, we deal with the behavioral reﬂection in the context of a
functional language Scheme. In particular, we show how to construct a
reﬂective interpreter where user programs are interpreted by the tower
of metacircular interpreters and have the ability to change any parts of
the interpreters during execution. Its distinctive feature compared to
the previous work is that the metalevel interpreters observed by users
are written in direct style. Based on the past attempt of the present
author, the current work solves the level-shifting anomaly by
defunctionalizing and inspecting the top of the continuation frames. The
resulting system enables us to freely go up and down the levels and
access/modify the direct-style metalevel interpreter. This is in
contrast to the previous system where metalevel interpreters were
written in continuation-passing style (CPS) and only CPS functions could
be exposed to users for modiﬁcation.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
