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
    Page](http://www.program-transformation.org/edit/Stratego/WorkerWrapperSplitting?t=1536825545)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/WorkerWrapperSplitting)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/WorkerWrapperSplitting)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/WorkerWrapperSplitting?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/WorkerWrapperSplitting?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/WorkerWrapperSplitting?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/WorkerWrapperSplitting)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/WorkerWrapperSplitting?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/WorkerWrapperSplitting?template=oopsmore&param1=1.1&param2=1.1)
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
Worker Wrapper Splitting {#worker-wrapper-splitting .twikiTopicTitle}
========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The `worker-wrapper` component of the [Stratego
optimizer](StrategoOptimizer){.twikiLink} splits strategy definitions
into a *wrapper* performing a pattern match, and a *worker* doing the
real work of the operator. That is, a definition of the form

      f(as1 | as2) = {xs : ?t ; s}

is split into the pair of definitions

      f(as1 | as2) = {xs : ?t ; g(as1 | as2, xs)}
      g(as1 | as2, xs) = s

Thus `f` is reduced to a small definition comprising only a match and a
call to the continuation `g`. The smaller definition for `f` becomes
attractive to inline, especially in the context of a choice where
[pattern match compilation](PatternMatchCompilation){.twikiLink} may
integrate it with other matches, or in the context of a build, which may
cancel against the match `?t`.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 17 Aug 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
