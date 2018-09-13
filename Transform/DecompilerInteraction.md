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
    Page](http://www.program-transformation.org/edit/Transform/DecompilerInteraction?t=1536826296)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilerInteraction)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilerInteraction)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilerInteraction?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilerInteraction?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/DecompilerInteraction?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DecompilerInteraction?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DecompilerInteraction?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilerInteraction)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilerInteraction?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilerInteraction?template=oopsmore&param1=1.2&param2=1.2)
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
Decompiler Interaction {#decompiler-interaction .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

In a poorly designed decompiler (including all current decompilers and
also disassemblers), a graphical user interface (GUI) or equivalent
(e.g. Sourcer\'s specification files) are necessary so that the user can
correct the gross mistakes made, or to implement features that the
analysis simply doesn\'t do. For example, in the [IDA
Pro](IDAPro){.twikiLink} disassembler, no attempt is made to separate
constants from pointers, so the user has to do all these via the GUI.
Stack depth is sometimes calculated correctly, but when the called
function doesn\'t have the right calling convention, the user has to
correct the stack modification amount for the function.

For a long time, these corrections will be needed. However, it doesn\'t
hurt to dream: what use, if any, is there for a GUI in a decompiler that
has good analyses? Sure, all analyses can fail, but in those cases,
might it be better to just fix the limitation in the decompiler, and
leave it as a batch processing program (i.e. no GUI)? Or perhaps have a
GUI, but just to amuse the user and/or allow the user to browse the
results before the analysis is finished?

Well, it turns out that there are still some valid reasons to want to
have a GUI anyway, even if the analyses are very good. Many interesting
questions in decompilation (and in compilation and any other program
transformation or even visualisation) are equivalent to the halting
problem, and so cannot be answered in the general case. Compilers avoid
this problem by simply not performing certain optimisations when they
are not safe. Decompilers have to make other conservative actions, such
as putting a variable into the set of address-escaped variables even if
in fact no code uses that address to change the value of the variable
unexpectedly. Such variables cannot be propagated, since aliases may
cause the propagation to change the semantics of the program. Not
propagating the variable can result in a less readable program,
sometimes very significantly so. So if the GUI can in effect tell the
decompiler \"this apparently safe operation is hereby declated to be
safe\" (and if it is not, well the user asked for it!).

So here is partial list of things that a GUI could be used for:

-   as above, overriding conservative decisions by the analysis routines
-   (obviously) meaningful names for variables and procedures, and
    meaningful comments
-   arbitrary choices, where the result is better only in the eyes of
    the reader (e.g. a complex for loop verses the equivalent while
    loop; hex verses decimal verses octal verses character notation for
    a particular constant)

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
