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
    Page](http://www.program-transformation.org/edit/Stratego/PLogicProver?t=1536825496)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/PLogicProver)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/PLogicProver)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/PLogicProver?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/PLogicProver?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/PLogicProver?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/PLogicProver)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/PLogicProver?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/PLogicProver?template=oopsmore&param1=1.1&param2=1.1)
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
PLogic Prover {#plogic-prover .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

I thought I\'d give you an brief update on my attempt to build a
verification tool for P-logic, the logic for Haskell98 that we have
developed in the Programatica project. I\'m satisfied with the progress
made, though of course it is far from finished \-- a theorem-prover is
never finished as the task itself is incomplete.

I haven\'t used the parsing capabilities that have been integrated with
Stratego as we have our own, very capable front-end tool built by Thomas
Hallgren) for Haskell, which does parsing, slicing and type checking for
Haskell with embedded logical assertions. So it\'s a pure Stratego
exercise. There is is set of slides describing the current capabilities
of the theorem prover, under the title, \"Strategies for Verification\"
under the Presentations tab on the Programatica web page,
<http://www.cse.ogi.edu/PacSoft/projects/programatica/default.htm>

The cool thing about this verifier \-- and the sole motivation for
building it \-- is that it verifies properties directly expressed of
Haskell programs, rather than verifying properties of some model of
Haskell programs as translated into a generic functional language that
lacks the expressiveness of Haskell.

The existing theorem provers with which I\'m familiar don\'t make much
use of programmed strategies; many are based upon conditional rewriting
to control the application of rules. Some which attempt full automation
(like ACL2) use programmed heuristics to control things like the
selection of induction variables, a problem I have not yet confronted. A
big issue in a successful verifier is its ability to interact with
decision procedures for theories such as boolean algebra, linear
arithmetic, or lists. In principle, decision procedures can be
integrated in a Nelson-Oppen framework, but it isn\'t entirely clear how
to do this with \"black-box\" decision-procedure components. So far, I
have integrated only a congruence-closure decision procedure for
equalities, which I programmed in Stratego. This was pretty
straightforward and achieved a big improvement over programming equality
axioms as rewrite strategies.

So far, my experience confirms that Stratego is a great language for
programming a theorem prover. Although types could definitely be
helpful.

\-- Richard Kieburtz - 18 Jul 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
