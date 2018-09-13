::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[PEPM 2007](WebHome){.twikiLink}**\
[Call for Papers](CallForPapers){.twikiLink}\
[Important Dates](ImportantDates){.twikiLink}\
[Program Committee](ProgramCommittee){.twikiLink}\
[PEPM Publicity](PEPMPublicity){.twikiLink}\
\
**Advice for Authors**\
[Research Paper Advice](ResearchPaperAdvice){.twikiLink}\
[Tool Paper Advice](ToolPaperAdvice){.twikiLink}\
[Paper Submission](PaperSubmission){.twikiLink}\
\
**[PEPM Program](PEPMProgram){.twikiLink}**\
[Invited Talks](InvitedTalks){.twikiLink}\
[Affiliated Meetings](AffiliatedMeetings){.twikiLink}\
[Venue](WorkshopVenue){.twikiLink}\
[Registration & Accommodation](RegistrationAndAccomodation){.twikiLink}\
\
**History**\
[Previous Workshops](PreviousWorkshops){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/PEPM07/ObjectOrientedQueriesOverSoftwareSystems?t=1536827649)
-   [Rename
    Page](http://www.program-transformation.org/rename/PEPM07/ObjectOrientedQueriesOverSoftwareSystems)
-   [Attach
    File](http://www.program-transformation.org/attach/PEPM07/ObjectOrientedQueriesOverSoftwareSystems)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PEPM07/ObjectOrientedQueriesOverSoftwareSystems?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PEPM07/ObjectOrientedQueriesOverSoftwareSystems?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/PEPM07/ObjectOrientedQueriesOverSoftwareSystems?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/PEPM07/ObjectOrientedQueriesOverSoftwareSystems)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PEPM07/ObjectOrientedQueriesOverSoftwareSystems?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/PEPM07/ObjectOrientedQueriesOverSoftwareSystems?template=oopsmore&param1=1.1&param2=1.1)
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
Object Oriented Queries Over Software Systems {#object-oriented-queries-over-software-systems .twikiTopicTitle}
=============================================

::: {.twikiWebTitle}
ACM SIGPLAN 2007 Workshop on Partial Evaluation and Program Manipulation
:::

### []{#Invited_Talk_by_Oege_de_Moor} Invited Talk by Oege de Moor

#### []{#Joint_work_with_Elnar_Hajiyev_an} Joint work with Elnar Hajiyev, and Mathieu Verbaere

### []{#Abstract} Abstract

Code queries are useful for enforcing coding conventions, navigating a
large code base, and for identifying locations to refactor. The program
understanding community has long advocated the use of a relational
database to facilitate such code queries, but relational queries over
code have not found widespread use.

We argue this is due to a lack of scalability (it takes too long to
evaluate queries), and a lack of a modern query language with all the
tool support that entails (writing code queries in SQL can take many
pages). In this talk we demonstrate a new system that goes some way
towards alleviating both problems.

First, we demonstrate IQL, an object-oriented query language. It allows
the concise expression of complex queries; due to its object-oriented
features, it is easy to extend and modify existing queries. Another
benefit of object-orientation is that it gives natural tool support, for
instance for auto-completion.

The semantics of IQL is defined by translation to Datalog. Datalog is a
logic programming language like Prolog, but it lacks data structures. As
a consequence, all queries in Datalog are guaranteed to terminate, and
they have a very simple semantics, enabling aggressive optimisations.

While Datalog has been extensively studied in the theoretical database
community, it lacks a proper type system. We introduce a type system
with subtyping to account for the class hierarchy of IQL. Type inference
is achieved via an abstract interpretation that maps each relation
between runtime values to a relation between binding sites.

We implement Datalog itself via a compiler to procedural SQL; a
configuration file allows us one target different relational database
systems as the backend. The compiler performs many optimisations,
ranging from straightforward constant propagation to a form of the
well-known \`magic sets\' transformation. It also performs type
specialisation, based on the abstract interpretation in the type
inference algorithm.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
