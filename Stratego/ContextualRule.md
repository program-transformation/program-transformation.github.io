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
    Page](http://www.program-transformation.org/edit/Stratego/ContextualRule?t=1536825572)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ContextualRule)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ContextualRule)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ContextualRule?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ContextualRule?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ContextualRule?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ContextualRule?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ContextualRule?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ContextualRule)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ContextualRule?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/ContextualRule?template=oopsmore&param1=1.2&param2=1.2)
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
Contextual Rule {#contextual-rule .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Description](ContextualRule#Description)
-   [Issues](ContextualRule#Issues)
-   [Contexts in Strategy](ContextualRule#Contexts_in_Strategy)
-   [Different Implementation](ContextualRule#Different_Implementation)
:::

------------------------------------------------------------------------

### []{#Description} Description

A *contextual rule* is a [rewrite rule](RewriteRule){.twikiLink} in
which the left-hand side and right-hand side terms contain contexts of
the form `x[t]`.

A typical example of a contextual rule is the following inlining rule:

      Inline : Let(x, e1, e2[Var(x)]) -> Let(x, e1, e2[e1])

The idea is that an occurrence of `Var(x) in =e2` is replaced with the
term `e1`.

Contextual rules are treated as syntactic sugar and translated to a
normal rule, which performs a traversal over the context subterm. The
inlining rule above is translated to the rule:

      Inline : 
        Let(x, e1, e2) -> Let(x, e1, e2')
        where <oncetd(?Var(x); !e1)> e2 => e2'

The traversal strategy `oncetd` is used to find an occurrence of
`Var(x)` and replace it with `e1`. Note that in the match of `Var(x)`,
the variable `x` is already bound by the match of the left-hand
`Let(x, e1, e2)` side of the rule.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 08 Jan 2002

Note that for many applications (such as inlining) [dynamic
rules](DynamicRule){.twikiLink} are often more appropriate than
contextual rules since they allow the replacement traversal and the
surrounding traversal to be merged.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 29 Jul 2003

------------------------------------------------------------------------

### []{#Issues} Issues

-   traversal strategy
-   multiple contexts
-   conditions
-   overlapping contextual rules
-   backtracking

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 08 Jan 2002

------------------------------------------------------------------------

### []{#Contexts_in_Strategy} Contexts in Strategy

I\'m trying to use context matching inside a strategy.

For example,

    rule1 : MyTerm(x[AnotherTerm]) -> MyTerm(x[AnotherTerm])

will match fine. but when I try to do it in a strategy the sc compiler
complains (not a term-expression: Con \....)

    strat1: ?MyTerm(x[AnotherTerm]) ; debug

So, can someone tell me how to do deep context matching inside a
strategy? I need to do this so that I can use the contents of a variable
as part of the search criteria. I can\'t see how to do this with a rule.

\-- DAN - 29 Jul 2003

That is correct; contexts are only implemented for rules.

Here are some ways to do it:

\(1) first match, then traverse

    ?MyTerm(x); where(<oncetd(?AnotherTerm)> x); debug

This actually corresponds to the desugaring of contextual rules. That
is, rule1 is really sugar for

       rule1 : MyTerm(x) -> MyTerm(x')
                 where <oncetd(?AnotherTerm1; !AnotherTerm2)> x => x'

\(2) Using [TermProject](TermProject){.twikiLink} you can abbreviate (1)
as

    ?MyTerm(<oncetd(?AnotherTerm)>); debug

you should note, however, that the debug will now print the subterm of
`MyTerm`. That is (2) is the same as

    ?MyTerm(x); <oncetd(?AnotherTerm)> x; debug 

that is (1) without the where surrounding the traversal.

\(3) If necessary you can of course use alternative traversals.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 29 Jul 2003

------------------------------------------------------------------------

### []{#Different_Implementation} Different Implementation

A different implementation of contexual rules is possible though. The
current implementation optimizes finding and replacing the holes in a
context. It is of course possible to treat matching and building with
context separately, just as is done with normal terms. This would mean
that a context match `?MyTerm(x[t])` would bind to `x` an object
representing the subterm of `MyTerm` with holes at the place (or places)
where t was found. A build `!MyTerm(x[t'])` would fill the holes with
`t'`. The more efficient implementation currently used might be
derivable from the more general one.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 29 Jul 2003

------------------------------------------------------------------------

[CategoryGlossary](CategoryGlossary){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
