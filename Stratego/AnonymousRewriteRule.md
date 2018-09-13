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
    Page](http://www.program-transformation.org/edit/Stratego/AnonymousRewriteRule?t=1536825564)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/AnonymousRewriteRule)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/AnonymousRewriteRule)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/AnonymousRewriteRule?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/AnonymousRewriteRule?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/AnonymousRewriteRule?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/AnonymousRewriteRule)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/AnonymousRewriteRule?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/AnonymousRewriteRule?template=oopsmore&param1=1.1&param2=1.1)
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
Anonymous Rewrite Rule {#anonymous-rewrite-rule .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

An [anonymous rewrite rule](AnonymousRewriteRule){.twikiLink} is a
[rewrite rule](RewriteRule){.twikiLink} that can be used inside a
stategy expression.

An anonymous rewrite rule of the form:

    \ p1 -> p2 where s \ 

is desugared to

    {x1, ..., xn : ?p1; where(s); !p2} 

where x1, \..., xn are the free variables of `p1`. Any free variables
used in `s` and `p2`, which do not occur in `p1` are bound in the
context of the anonymous rewrite rule.

An anonymous rewrite rule of the form:

    ( p1 -> p2 where s ) 

is desugared to

    (?p1; where(s); !p2)

This style doesn\'t imply any scope for the variables of the rule: it
only provides rule-like syntax. The variables of p1, s and p2 are all
bound in the context of the anonymous rewrite rule.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
