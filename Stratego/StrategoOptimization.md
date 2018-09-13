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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoOptimization?t=1536825677)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoOptimization)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoOptimization)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoOptimization?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoOptimization?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/StrategoOptimization?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/StrategoOptimization?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoOptimization?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoOptimization?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoOptimization?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoOptimization)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoOptimization?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoOptimization?template=oopsmore&param1=1.3&param2=1.3)
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
Stratego Optimization {#stratego-optimization .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The [StrategoCompiler](StrategoCompiler){.twikiLink} performs a number
of transformations/optimizations including the following:

-   Pattern match merging
-   Symbol caching
-   Simplification
-   Desugaring

The following optimizations are supported experimentally, but
implementation should be improved:

-   [DefinitionInlining[^?^](http://www.program-transformation.org/edit/Stratego/DefinitionInlining?topicparent=Stratego.StrategoOptimization)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [InnermostFusion](InnermostFusion){.twikiLink}
-   [BuildMatchFusion](BuildMatchFusion){.twikiLink}

New optimizations that could beneficial

-   [MatchingOnlyCongruence[^?^](http://www.program-transformation.org/edit/Stratego/MatchingOnlyCongruence?topicparent=Stratego.StrategoOptimization)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [EffectsAnalysis](EffectsAnalysis){.twikiLink}
-   [ConstantTermCaching](ConstantTermCaching){.twikiLink}

To measure the effect of optimizations set up

-   [StrategoBench[^?^](http://www.program-transformation.org/edit/Stratego/StrategoBench?topicparent=Stratego.StrategoOptimization)]{.twikiNewLink
    style="background : #FFFFCE;"}

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 08 Dec 2001\

------------------------------------------------------------------------

-   Control what kind of object files (dbg, opt, prof) are linked
    -   use gcc lib as standard (is optimized O4)

<!-- -->

-   F(id,\\ H(x) -\> G(x,x) \\, id) is equivalent to \\ F(a, H(x), b)
    -\> F(a, G(x,x), b)
-   set up benchmarks and reggression tests
    -   propositional formulae
    -   sieve
    -   note: the compiler itself is of course the real regression test
        although it does not cover all aspects/constructs of the
        language

<!-- -->

-   Make a set of benchmarks that can function as reference for
    optimizations

<!-- -->

-   Do effects analysis on strategy expressions; distinghuish the
    following effects: no effect, transformation effect, variable
    binding effect, failure effect

<!-- -->

-   Also inline sums of rules if they occur inside a sum

<!-- -->

-   Generate congruence definition by need in the same style as
    threading and distributing congruences.

------------------------------------------------------------------------

[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.StrategoOptimization)]{.twikiNewLink
style="background : #FFFFCE;"} \| [ToDo](ToDo){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.StrategoOptimization moved from Stratego.StrategoOptimizations
on 09 Dec 2001 - 14:24 by
[EelcoVisser](../Main/EelcoVisser){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Stratego/StrategoOptimization?newweb=Stratego&newtopic=StrategoOptimizations&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
