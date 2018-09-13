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
    Page](http://www.program-transformation.org/edit/Transform/JavaReflection?t=1536826504)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/JavaReflection)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/JavaReflection)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/JavaReflection?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/JavaReflection?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/JavaReflection?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/JavaReflection)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/JavaReflection?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/JavaReflection?template=oopsmore&param1=1.1&param2=1.1)
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
Java Reflection {#java-reflection .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Description**

One of Java\'s strengths is that it was designed with the assumption
that the environment in which it was running would be changing
dynamically. Classes are loaded dynamically, binding is done
dynamically, and object instances are created dynamically on the fly
when they are needed. What has not been very dynamic historically is the
ability to manipulate \"anonymous\" classes. In this context, an
anonymous class is one that is loaded or presented to a Java class at
run time and whose type was previously unknown to the Java program.
\[Sun 1998\]

Java programs can now \"reflect\" upon themselves or upon an arbitrary
class to determine the methods and fields defined by that class,
arguments and so on. What exactly does that mean? By utilizing the
packages in the Java Reflection [API](API){.twikiLink} to obtain
complete information about any object, array, method, constructor, or
field.

Fundamentally, the Reflection [API](API){.twikiLink} consists of two
components: objects that represent the various parts of a class file,
and a means for extracting those objects in a safe and secure way.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
