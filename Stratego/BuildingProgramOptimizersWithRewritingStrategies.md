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
    Page](http://www.program-transformation.org/edit/Stratego/BuildingProgramOptimizersWithRewritingStrategies?t=1536825424)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/BuildingProgramOptimizersWithRewritingStrategies)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/BuildingProgramOptimizersWithRewritingStrategies)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/BuildingProgramOptimizersWithRewritingStrategies?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/BuildingProgramOptimizersWithRewritingStrategies?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/BuildingProgramOptimizersWithRewritingStrategies?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/BuildingProgramOptimizersWithRewritingStrategies?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/BuildingProgramOptimizersWithRewritingStrategies?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/BuildingProgramOptimizersWithRewritingStrategies?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/BuildingProgramOptimizersWithRewritingStrategies?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/BuildingProgramOptimizersWithRewritingStrategies)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/BuildingProgramOptimizersWithRewritingStrategies?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/BuildingProgramOptimizersWithRewritingStrategies?template=oopsmore&param1=1.3&param2=1.3)
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
[E. Visser](EelcoVisser){.twikiLink}, Z.-e.-A. Benaissa, and A. Tolmach.
**Building program optimizers with rewriting strategies.** In
*Proceedings of the third ACM SIGPLAN International Conference on
Functional Programming (ICFP\'98)*, pages 13\--26. ACM Press, September
1998.

### []{#Abstract} Abstract

We describe a language for defining term rewriting strategies, and its
application to the production of program optimizers. Valid
transformations on program terms can be described by a set of rewrite
rules; rewriting strategies are used to describe when and how the
various rules should be applied in order to obtain the desired
optimization effects. Separating rules from strategies in this fashion
makes it easier to reason about the behavior of the optimizer as a
whole, compared to traditional monolithic optimizer implementations. We
illustrate the expressiveness of our language by using it to describe a
simple optimizer for an ML-like intermediate representation.

The basic strategy language uses operators such as sequential
composition, choice, and recursion to build transformers from a set of
labeled unconditional rewrite rules. We also define an extended language
in which the side-conditions and contextual rules that arise in
realistic optimizer specifications can themselves be expressed as
strategy-driven rewrites. We show that the features of the basic and
extended languages can be expressed by breaking down the rewrite rules
into their primitive building blocks, namely matching and building terms
in variable binding environments. This gives us a low-level core
language which has a clear semantics, can be implemented
straightforwardly and can itself be optimized. The current
implementation generates C code from a strategy specification.

### []{#Preprint} Preprint

-   <http://www.cs.uu.nl/~visser/ftp/VBT98.ps.gz>
-   <http://www.cs.uu.nl/~visser/ftp/VBT98.ps.zip>

<!-- -->

-   Citeseer: <http://citeseer.nj.nec.com/54625.html>,
    <http://citeseer.nj.nec.com/visser98building.html>

------------------------------------------------------------------------

[CategoryPaper](../Transform/CategoryPaper){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
