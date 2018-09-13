::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
[Home](WebHome){.twikiLink}

**XT Tools**

-   [Reference Docs](ToolReference){.twikiLink}
-   [GPP](GenericPrettyPrinter){.twikiLink}
-   [ATerm](ATermTools){.twikiLink}
-   [SDF](SdfTools){.twikiLink}
-   [AsFix](AsFixTools){.twikiLink}

**Languages**

-   [Stratego](../Stratego/WebHome){.twikiLink}
-   [SDF](../Sdf/WebHome){.twikiLink}
-   [ATerm](ATermFormat){.twikiLink}

**Software**

-   [Stratego/XT](../Stratego/StrategoDownload){.twikiLink}
-   [SDF2 Bundle](../Sdf/SdfBundle){.twikiLink}
-   [KoalaCompiler](KoalaCompiler){.twikiLink}
-   [AutoBundle](AutoBundle){.twikiLink}
-   [AutoBuild](AutoBuild){.twikiLink}
-   [DailyBuildSystem](DailyBuildSystem){.twikiLink}

[![](http://www.program-transformation.org/twiki/pub/rss.gif "RSS 1.0 feed")](http://www.program-transformation.org/twiki/bin/view/Tools/WebRss?skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Tools/HowToOptions?t=1536825805)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/HowToOptions)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/HowToOptions)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/HowToOptions?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/HowToOptions?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tools/HowToOptions?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/HowToOptions?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/HowToOptions?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/HowToOptions)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/HowToOptions?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tools/HowToOptions?template=oopsmore&param1=1.2&param2=1.2)
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
How To Options {#how-to-options .twikiTopicTitle}
==============

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

The [KoalaCompiler](KoalaCompiler){.twikiLink} components are all tool
components that use a standard set of command-line switches to control
their operation. Below we describe the common switches. Tool-specific
switches are discussed on the corresponding tool description page.

  ------------------ -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  \--help            By specifying the \'\--help\' switch, a tool component gives a brief list of the switches it accpets. Some times a brief decription of the tool is also displayed.
  -i \<file\>        All components consume input. Input is read from standard input or from the file specified with the \'-i\' switch.
  -o \<file\>        Components that have one output (e.g., [`koala-text`](KoalaText){.twikiLink}, [`koala-dot`](KoalaDot){.twikiLink}), write their result to standard output or to the file specified with the \'-o\' switch.
  -d \<dir\>         Components with multiple outputs (e.g., [`koala-c`](KoalaC){.twikiLink}, [`koala-stc`](KoalaSTC){.twikiLink}), store their results in the current working directory or in the directory specified with the \'-d\' option.
  -I \<dir\>         The \'-I\' switch serves to define a search path where the koala compiler components should look for component, interface, datatype definitions, and for C source files. Multiple \'-I\' switches can be specified. Only the root of a directory tree needs to be specified with the \'-I\' switch. Searching will automatically recurse in subdirectories.
  \--verbose \<n\>   Verbose execution can be controlled with the \'\--verbose\' switch. The number \'n\' indicates the level of verbosity.
  ------------------ -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 22 Dec 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
