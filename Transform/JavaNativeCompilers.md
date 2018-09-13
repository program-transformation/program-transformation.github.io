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
    Page](http://www.program-transformation.org/edit/Transform/JavaNativeCompilers?t=1536826503)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/JavaNativeCompilers)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/JavaNativeCompilers)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/JavaNativeCompilers?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/JavaNativeCompilers?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/JavaNativeCompilers?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/JavaNativeCompilers)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/JavaNativeCompilers?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/JavaNativeCompilers?template=oopsmore&param1=1.1&param2=1.1)
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
Java Native Compilers {#java-native-compilers .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

It seems that most Java native compilers (which allow you to compile
your Java source code to native machine instructions) actually read
.class files, rather than .java files. In other words, you have to use a
standard Java compiler such as *javac* to compile your Java source file
into a .class file. Apparently, this is to save the hassle of parsing
the Java source file, providing error messages for syntax errors, and so
on. It also means that .class files have almost as much information in
them as .java files do, at least enough to translate them to native
code.

In other words, Java native compilers are much closer to [Binary
Translators](BinaryTranslation){.twikiLink} than [Java Dynamic
Compilers](JavaDynamicCompilers){.twikiLink} are. If you consider the
bytecode format to be a binary format, then they are true binary
translators. My ([MikeVanEmmerik](MikeVanEmmerik){.twikiLink}\'s)
opinion is that class files are true binary files; it just happens that
they are rich with class and method names and the like.

Links

-   [Web Pages Related to Compiling the Java Programming
    Language](http://www.bearcave.com/software/java/comp_java.html)
-   [Marco Schmidt\'s Java Compilers
    page](http://www.geocities.com/SiliconValley/Lakes/6686/jcomp.html#native)

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 02 Apr 2002\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
