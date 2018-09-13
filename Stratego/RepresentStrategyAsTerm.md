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
    Page](http://www.program-transformation.org/edit/Stratego/RepresentStrategyAsTerm?t=1536825663)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/RepresentStrategyAsTerm)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/RepresentStrategyAsTerm)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/RepresentStrategyAsTerm?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/RepresentStrategyAsTerm?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/RepresentStrategyAsTerm?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/RepresentStrategyAsTerm?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/RepresentStrategyAsTerm?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/RepresentStrategyAsTerm?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/RepresentStrategyAsTerm?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/RepresentStrategyAsTerm)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/RepresentStrategyAsTerm?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/RepresentStrategyAsTerm?template=oopsmore&param1=1.3&param2=1.3)
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
Represent Strategy As Term {#represent-strategy-as-term .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

By representing a strategy as a term, it can be passed around. This
requires an
[EvalStrategy[^?^](http://www.program-transformation.org/edit/Stratego/EvalStrategy?topicparent=Stratego.RepresentStrategyAsTerm)]{.twikiNewLink
style="background : #FFFFCE;"} operator that evaluates such a term. This
need not be a primitive;

Problems

-   How to distinghuish congruence strategies represented as terms from
    terms themselves?

<!-- -->

-   By declaring *constructors* for the strategies, a congruence
    operator is declared automatically. This should be avoided. That is,
    the user should not declare these constructors, but they should be
    generated implicitly from strategy definitions.

<!-- -->

-   Closures?

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 27 Oct 2001\

A possibility is to use a quotation mechanism in the style of
[MetaML](../Transform/MetaML){.twikiLink} and represent quoted stategies
internally using abstract syntax representation. This requires an
interpreter that maps calls to strategy operators, but has to interprete
ordinary combinators. This would make possible an integration of the
interpreter
[StrategoScript[^?^](http://www.program-transformation.org/edit/Stratego/StrategoScript?topicparent=Stratego.RepresentStrategyAsTerm)]{.twikiNewLink
style="background : #FFFFCE;"} with the
[StrategoCompiler](StrategoCompiler){.twikiLink}. In fact,
[StrategoScript[^?^](http://www.program-transformation.org/edit/Stratego/StrategoScript?topicparent=Stratego.RepresentStrategyAsTerm)]{.twikiNewLink
style="background : #FFFFCE;"} already calls C functions, i.e., the
Stratego primitives from the [Stratego standard
library[^?^](http://www.program-transformation.org/edit/Stratego/StrategoStandardLibrary?topicparent=Stratego.RepresentStrategyAsTerm)]{.twikiNewLink
style="background : #FFFFCE;"}.

[ELAN](../Transform/ELAN){.twikiLink} provides such a mechanism. The
idea of
[RewritingByRewriting[^?^](http://www.program-transformation.org/edit/Transform/RewritingByRewriting?topicparent=Stratego.RepresentStrategyAsTerm)]{.twikiNewLink
style="background : #FFFFCE;"} is based on this idea, if I remember
correctly.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 02 Nov 2001\

------------------------------------------------------------------------

[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.RepresentStrategyAsTerm)]{.twikiNewLink
style="background : #FFFFCE;"} \| [ToDo](ToDo){.twikiLink} \|
[LanguageExtensions](LanguageExtensions){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
