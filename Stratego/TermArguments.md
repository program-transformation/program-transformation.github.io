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
    Page](http://www.program-transformation.org/edit/Stratego/TermArguments?t=1536825554)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/TermArguments)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/TermArguments)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/TermArguments?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/TermArguments?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/TermArguments?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/TermArguments)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/TermArguments?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/TermArguments?template=oopsmore&param1=1.1&param2=1.1)
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
Term Arguments {#term-arguments .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Starting with [StrategoRelease093](StrategoRelease093){.twikiLink},
strategy operators can be passed terms in addition to strategies.
Currently, a strategy definition is of the form

      f(s1, ..., sn) = body

where `body` is a strategy expression referring to the strategy
arguments `si`.

A term can be passed to such a strategy by passing a build, e.g.,
`foo(t)`. The receiving strategy accesses the term by executing the
corresponding strategy.

In certain situations, which arise for example in the compilation of
strategies, it is desirable to pass a term \'by value\'. Thus, the
syntax of Stratego has been extended to allow this. A strategy
definition now has the form

      f(s1,..., sn | x1, ..., xm) = body

where the `xi` are term arguments of `f`, which can be referred to
directly in match and build expressions. Such an operator is called
using the syntax `f(s1,...,sn|t1,...,tm)`

Note that the following sugar is defined:

-   `f(s1,...,sn) = body` is sugar for `f(s1,...,sn|) = body`
-   `f = body` is sugar for `f(|) = body`

and similarly for rules. Corresponding sugar holds for strategy calls:

-   `f(s1,...,sn)` is sugar for `f(s1,...,sn|)`
-   `f` is sugar for `f(|)`

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 23 Aug 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
