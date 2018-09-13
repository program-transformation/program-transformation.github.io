::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![gpce-logo.jpg](../pub/GPCE12/WebLeftBar/gpce-logo.jpg){width="100"
height="120"}

**[GPCE Home](http://program-transformation.org/Gpce)**\
**[GPCE\'12 Home](WebHome){.twikiLink}**\
**[GPCE\'13 Home](http://program-transformation.org/GPCE13/WebHome)**\

[Program](ConferenceProgram){.twikiLink}\
[Registration](GpceRegistration){.twikiLink}\
[Venue and Accommodation](VenueAccomodation){.twikiLink}\
[Organization](ConferenceOrganization){.twikiLink}\
[Dates](ImportantDates){.twikiLink}

**Calls for**\
[Papers](CallForPapers){.twikiLink}\
[Tech Talks](CallForTechTalks){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/GPCE12/Tutorial1ProjectFortress?t=1536828834)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE12/Tutorial1ProjectFortress)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE12/Tutorial1ProjectFortress)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE12/Tutorial1ProjectFortress?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE12/Tutorial1ProjectFortress?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/GPCE12/Tutorial1ProjectFortress?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/GPCE12/Tutorial1ProjectFortress?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/GPCE12/Tutorial1ProjectFortress?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/GPCE12/Tutorial1ProjectFortress?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/GPCE12/Tutorial1ProjectFortress?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE12/Tutorial1ProjectFortress)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE12/Tutorial1ProjectFortress?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/GPCE12/Tutorial1ProjectFortress?template=oopsmore&param1=1.3&param2=1.3)
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
Tutorial 1 {#tutorial-1 .twikiTopicTitle}
==========

::: {.twikiWebTitle}
Generative Programming and Component Engineering
:::

### []{#Project_Fortress_A_Growable_Lang} Project Fortress: A Growable Language for Scientists and Engineers

##### []{#http_plrg_kaist_ac_kr_ryu_Sukyou}[]{#_http_plrg_kaist_ac_kr_ryu_Sukyo} [Sukyoung Ryu](http://plrg.kaist.ac.kr/ryu)

###### []{#Abstract} Abstract

We can think of a programming language as a vocabulary of words and a
set of rules that deﬁne how to combine words into meaningful constructs.
Creating a vocabulary and a set of rules that allow programmers to
express their ideas clearly and concisely is one of the main goals of
language design. However, it is diﬃcult to anticipate the vocabulary and
the set of rules that are suitable for solving various problems. It
often depends on domain-speciﬁc applications, new hardware platforms,
and any unexpected feature requests. Therefore, a language should grow
over time to accommodate the changing needs of its users.

Fortress is a new programming language designed for growth by community
instead of a single core team. It provides mathematical syntax to enable
scientists and engineers to write programs in a notation they are
accustomed to. It also provides built-in support for parallel
programming. Moreover, its macro system allows for the language growth
by extending the syntax and semantics of Fortress.

In designing Fortress, we have adopted the following design strategy:
"Whenever possible, implement a proposed language feature in a library
rather than building it into the compiler." For this approach to work,
library writers must have substantial ﬂexibility and control over both
syntax and semantics. By designing the language for growth, we are
designing it for community participation and development. Hence, we have
made Project Fortress open source, and are collaborating on its
development with many groups and individuals all over the world.

Please come take it for a spin, or pitch in and help us grow!

###### []{#Author_biography} Author biography

[Sukyoung Ryu](http://plrg.kaist.ac.kr/ryu) is an Assistant Professor at
the Computer Science Department of KAIST (Korea Advanced Institute of
Science and Technology). Before joining KAIST in December 2009, she
worked as a Member of Technical Staﬀ in Sun Microsystems Laboratories,
where she worked on formally designing and developing the Fortress
programming language. Before that, she was a Research Associate in
Computer Science at Harvard, where she worked on the Debugging
Everywhere project. She received her Ph.D. (2001), M.S. (1996), and B.S.
(1995), in Computer Science from KAIST. Her most recent research focuses
on developing language features that are both useful in practice and
proven to be sound. She led the effort to construct the core calculi of
the Fortress language, to improve the Fortress prose speciﬁcation, and
to build a full-ﬂedged parser for Fortress that runs entirely on the
JVM.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
