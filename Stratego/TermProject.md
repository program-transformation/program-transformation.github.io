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
    Page](http://www.program-transformation.org/edit/Stratego/TermProject?t=1536825559)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/TermProject)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/TermProject)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/TermProject?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/TermProject?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/TermProject?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/TermProject?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/TermProject?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/TermProject?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/TermProject?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/TermProject?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/TermProject)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/TermProject?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/TermProject?template=oopsmore&param1=1.4&param2=1.4)
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
Term Project {#term-project .twikiTopicTitle}
============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[TermProject](TermProject){.twikiLink} patterns simplify projection of
sub-terms. A strategy application inside a match pattern selects the
corresponding sub-term and applies s to it. For example, instead of
writing

    A : Typed(Var(x),_) -> x

it is now possible to write

    A = ?Typed(Var(<id>),_)

This feature can also be used to perform tests on subterm in a match
pattern, e.g., the pattern

    ?[x | <not([])>]

binds the head of a list to `x`, checks that the tail is not empty and
produces the tail as result.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.TermProject moved from Stratego.MatchProject on 09 Dec 2001 -
14:42 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Stratego/TermProject?newweb=Stratego&newtopic=MatchProject&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
