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
    Page](http://www.program-transformation.org/edit/Stratego/RefactoringStrategies?t=1536825662)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/RefactoringStrategies)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/RefactoringStrategies)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/RefactoringStrategies?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/RefactoringStrategies?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/RefactoringStrategies?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/RefactoringStrategies?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/RefactoringStrategies?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/RefactoringStrategies)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/RefactoringStrategies?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/RefactoringStrategies?template=oopsmore&param1=1.2&param2=1.2)
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
Refactoring Strategies {#refactoring-strategies .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

**Description**

The design of Stratego specifications can be improved by
[ReFactoring](../Transform/ReFactoring){.twikiLink}. Here is a list of
refactorings. Please add to the list if you use missing refactorings.

**Refactorings**

-   [SplitChoice](SplitChoice){.twikiLink}

<!-- -->

-   Extract Strategy: take out a sub-expression from a strategy
    definition and give a name

<!-- -->

-   Extract Rule

<!-- -->

-   Inline Strategy

<!-- -->

-   Inline Rule

<!-- -->

-   Rename Label/operator

<!-- -->

-   Translate Strategy Into Rule: a strategy of the form ?t1; s1;
    \...;!t2 can be replaced by a rule

<!-- -->

-   Translate Rule Into Strategy: a rule with trivial lhs and rhs, but
    complex condition is often better expressed as a strategy (pipeline)

<!-- -->

-   Extract Module: place a set of rules and strategies in their own
    module

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.RefactoringStrategies moved from Stratego.StrategoRefactoring
on 29 Apr 2002 - 07:55 by
[EelcoVisser](../Main/EelcoVisser){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Stratego/RefactoringStrategies?newweb=Stratego&newtopic=StrategoRefactoring&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
