::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![gpce-logo.jpg](../pub/GPCE07/WebLeftBar/gpce-logo.jpg){width="100"
height="120"}

**[GPCE Home](http://www.gpce.org/)**\
**[GPCE\'07 Home](WebHome){.twikiLink}**\
[Conference Program](ConferenceProgram){.twikiLink} br /& **[Final
Program[^?^](/edit/GPCE07/PubGPCE07WebHomeGpceProgrampdf?topicparent=GPCE07.TutorialGPCE2)]{.twikiNewLink
style="background : #FFFFCE;"}(pdf)** \--\>\
[Organization](ConferenceOrganization){.twikiLink}\
[Dates](ImportantDates){.twikiLink}\
[Venue (with
ESWEEK)](http://www.ida.liu.se/conferences/codes/esweek/venue.shtml)\
[Registration and hotel
information](ConferenceRegistration){.twikiLink}\
\
**[Tutorials (Sept. 30)](GpceTutorials){.twikiLink}**\
a class=\"twikiLink\" href=\"/GPCE07/TutorialGPCE1\"/a& \|\--\>
[GPCE2](TutorialGPCE2){.twikiLink} br /&
[GPCE3](/GPCE07/TutorialGPCE3){.twikiLink} \|
[GPCE4](/GPCE07/TutorialGPCE4){.twikiLink}\--\>\
\
**[Workshops (Oct. 4)](GpceWorkshops){.twikiLink}**\
[APGES\'07](APGES07){.twikiLink}\
[AOPLE\'07](AOPLE07){.twikiLink}\
\
**Calls for**\
[Papers](CallForPapers){.twikiLink}\
[Tutorials](http://resource-aware.org/twiki/bin/view/GPCE07/CallForTutorials)\
[Workshops](CallForWorkshops){.twikiLink}\
\
**[Electronic
submission](http://www.easychair.org/conferences/?conf=GPCE07)**
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/GPCE07/TutorialGPCE2?t=1536828009)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE07/TutorialGPCE2)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE07/TutorialGPCE2)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE07/TutorialGPCE2?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE07/TutorialGPCE2?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/GPCE07/TutorialGPCE2?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/GPCE07/TutorialGPCE2?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/GPCE07/TutorialGPCE2?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/GPCE07/TutorialGPCE2?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/GPCE07/TutorialGPCE2?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/GPCE07/TutorialGPCE2?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE07/TutorialGPCE2)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE07/TutorialGPCE2?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/GPCE07/TutorialGPCE2?template=oopsmore&param1=1.8&param2=1.8)
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
TutorialGPCE2 {#tutorialgpce2 .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Generative Programming and Component Engineering
:::

[]{#Building_Composable_Domain_speci} Building Composable, Domain-specific and General Purpose Extensions to Java
-----------------------------------------------------------------------------------------------------------------

**Note:** Despite low registration in all tutorials, this tutorial will
be held. But it is running informally, without any charges to the
participants. The tutorial will take place Sunday 9:00-12:30 in [NH
Hotel
Salzburg](http://www.nh-hotels.com/nh/en/hotels/austria/salzburg/nh-salzburg-city.html)
in the \"Club\" meeting room. To attend the tutorial, please send an
email to [Ulrik Schultz](mailto:ups@mmmi.sdu.dk).

------------------------------------------------------------------------

Eric Van Wyk, University of Minnesota

This tutorial provides an introduction to building domain-specific and
general purpose language extensions to Java. This is illustrated using
ableJ, an attribute grammar-based extensible language framework for
Java. Language extensions may define the syntax, semantic analysis, and
optimizations of new language features. We describe several language
extensions and their implementation in the framework. For example, one
embeds the SQL database query language into Java and statically checks
for syntax and type errors in SQL queries. AbleJ supports the modular
specification of composable language extensions so that programmers can
import into Java the unique set of extensions that they desire.

The tutorial introduces Silver, a feature-rich attribute grammar
specification language that also supports local and composable global
transformations. It also covers the ableJ framework; a specification of
Java written in Silver. We cover various aspects of this specification
to show how one can build new language extensions to Java.

**Duration:** Half-day

**Level:** Introductory

**Required Knowledge:** Although a basic understanding of compilers,
context free grammars and abstract syntax trees is helpful it is not
required. These basic concepts will be discussed in the context of
Silver. Basic understanding of Java is assumed.

**Speaker Profile**

Dr. Eric Van Wyk is an assistant professor at the University of
Minnesota and is a McKnight Land-Grant professor. His research interests
include techniques for the declarative specification and implementation
of languages and language extensions.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
