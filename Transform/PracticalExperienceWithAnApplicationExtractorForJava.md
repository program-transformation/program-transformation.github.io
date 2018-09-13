::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

[![](../pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Transform/PracticalExperienceWithAnApplicationExtractorForJava?t=1536826535)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/PracticalExperienceWithAnApplicationExtractorForJava)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/PracticalExperienceWithAnApplicationExtractorForJava)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/PracticalExperienceWithAnApplicationExtractorForJava?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/PracticalExperienceWithAnApplicationExtractorForJava?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/PracticalExperienceWithAnApplicationExtractorForJava?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/PracticalExperienceWithAnApplicationExtractorForJava)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/PracticalExperienceWithAnApplicationExtractorForJava?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/PracticalExperienceWithAnApplicationExtractorForJava?template=oopsmore&param1=1.1&param2=1.1)
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
Practical Experience With An Application Extractor For Java {#practical-experience-with-an-application-extractor-for-java .twikiTopicTitle}
===========================================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Frank Tip, Chris Laffra, Peter F. Sweeny, David Streeter. *Practical
Experience with an Application Extractor for Java*. In Proceedings of
the Fourteenth Annual Conference on Object-Oriented Programming Systems,
Languages, and Applications(OOPSLA99), (Denver, Colorado, November
1\--5, 1999).

**Abstract**

Java programs are routinely transmitted over low-bandwidth network
connections as compressed class file archives (i.e., zip files and jar
files). Since archive size is directly proportional to download time, it
is desirable for applications to be as small as possible. This work is
concerned with the use of program transformations such as removal of
dead methods and fields, inlining of method calls, and simplification of
the class hierarchy for reducing application size. Such \`\`extraction\_
techniques are generally believed to be especially useful for
applications that use class libraries, since typically only a small
fraction of a library\'s functionality is used. By \`\`pruning away\_
unused library functionality, application size can be reduced
dramatically. We implemented a number of application extraction
techniques in JAX, an application extractor for Java, and evaluate their
effectiveness on a set of realistic benchmarks ranging from 27 to 2,332
classes (with archives ranging from 56,796 to 3,810,120 bytes). We
report archive size reductions ranging from 13.4% to 90.2% (48.7% on
average).

**See also**

-   Jax: <http://www.research.ibm.com/jax/>

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
