::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
  ----------------------------------------------------------------------------------
  [![](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)](WebHome)
  ----------------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

-   [Documentation](StrategoDocumentation){.twikiLink}
-   [Language](StrategoLanguage){.twikiLink}
-   [Research Papers](StrategoPublications){.twikiLink}
-   [Applications](StrategoApplication){.twikiLink}

**[Download](StrategoDownload){.twikiLink}**

-   [Continuous build](ContinuousBuild){.twikiLink}
-   [Extensions](AdditionalPackageDownload){.twikiLink}

**[Support](StrategoSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Users Days](StrategoUsersDay){.twikiLink}
-   [Bug Reports](http://yellowgrass.org/project/StrategoXT)

**[Developers](StrategoDev){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/StrategoXT/strategoxt/trunk)
-   [Buildfarm
    results](http://hydra.nixos.org/jobset/strategoxt/strategoxt-release/all)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Stratego/StrategoDebug?t=1536825673)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoDebug)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoDebug)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoDebug?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoDebug?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoDebug?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoDebug?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoDebug?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoDebug)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoDebug?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoDebug?template=oopsmore&param1=1.2&param2=1.2)
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
Stratego Debug {#stratego-debug .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

There are several [DebuggingTechniques](DebuggingTechniques){.twikiLink}
for debugging Stratego programs. More support from the
[StrategoCompiler](StrategoCompiler){.twikiLink} could be useful
sometimes.

### []{#Tracing} Tracing

Since [StrategoRelease062](StrategoRelease062){.twikiLink} there is some
support for letting the compiler instrument a program to trace the
strategies called. Compilation with the flag `--trace-all` leads to
tracing of all strategy definitions and rules.

### []{#Animation} Animation

The tracing could be improved to produce input for debugging frameworks
such as [PieterOlivier](../Transform/PieterOlivier){.twikiLink}\'s Tide
that can be used to animate the execution of a program. Besides
debugging this could be useful for explaining the operational semantics
of Stratego programs.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 09 Dec 2001\

------------------------------------------------------------------------

[ToDo](ToDo){.twikiLink} \|
[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.StrategoDebug)]{.twikiNewLink
style="background : #FFFFCE;"}

### []{#Enhanced_debug_output} Enhanced debug output

One of the main problems while debugging can be the huge amounts of
ATerm dumps in one\'s terminal.

[StrategoMisc](StrategoMisc){.twikiLink} offers some tools (output
coloring, nested, tree-like debug output) to obtain more structured
debug output and better distinction between the output of various debug
statements.

\-- [ArthurVanDam](../Main/ArthurVanDam){.twikiLink} - 03 Feb 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
