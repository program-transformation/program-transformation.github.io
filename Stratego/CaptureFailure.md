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
    Page](http://www.program-transformation.org/edit/Stratego/CaptureFailure?t=1536825566)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/CaptureFailure)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/CaptureFailure)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/CaptureFailure?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/CaptureFailure?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/CaptureFailure?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/CaptureFailure?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/CaptureFailure?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/CaptureFailure)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/CaptureFailure?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/CaptureFailure?template=oopsmore&param1=1.2&param2=1.2)
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
Capture Failure {#capture-failure .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Success and failure in Stratego allows one to avoid computing with
Boolean values all the time. However, sometimes it is necessary to
capture the failure (or success) of a strategy and translate it into a
term. For example, when performing [constant
folding[^?^](http://www.program-transformation.org/edit/Stratego/ConstantFolding?topicparent=Stratego.CaptureFailure)]{.twikiNewLink
style="background : #FFFFCE;"} of relational expressions one would like
to write

    ConstFold :
      |[ i < j ]| -> <lt>(i, j)

However, when the `lt` fails, the rule fails. What is needed is a little
wrapper strategy that turns failure and success into an appropriate
term.

    ConstFold :
      |[ i < j ]| -> <to-bool(<lt>(i,j))>

where `to-bool` could be defined as

    to-bool(s) =
      if s then
        !|[ true ]|
      else
        !|[ false ]|
      end

that is, when `s` succeeds return `true`, otherwise return `false`.

(Note that these examples use [concrete
syntax](ConcreteSyntax){.twikiLink}.)

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 17 Jun 2002\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
