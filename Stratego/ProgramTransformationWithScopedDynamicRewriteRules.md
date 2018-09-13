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
    Page](http://www.program-transformation.org/edit/Stratego/ProgramTransformationWithScopedDynamicRewriteRules?t=1536825425)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ProgramTransformationWithScopedDynamicRewriteRules)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ProgramTransformationWithScopedDynamicRewriteRules)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ProgramTransformationWithScopedDynamicRewriteRules?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ProgramTransformationWithScopedDynamicRewriteRules?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/ProgramTransformationWithScopedDynamicRewriteRules?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/ProgramTransformationWithScopedDynamicRewriteRules?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ProgramTransformationWithScopedDynamicRewriteRules?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ProgramTransformationWithScopedDynamicRewriteRules?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ProgramTransformationWithScopedDynamicRewriteRules?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ProgramTransformationWithScopedDynamicRewriteRules)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ProgramTransformationWithScopedDynamicRewriteRules?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/ProgramTransformationWithScopedDynamicRewriteRules?template=oopsmore&param1=1.3&param2=1.3)
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
M. Bravenboer, A. van Dam, K. Olmos, and E. Visser. **Program
Transformation with Scoped Dynamic Rewrite Rules.** Fundamenta
Informaticae, 69:1\--56, 2005.
([techrep](http://www.cs.uu.nl/research/techreps/UU-CS-2005-005.html))

### []{#Abstract} Abstract

The applicability of term rewriting to program transformation is limited
by the lack of control over rule application and by the context-free
nature of rewrite rules. The first problem is addressed by languages
supporting user-definable rewriting strategies. The second problem is
addressed by the extension of rewriting strategies with scoped dynamic
rewrite rules. Dynamic rules are defined at run-time and can access
variables available from their definition context. Rules defined within
a rule scope are automatically retracted at the end of that scope. In
this paper we explore the design space of dynamic rules, their
application to transformation problems, and their implementation. The
technique is formally defined by extending the operational semantics
underlying the program transformation language Stratego, and illustrated
by means of several program tranformations in Stratego, including
constant propagation, bound variable renaming, dead code elimination,
function inlining, and function specialization.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
