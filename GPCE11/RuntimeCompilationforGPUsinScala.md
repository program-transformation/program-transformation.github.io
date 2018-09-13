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
    Page](http://www.program-transformation.org/edit/GPCE11/RuntimeCompilationforGPUsinScala?t=1536828809)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE11/RuntimeCompilationforGPUsinScala)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE11/RuntimeCompilationforGPUsinScala)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE11/RuntimeCompilationforGPUsinScala?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE11/RuntimeCompilationforGPUsinScala?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/GPCE11/RuntimeCompilationforGPUsinScala?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE11/RuntimeCompilationforGPUsinScala)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE11/RuntimeCompilationforGPUsinScala?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/GPCE11/RuntimeCompilationforGPUsinScala?template=oopsmore&param1=1.1&param2=1.1)
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
Firepile: Run-time Compilation for GPUs in Scala {#firepile-run-time-compilation-for-gpus-in-scala .twikiTopicTitle}
================================================

::: {.twikiWebTitle}
Nathaniel Nystrom, Derek White and Kishen Das
:::

**Abstract**:

Recent advances have enabled GPUs to be used as general-purpose parallel
processors on commodity hardware for little cost. However, the ability
to program these devices has not kept up with their performance. The
programming model for GPUs has a number of restrictions that make it
difﬁcult to program. For example, software running on the GPU cannot
perform dynamic memory allocation, requiring the programmer to
pre-allocate all memory the GPU might use. To achieve good performance,
GPU programmers must also be aware of how data is moved between host and
GPU memory and between the different levels of the GPU memory hierarchy.
We describe Firepile, a library for GPU programming in Scala. The
library enables a subset of Scala to be executed on the GPU. Code trees
can be created from run-time function values, which can then be analyzed
and transformed to generate GPU code. A key property of this mechanism
is that it is modular: unlike with other meta-programming constructs,
the use of code trees need not be exposed in the library interface. Code
trees are general and can be used by library writers in other
application domains. Our experiments show Firepile users can achieve
performance comparable to C code targeted to the GPU with shorter,
simpler, and easier-tounderstand code.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
