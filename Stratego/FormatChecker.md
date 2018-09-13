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
    Page](http://www.program-transformation.org/edit/Stratego/FormatChecker?t=1536825582)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/FormatChecker)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/FormatChecker)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/FormatChecker?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/FormatChecker?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Stratego/FormatChecker?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/FormatChecker?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/FormatChecker?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/FormatChecker?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/FormatChecker?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/FormatChecker?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/FormatChecker)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/FormatChecker?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Stratego/FormatChecker?template=oopsmore&param1=1.6&param2=1.6)
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
Format Checker {#format-checker .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

A format checker is a strategy that checks the well-formedness of an
term. Format checkers can check more properties than can just be
described using signatures. For example, checking that a term is
normalized in a certain way.

Format checkers can be defined easily using
[RecursivePattern](RecursivePattern){.twikiLink}. Consider the following
signature of a simple expression language:

    signature
      sorts Exp
      constructors
        Var : String -> Exp
        Add : Exp * Exp -> Exp
        Mul : Exp * Exp -> Exp

The following format checking strategy `Exp` checks that a term is a
well-formed `Exp` term.

    strategies

      Exp = Var(is-string) + Add(Exp, Exp) + Mul(Exp, Exp)

It is also possible to check more strict properties such as being an
additive expression (if that is a term), i.e., an expression consisting
of additions on top and multiplications within. No addition should occur
as a sub-term of a multiplication. The following strategy definition is
a more concise way of expressing this property:

    AdditiveExp = 
      rec a(Add(a, a) + rec m(Mul(m, m) + Var(is-string)))

Note that the use of the `rec`
[RecursionOperator](RecursionOperator){.twikiLink} makes the definition
more concise (without it an additional strategy definition would be
needed).

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 28 Nov 2001\

The tool `format-check` (available from StrategoXT 0.10) checks if an
ATerm is part of the language defined by an abstract syntax definition
in [RTG](RegularTreeGrammar){.twikiLink}.

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 29 Jun
2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
