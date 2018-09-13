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
    Page](http://www.program-transformation.org/edit/Stratego/FusingLogicAndControl?t=1536825459)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/FusingLogicAndControl)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/FusingLogicAndControl)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/FusingLogicAndControl?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/FusingLogicAndControl?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/FusingLogicAndControl?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/FusingLogicAndControl?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/FusingLogicAndControl?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/FusingLogicAndControl)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/FusingLogicAndControl?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/FusingLogicAndControl?template=oopsmore&param1=1.2&param2=1.2)
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
Fusing Logic And Control {#fusing-logic-and-control .twikiTopicTitle}
========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[PatriciaJohann](../Transform/PatriciaJohann){.twikiLink} and
[EelcoVisser](../Main/EelcoVisser){.twikiLink}. **Strategies for Fusing
Logic and Control via Local, Application-Specific Transformations.**
[Technical Report
UU-CS-2003-050](http://www.cs.uu.nl/research/techreps/UU-CS-2003-050.html),
Institute of Information and Computing Science, Utrecht University.
([pdf](http://www.cs.uu.nl/~visser/ftp/JV03.pdf)). (This is a revised
and extended version of the publication below.)

### []{#Abstract} Abstract

Abstract programming supports the separation of logical concerns from
issues of control in program construction. While this separation of
concerns leads to reduced code size and increased reusability of code,
its main disadvantage is the computational overhead it incurs. Fusion
techniques can be used to combine the reusability of abstract programs
with the efficiency of specialized programs.

Stratego is a language for program transformation based on the paradigm
of rewriting strategies. In Stratego, transformation rules define basic
transformation steps and user-definable strategies control the
application of rules to a program. Since the problem-specific rules and
the highly generic strategies which apply them are kept separate, these
elements can be combined in a mix-and-match fashion to produce a variety
of program transformations. In some instances this separation of
concerns leads to inefficient implementations.

In this paper we show how such inefficiencies can be remedied using
fusion. Furthermore, we show how fusion can be implemented using
rewriting strategies by studying in detail the application of rewriting
strategies to the fusion of the generic innermost strategy with sets of
arbitrary-but-specific rewrite rules. Both the optimization and the
programs to which the optimization applies are specified in Stratego.

The contributions of this work are twofold. In the first place, we show
how to optimize and reason about rewriting strategies, which opens up a
new area of strategy optimization. In the second place, we demonstrate
how such optimizations can be implemented effectively using local,
application-specific transformations. These techniques are applicable to
transformation of programs in languages other than Stratego.

------------------------------------------------------------------------

[PatriciaJohann](../Transform/PatriciaJohann){.twikiLink} and
[EelcoVisser](../Main/EelcoVisser){.twikiLink}. **Fusing Logic and
Control with Local Transformations: An Example Optimization.** In
*Workshop on Reduction Strategies in Rewriting and Programming
([WRS](../Transform/WRS){.twikiLink}\'01)*, volume 57 of *Electronic
Notes in Theoretical Computer Science*, Utrecht, The Netherlands, May
2001. Elsevier Science Publishers.

### []{#Abstract} Abstract

Abstract programming supports the separation of logical concerns from
issues of control in program construction. While this separation of
concerns leads to reduced code size and increased reusability of code,
its main disadvantage is the computa- tional overhead it incurs. Fusion
techniques can be used to combine the reusability of abstract programs
with the efficiency of specialized programs.

In this paper we illustrate some of the ways in which rewriting
strategies can be used to separate the denition of program
transformation rules from the strategies under which they are applied.
Doing so supports the generic denition of program transformation
components. Fusion techniques for strategies can then be used to
specialize such generic components.

We show how the generic innermost rewriting strategy can be optimized by
fusing it with the rules to which it is applied. Both the optimization
and the programs to which the optimization applies are specied in the
strategy language Stratego. The optimization is based on small
transformation rules that are applied locally under the control of
strategies, using special knowledge about the contexts in which the
rules are applied.

**Online**

-   <http://www.elsevier.nl/locate/entcs/volume57.html>
-   <http://www.cs.uu.nl/people/visser/ftp/JV01.pdf>

------------------------------------------------------------------------

[CategoryPaper](../Transform/CategoryPaper){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
