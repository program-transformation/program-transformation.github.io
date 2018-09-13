::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![gpce-logo.jpg](../pub/GPCE14/WebLeftBar/gpce-logo.jpg){width="100"
height="120"}

**[GPCE Home](http://program-transformation.org/Gpce)**\
**[GPCE\'14 Home](WebHome){.twikiLink}**\
\
**[Registration](GpceRegistration){.twikiLink}**\
\
[Program](ConferenceProgram){.twikiLink}\
[Keynote](KeynoteSpeakers){.twikiLink}\
[Tech Talk](TechTalk){.twikiLink}\
\
[Poster and Flyer](Poster){.twikiLink}\
[Organization](ConferenceOrganization){.twikiLink}\
[Dates](ImportantDates){.twikiLink}\
[Call for Papers](CallForPapers){.twikiLink}\
\
[Grants](Grants){.twikiLink}\
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/GPCE14/KaestnerTechTalk?t=1536828855)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE14/KaestnerTechTalk)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE14/KaestnerTechTalk)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE14/KaestnerTechTalk?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE14/KaestnerTechTalk?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/GPCE14/KaestnerTechTalk?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/GPCE14/KaestnerTechTalk?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/GPCE14/KaestnerTechTalk?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/GPCE14/KaestnerTechTalk?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/GPCE14/KaestnerTechTalk?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE14/KaestnerTechTalk)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE14/KaestnerTechTalk?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/GPCE14/KaestnerTechTalk?template=oopsmore&param1=1.3&param2=1.3)
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
Tech talk: An Introduction to Variability-Aware Analysis {#tech-talk-an-introduction-to-variability-aware-analysis .twikiTopicTitle}
========================================================

::: {.twikiWebTitle}
Christian Kästner and Sven Apel
:::

Compile-time variability is paramount in many software systems: Users
can select desired features and generate a product tailored for their
needs. For example, the Linux kernel has over 10000 such compile-time
configuration options. Typically organized as software product lines,
there are many different implementation mechanisms that can all be
regarded as generators that produce products based on variability
specifications.

However, variability often implies complexity. Already with few
configuration options, we can generate a vast number (easily exceeding
billions) of potential products. Checking all products individually
using classic testing or analysis techniques is not feasible.

Recently, researchers have begun to adapt existing analysis techniques,
such as type checking, model checking, theorem proving, static analysis,
and parsing, to incorporate variability. Usually, the idea is to check
the entire product line in a single step and to reason about variability
locally where it manifests at the code level. When the product line
passes the check (e.g., the product line is well-typed), it is
guaranteed that all possible generated products pass the check as well
(e.g., all products that can be generated are well-typed, too). Such
variability-aware analyses take variability information into account,
including feature models and implementation artifacts, thus spanning
problem and solution space.

In the talk, we provide an overview of concepts for variability-aware
analysis, discuss different strategies (brute force, sampling,
family-based analysis, feature-based analysis), and show recurring ideas
and patterns of how existing analysis are extended for variability.
While taking a broad view, we illustrate key ideas and also initial
results by means of a number of case studies, including the development
of a variability-aware type system and its application to Linux and the
application of variability-aware verification techniques to product-line
models.

###### []{#Biography} Biography

Christian Kästner is a researcher in the Programming Languages Group at
the Philipps University Marburg, Germany. He received his Ph.D. in
Computer Science in 2010 from the University of Magdeburg, Germany for
his work on virtual separation of concerns, which included developing a
variability-aware type system for software product lines. His research
focuses on correctness and understanding of systems with variability,
including work on implementation mechanisms, tools, different kinds of
analyses, feature interactions, and variability mining and refactoring.
He is the author or coauthor of over a fifty peer-reviewed scientific
publications.

Sven Apel is the leader of the Software Product-Line Group funded by the
esteemed Emmy Noether Programme of the German Research Foundation (DFG).
The group resides at the University of Passau, Germany. Dr.-Ing. Sven
Apel received his Ph. D. in Computer Science in 2007 from the University
of Magdeburg, Germany. His research interests include novel programming
paradigms, software engineering and product lines, and formal and
empirical methods. He is the author or coauthor of over a hundred
peer-reviewed scientific publications. Sven Apel has been a program
committee member of several highly ranked international conferences. His
work received awards by the Ernst Denert Foundation and the Karin Witte
Foundation\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
