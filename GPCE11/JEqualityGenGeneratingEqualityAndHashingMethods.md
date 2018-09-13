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
    Page](http://www.program-transformation.org/edit/GPCE11/JEqualityGenGeneratingEqualityAndHashingMethods?t=1536828814)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE11/JEqualityGenGeneratingEqualityAndHashingMethods)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE11/JEqualityGenGeneratingEqualityAndHashingMethods)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE11/JEqualityGenGeneratingEqualityAndHashingMethods?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE11/JEqualityGenGeneratingEqualityAndHashingMethods?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/GPCE11/JEqualityGenGeneratingEqualityAndHashingMethods?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE11/JEqualityGenGeneratingEqualityAndHashingMethods)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE11/JEqualityGenGeneratingEqualityAndHashingMethods?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/GPCE11/JEqualityGenGeneratingEqualityAndHashingMethods?template=oopsmore&param1=1.1&param2=1.1)
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
JEqualityGen: Generating equality and hashing methods {#jequalitygen-generating-equality-and-hashing-methods .twikiTopicTitle}
=====================================================

::: {.twikiWebTitle}
Neville Grech, Julian Rathke and Bernd Fischer
:::

**Abstract**: Manually implementing equals (for object comparisons) and
hashCode (for object hashing) methods in large software projects is
tedious and error-prone. This is due to many special cases, such as
field shadowing, comparison between different types, or cyclic object
graphs. Here, we present JEqualityGen, a source code generator that
automatically derives implementations of these methods.

JEqualityGen proceeds in two states: it first uses source code
reflection in MetaAspectJ to generate aspects that contain the method
implementations, before it uses weaving on the bytecode level to insert
these into the target application. JEqualityGen generates not only
correct, but efficient source code that on a typical large-scale Java
application exhibits a performance improvement of more than two orders
of magnitude in the equality operations generated, compared to an
existing system based on runtime reflection. JEqualityGen achieves this
by generating runtime profiling code that collects data. This enables it
to generate optimised method implementations in a second round.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
