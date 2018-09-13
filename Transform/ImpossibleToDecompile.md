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
    Page](http://www.program-transformation.org/edit/Transform/ImpossibleToDecompile?t=1536826296)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ImpossibleToDecompile)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ImpossibleToDecompile)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ImpossibleToDecompile?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ImpossibleToDecompile?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/ImpossibleToDecompile?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/ImpossibleToDecompile?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/ImpossibleToDecompile?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ImpossibleToDecompile)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ImpossibleToDecompile?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/ImpossibleToDecompile?template=oopsmore&param1=1.2&param2=1.2)
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
Impossible To Decompile {#impossible-to-decompile .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

There may be a few machine code patterns that are impossible to
decompile automatically. These would therefore require expert human
intervention to decompile successfully.

There are features such as the original comments, variable names and
function names that can never be recovered, although very powerful
analyses may be able to suggest good (perhaps even better than the
original, in some cases) alternatives. These unrecoverable features are
not the aim of this page, since correct decompilations can be generated
(even if usually less readable that the original) without recovering the
original comments or names.

#### []{#Reference_combined_with_casts} Reference combined with casts

This is an example of a machine code pattern that initially I thought
was not decompilable automatically. However, correct, if less readable,
code is possible with an automatic decompiler.

Consider a reference to a memory variable. In machine code, an
expression such as `sp-K` where `sp` is the stack pointer register and
`K` is a constant, takes the address of a local variable, and could be
passed as a parameter to a library function. It may not be known whether
this reference will define or use the implied memory expression (in the
example, `m[sp-K]`, where `m[x]` means the memory at address `x`). It is
possible that the memory location is the coalescing of two or more
original variables of different type, so that in the most readable
decompilation, the memory location would be split into two different
variables in the decomiled output. Usually, the decompiler would be able
to use the type of the reference to decide which of several live ranges
the reference belongs to, i.e. which original variable the expression is
the address of.

      lea eax, [esp-24]
      push eax
      call use-as-char-star
      lea eax, [esp-24]
      push eax
      call use-as-float
      lea eax, [esp-24]
      push eax
      call use-as-int

In the above example, the four bytes at `m[esp-24]` are used as a
reference to a char\*, a float, and as an int. (At the machine code
level, references are handled by passing the address as a value
parameter). Are they all the same variable with at least two casts? Or
does the call to use-as-float overwrite the original variable, and
therefore reference a different variable to the first reference? (So the
compiler re-used the same local variable address for three separate
source code variables). Here are two of several possible outputs (in C;
in C++, the & could be removed from the calls):

      char* px;                      char* px;
      float* py;
      int* pz;

      use-as-char-star(&px);         use-as-char-star(&px);
      use-as-float(&py);             use-as-float((float*)&px);
      use-as-int(&pz);               use-as-int((int*)&px);

However, the second decompilation, while arguably less readable with the
casts, is just as valid as the input program, so an automatic decompiler
can generate the second version and always have correct, working output.
If the user wants to, s/he can attempt to improve the program to the
original version, taking the risk that the program may no longer work.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 08 May 2006\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
