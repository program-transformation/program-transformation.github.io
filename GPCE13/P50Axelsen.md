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
    Page](http://www.program-transformation.org/edit/GPCE13/P50Axelsen?t=1536828843)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE13/P50Axelsen)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE13/P50Axelsen)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE13/P50Axelsen?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE13/P50Axelsen?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/GPCE13/P50Axelsen?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE13/P50Axelsen)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE13/P50Axelsen?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/GPCE13/P50Axelsen?template=oopsmore&param1=1.1&param2=1.1)
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
Package Templates: A Definition by Semantics-Preserving Source-to-Source Transformations to Efficient Java Code {#package-templates-a-definition-by-semantics-preserving-source-to-source-transformations-to-efficient-java-code .twikiTopicTitle}
===============================================================================================================

::: {.twikiWebTitle}
Eyvind W. Axelsen and Stein Krogdahl
:::

Package Templates (PT) is a mechanism designed for writing reusable
modules, called templates, each consisting of a set of classes that can
be adapted to their use in a program through compile-time
specialization. A template must be instantiated in a program before its
classes can be used. The mechanism supports type-safe renaming, merging,
type parameterization and refinement in the form of static additions and
overrides that are orthogonal to the corresponding concepts of ordinary
inheritance.

In this paper, we consider PT as an extension to Java, and a PT program
will then consist of a number of Java packages and templates, where
templates are instantiated in packages or other templates. Our aim and
main contribution is to define the meaning of such a program, and to
show that this definition is consistent. We first show this for a core
subset of PT, C-PT, and define a set of source-to-source transformations
for converting C-PT programs to plain Java programs using semantics we
have described informally in previous papers. We can then define the
meaning of a C-PT program in terms of the resulting Java program. Thus,
we have to verify that the transformations will always convert a legal
C-PT program to a legal Java program. Finally, we briefly discuss how
this approach can be extended to full PT.

A main challenge is to preserve externally visible names (for classes,
methods and fields), and at the same time prevent unwanted subsequent
rebindings caused e.g. by overload resolution in the Java compiler.
Names that are bound to declarations in a template should not be rebound
to different declarations by subsequent compositions or adaptions.

In addition to defining the runtime semantics of PT constructs in terms
of their translation to Java, the transformation rules can also be seen
as a high-level approach to how a compiler for this language might be
implemented.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
