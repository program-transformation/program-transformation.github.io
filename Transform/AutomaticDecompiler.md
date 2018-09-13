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
    Page](http://www.program-transformation.org/edit/Transform/AutomaticDecompiler?t=1536826294)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/AutomaticDecompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/AutomaticDecompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/AutomaticDecompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/AutomaticDecompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/AutomaticDecompiler?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/AutomaticDecompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/AutomaticDecompiler?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/AutomaticDecompiler?template=oopsmore&param1=1.1&param2=1.1)
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
Automatic Decompiler {#automatic-decompiler .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Every few months, I get an email asking where to find an automatic
decompiler that will take a binary as input and produce good quality C
or C++ code for maintaining an application. Usually, the correspondent
owns the binary code, but somehow they don\'t have the source code and
would like it back.

Regrettably, the state of the art in decompilation is such that this is
still not possible. About the closest thing to such an automatic
decompiler is [REC](DecompilationGeneralApproach#REC){.twikiAnchorLink}
(Reverse Engineering Decompiler). But it doesn\'t generate compilable C,
just C-like code that helps understand a binary program.

One day, the [Boomerang](DecompilationBoomerang){.twikiLink} decompiler
may be good enough to use for this purpose, but it\'s probably at least
one, probably several years away from that state.

So the best I can recommend is a good disassembler, such as \[IDA Pro\].
It will not be automatic; the disassembler can make a lot of guesses
automatically, but it leaves many decisions up to the user. With enough
work, and an expert user, you will probably be able to generate code
that is good enough to maintain. But you will have to use assembly
language experts to maintain the code, and they are less common than
they used to be. Also, your code will only work on one machine; you
don\'t have the option of porting it to another machine (so if it starts
on an Intel machine, it will stay on Intel machines).

This is not what many people expect, and not what they want to hear. But
it\'s the reality for the time being.

------------------------------------------------------------------------

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
