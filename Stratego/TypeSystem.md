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
    Page](http://www.program-transformation.org/edit/Stratego/TypeSystem?t=1536825715)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/TypeSystem)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/TypeSystem)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/TypeSystem?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/TypeSystem?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/TypeSystem?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/TypeSystem?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/TypeSystem?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/TypeSystem)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/TypeSystem?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/TypeSystem?template=oopsmore&param1=1.2&param2=1.2)
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
Type System {#type-system .twikiTopicTitle}
===========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Currently Stratego is very weakly typed. The reason for the weak type
system is that it is not clear how to combine strong typing with generic
traversals and transformations.

Here is a relevant quote (I don\'t remember where I got it from):

> Stefan Kahrs in \[Kah96\] discusses the notion of
> completeness\--programs which never go wrong can be
> type-checked\--which complements Milner\'s notion of
> soundness\--type-checked programs never go wrong \[Mil78\].

It is not difficult to make a sound type system for Stratego based on
standard type systems, but that would restrict the range of useful
Stratego programs too much. What is needed is a complete type system in
the sense of the citation that supports the full range of Stratego
programming.

Here are some properties that a type system might check

-   Given a term of this type, this strategy returns a term of that type
-   This strategy always succeeds
-   Given an initial term of this type or form, this strategy will
    succeed *and* transform it to a term in this format

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 1999\

By now there are several proposals for typing languages with generic
traversal strategies.
[RalfLaemmel](../Transform/RalfLaemmel){.twikiLink} proposes a typed
version of [SystemS](SystemS){.twikiLink}. It would be interesting to
implement his system in the
[StrategoCompiler](StrategoCompiler){.twikiLink} and see where it
breaks. \-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 22 Nov
2001\

------------------------------------------------------------------------

[ToDo](ToDo){.twikiLink} \| Contributions by
[EelcoVisser](../Main/EelcoVisser){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
