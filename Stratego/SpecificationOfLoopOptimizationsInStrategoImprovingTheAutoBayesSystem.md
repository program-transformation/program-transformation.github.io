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
    Page](http://www.program-transformation.org/edit/Stratego/SpecificationOfLoopOptimizationsInStrategoImprovingTheAutoBayesSystem?t=1536825429)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/SpecificationOfLoopOptimizationsInStrategoImprovingTheAutoBayesSystem)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/SpecificationOfLoopOptimizationsInStrategoImprovingTheAutoBayesSystem)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/SpecificationOfLoopOptimizationsInStrategoImprovingTheAutoBayesSystem?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/SpecificationOfLoopOptimizationsInStrategoImprovingTheAutoBayesSystem?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/SpecificationOfLoopOptimizationsInStrategoImprovingTheAutoBayesSystem?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/SpecificationOfLoopOptimizationsInStrategoImprovingTheAutoBayesSystem?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/SpecificationOfLoopOptimizationsInStrategoImprovingTheAutoBayesSystem?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/SpecificationOfLoopOptimizationsInStrategoImprovingTheAutoBayesSystem)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/SpecificationOfLoopOptimizationsInStrategoImprovingTheAutoBayesSystem?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/SpecificationOfLoopOptimizationsInStrategoImprovingTheAutoBayesSystem?template=oopsmore&param1=1.2&param2=1.2)
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
[Jozef Kruger](../Main/JozefKruger){.twikiLink}. **Specification Of Loop
Optimizations In Stratego. Improving the AutoBayes System**. Master\'s
thesis. Institute of Information and Computing Sciences, Utrecht
University, The Netherlands. November 2003.
([pdf](http://www.cs.uu.nl/~visser/ftp/Kru03.pdf))

### []{#Abstract} Abstract

Manually writing programs that perform statistic data analysis is an
arduous and error prone task. In order to automatically generate such
programs the AutoBayes system has been developed at NASA Ames,
California. This system takes an analysis description and generates
fully documented C/C++ code from it, this process is called program
synthesis. In this process of generating code, no optimizations are
performed. This project extends the AutoBayes system with an optimizer
that especially aims at loop optimizations.

XBayes is the (loop-)optimizer described in this thesis and it performs
a number of optimizations: loop fusion, sum simplification, invariant
code elimination, common subexpression elimination with alpha equality
and constant propagation. A large part of the project consists of
dependence analysis; data dependences in particular. This is the basis
for the loop fusion algorithm. The loop fusion algorithm we will present
in this thesis has been based upon Typed Fusion, but is completely
rewritten in order to obtain a rewriting algorithm instead of an
imperative one.

The system transforms abstract syntax trees (ASTs), which are a high
level representation of programs generated by the AutoBayes system. One
of the benifits of this high level representation is that more
information (or structure) about the program is available. An example of
this are summation constructs which are transformed into loops when C
code is generated. With these constructs, more specific transformations
can be done (sum simplification for example).

The optimizer has been implemented in the Stratego language, a language
based on the paradigm of rewriting rules and strategies. The AutoBayes
system was written in Prolog, therefore a bridge between the two
languages has been built as well. AutoBayes makes heavy use of
attributes to assert conditions and generate comments throughout its
synthesis phase, the optimizations described in this thesis also add
comments whenever a transformation has been done.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
