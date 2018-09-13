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
    Page](http://www.program-transformation.org/edit/Stratego/PatternMatchCompilation?t=1536825605)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/PatternMatchCompilation)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/PatternMatchCompilation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/PatternMatchCompilation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/PatternMatchCompilation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/PatternMatchCompilation?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/PatternMatchCompilation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/PatternMatchCompilation?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/PatternMatchCompilation?template=oopsmore&param1=1.1&param2=1.1)
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
Pattern Match Compilation {#pattern-match-compilation .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The pattern match optimizer of the [Stratego
compiler](StrategoCompiler){.twikiLink} optimizes choices of strategies
guarded with a pattern match operation `?t`. A strategy of the form

       {xs1 : ?t1; s1} 
       <+ {xs2 : ?t2; s2}
       <+ ...
       <+ {xsn : ?tn; sn}

is transformed to a strategy of the form

       let f1(|ys1) = s1
           ...
           fn(|ysn) = sn
        in { zs :
             ?F1(z1,...,zn)
             < (!z1
                ; ?G1(z) 
                  < fi(|z1,...,zn)
                  + fail)
             + ?F2(zn+1,...,zn+m)
               < (fj(|zn+1,...,zn+m) <+ fk(|zn+1,...,zn+m)
               + ...
           }

In such a way that no constructor `Fi` is matched more than once at the
same node. That is, the patterns are merged as much as possible. If
there still exists overlap between two patterns, the continuation has a
choice between the continuations, as illustrated by the branch resulting
in a choice between `fj` and `fk`.

Pattern match compilation requires [strategy
inlining](StrategyInlining){.twikiLink} to ensure that the pattern
matches are actually exposed.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 14 Aug 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
