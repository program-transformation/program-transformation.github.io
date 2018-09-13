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
    Page](http://www.program-transformation.org/edit/Stratego/SimplifyingTheSimplifier?t=1536825429)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/SimplifyingTheSimplifier)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/SimplifyingTheSimplifier)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/SimplifyingTheSimplifier?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/SimplifyingTheSimplifier?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/SimplifyingTheSimplifier?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/SimplifyingTheSimplifier)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/SimplifyingTheSimplifier?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/SimplifyingTheSimplifier?template=oopsmore&param1=1.1&param2=1.1)
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
Simplifying The Simplifier {#simplifying-the-simplifier .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Alan van Dam. **Simplifying the Simplifier. [HsOpt](HsOpt){.twikiLink}:
a modular, rewrite rule based simplifier for the Helium compiler, a
non-strict functional compiler.** Institute of Information and Computing
Sciences, Utrecht University, The Netherlands Master\'s thesis
INF/SCR-03-25, July 7, 2003.
([pdf](http://www.cs.uu.nl/~visser/ftp/Dam03.pdf))

### []{#Abstract} Abstract

Modern compilers optimize code during the compilation process. The goal
of the optimizations is to obtain a program that is semantically
equivalent, executes faster and uses less memory. The Glasgow Haskell
Compiler also uses a simplifier. This simplifier is not modular and
difficult to extend. The [HsOpt](HsOpt){.twikiLink} simplifier is a
\'simplified\' GHC simplifier. The [HsOpt](HsOpt){.twikiLink} simplifier
is modular and relatively easy to extend. [HsOpt](HsOpt){.twikiLink} is
based on the paradigm of correctness preserving rewrite rules. The
transformations can be applied separately. [HsOpt](HsOpt){.twikiLink}
interacts with the Helium compiler, a compiler for a large subset of
Haskell. Helium uses a naive pattern matcher compiler which results in
straightforward intermediate Core code. [HsOpt](HsOpt){.twikiLink}
simplifies most of the straightforward code. The result is Core code
that could have been produced by an intelligent pattern match compiler.
The simplified programs execute 10-15% faster and uses 0-25% less
memory.

### []{#Links} Links

-   [HsOpt](HsOpt){.twikiLink}
-   <http://www.vandamnet.nl/hsopt>
-   <alan@vandamnet.nl>

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
