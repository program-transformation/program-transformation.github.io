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
    Page](http://www.program-transformation.org/edit/GPCE13/P112Efftinge?t=1536828840)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE13/P112Efftinge)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE13/P112Efftinge)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE13/P112Efftinge?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE13/P112Efftinge?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/GPCE13/P112Efftinge?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE13/P112Efftinge)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE13/P112Efftinge?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/GPCE13/P112Efftinge?template=oopsmore&param1=1.1&param2=1.1)
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
Xbase: Implementing Domain-Specific Languages for Java {#xbase-implementing-domain-specific-languages-for-java .twikiTopicTitle}
======================================================

::: {.twikiWebTitle}
Sven Efftinge, Moritz Eysholdt, Jan Köhnlein, Sebastian Zarnekow,
Wilhelm Hasselbring, Robert von Massow, and Michael Hanus
:::

Xtext is an open-source framework for implementing external, textual
domain-specific languages (DSLs). So far, most DSLs implemented with
Xtext and similar tools focus on structural aspects such as service
specifications and entities. Because behavioral aspects are
significantly more complicated to implement, they are often delegated to
general-purpose programming languages. This approach introduces complex
integration patterns and the DSL\'s high level of abstraction is
compromised.

We present Xbase as part of Xtext, an expression language that can be
reused via language inheritance in any DSL implementation based on
Xtext. Xbase expressions provide both control structures and program
expressions in a uniform way. Xbase is statically typed and tightly
integrated with the Java type system. Languages extending Xbase inherit
the syntax of a Java-like expression language as well as language
infrastructure components, including a parser, an unparser, a linker, a
compiler and an interpreter. Furthermore, the framework provides
integration into the Eclipse IDE including debug and refactoring
support.

The application of Xbase is presented by means of a domain model
language which serves as a tutorial example and by the implementation of
the programming language Xtend. Xtend is a functional and
object-oriented general purpose language for the Java Virtual Machine
(JVM). It is built on top of Xbase which is the reusable expression
language that is the foundation of Xtend.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
