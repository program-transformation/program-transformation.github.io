::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![gpce-logo.jpg](../pub/GPCE08/WebLeftBar/gpce-logo.jpg){width="100"
height="120"}

**[GPCE Home](http://www.gpce.org/)**\
**[GPCE\'08 Home](WebHome){.twikiLink}**\
[Program](ConferenceProgram){.twikiLink}\
[Organization](ConferenceOrganization){.twikiLink}\
[Dates](ImportantDates){.twikiLink}\
[Venue](ConferenceVenue){.twikiLink}\
[Registration](ConferenceRegistration){.twikiLink}

**[Tutorials](GpceTutorials){.twikiLink}**\
[GP1: MDE Systems](MdeTutorial){.twikiLink}\
[GP2: S. Jarzabek](PowerGenericsTutorial){.twikiLink}\
[GP3: W. Taha](MultiStageProgrammingTutorial){.twikiLink}

**[Workshops](GpceWorkshops){.twikiLink}**\
[DSPD 2008](http://www.labri.fr/perso/reveille/DSPD/2008/)\
[McGPLE
2008](http://www.infosun.fim.uni-passau.de/cl/staff/apel/McGPLE2008/index.html)\
[STS 2008](../Sts/STS08)

**Calls for**\
[Papers](CallForPapers){.twikiLink}\
[Tutorials](CallForTutorials){.twikiLink}\
[Workshops](CallForWorkshops){.twikiLink}

**[Electronic\
Submission](http://www.easychair.org/conferences/?conf=gpce2008)**
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/GPCE08/FundamentalistFunctionalProgramming?t=1536828763)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE08/FundamentalistFunctionalProgramming)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE08/FundamentalistFunctionalProgramming)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE08/FundamentalistFunctionalProgramming?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE08/FundamentalistFunctionalProgramming?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/GPCE08/FundamentalistFunctionalProgramming?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/GPCE08/FundamentalistFunctionalProgramming?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/GPCE08/FundamentalistFunctionalProgramming?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/GPCE08/FundamentalistFunctionalProgramming?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/GPCE08/FundamentalistFunctionalProgramming?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/GPCE08/FundamentalistFunctionalProgramming?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE08/FundamentalistFunctionalProgramming)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE08/FundamentalistFunctionalProgramming?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/GPCE08/FundamentalistFunctionalProgramming?template=oopsmore&param1=1.5&param2=1.5)
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
FundamentalistFunctionalProgramming {#fundamentalistfunctionalprogramming .twikiTopicTitle}
===================================

::: {.twikiWebTitle}
Generative Programming and Component Engineering
:::

[]{#Abstract} Abstract
----------------------

In 1984, John Hughes wrote a seminal paper titled, \"Why Functional
Programming Matters,\" in which he eloquently explained the value of
pure and lazy functional programming. Due to the increasing importance
of the Web and the introduction of many-core machines, in the quarter of
a century since the paper was written, the problems associated with
imperative languages and their side effects have become increasingly
evident. This talk argues that fundamentalist functional
programming---that is, radically eliminating all side effects from
programming languages, including strict evaluation---is what it takes to
conquer the concurrency and parallelism dragon. Programmers must embrace
pure, lazy functional programming \"all the way\"---with all effects
apparent in the type system of the host language using monads. A radical
paradigm shift is the answer, but does that mean that all current
programmers will be lost along the way? Fortunately not! By design, LINQ
is based on monadic principles, and the success of LINQ proves that the
world does not fear the monads.

[]{#Bio} Bio
------------

Erik Meijer is an accomplished programming-language designer who has
worked on a wide range of languages, including Haskell, Mondrian, X\#,
C-Omega, C\#, and Visual Basic. He runs the Data Programmability
Languages Team at Microsoft, where his primary focus has been to remove
the impedance mismatch between databases and programming languages. One
of the fruits of these efforts is LINQ, which not only adds a native
querying syntax to .NET languages, such as C\# and Visual Basic, but
also allows developers to query data sources other than tables, such as
objects or XML. Most recently, Erik has been working on democratizing
the Cloud using Volta and preaching the virtues of fundamentalist
functional programming in the new age of concurrency and many-core. Some
people might recognize him from his brief stint as the \"Head in the
Box\" on Microsoft VBTV.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*GPCE08.FundamentalistFunctionalProgramming moved from
GPCE08.ErikKeynote on 05 Aug 2008 - 05:21 by
[JeremySiek](../Main/JeremySiek){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/GPCE08/FundamentalistFunctionalProgramming?newweb=GPCE08&newtopic=ErikKeynote&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
