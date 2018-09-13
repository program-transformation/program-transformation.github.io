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
    Page](http://www.program-transformation.org/edit/Stratego/PrettyPrinter?t=1536825633)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/PrettyPrinter)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/PrettyPrinter)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/PrettyPrinter?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/PrettyPrinter?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Stratego/PrettyPrinter?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/PrettyPrinter?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/PrettyPrinter?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/PrettyPrinter?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/PrettyPrinter?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/PrettyPrinter?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/PrettyPrinter)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/PrettyPrinter?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Stratego/PrettyPrinter?template=oopsmore&param1=1.5&param2=1.5)
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
Pretty Printer {#pretty-printer .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

A [pretty printer](PrettyPrinter){.twikiLink} is a mapping from terms to
text. If this is done in a nice way, i.e., layout is placed in
appropriate places, the formatter deserves the term *pretty* printer.
For some applications, e.g., inspecting an intermediate term in a
transformation pipeline, an [ugly printer](UglyPrinter){.twikiLink} is
sufficient.

pretty printers can be defined manually, but that is a lot of work. A
better way is to use an intermediate format for representing layout
instructions and leaving the actual formatting to a tool that knows
about it.

The [generic pretty printing (gpp)](GPP){.twikiLink} package that comes
with [StrategoXT](StrategoXT){.twikiLink} provides tools for translating
terms to the [Box
language[^?^](http://www.program-transformation.org/edit/Stratego/BoxLanguage?topicparent=Stratego.PrettyPrinter)]{.twikiNewLink
style="background : #FFFFCE;"} and formatting the [Box
language[^?^](http://www.program-transformation.org/edit/Stratego/BoxLanguage?topicparent=Stratego.PrettyPrinter)]{.twikiNewLink
style="background : #FFFFCE;"} to text, html, and latex. The package
even supports generation of [pretty print
tables](../Tools/PrettyPrintTable){.twikiLink} from
[SDF](SDF){.twikiLink} syntax definitions.

If you need more control over pretty printing you can also write a
[pretty printer](PrettyPrinter){.twikiLink} with
[StrategoBox](StrategoBox){.twikiLink}. This approach uses [concrete
syntax](ConcreteSyntax){.twikiLink}for the [Box
language[^?^](http://www.program-transformation.org/edit/Stratego/BoxLanguage?topicparent=Stratego.PrettyPrinter)]{.twikiNewLink
style="background : #FFFFCE;"} inside the [Stratego
language](StrategoLanguage){.twikiLink}.

------------------------------------------------------------------------

[CategoryPrettyPrint[^?^](http://www.program-transformation.org/edit/Stratego/CategoryPrettyPrint?topicparent=Stratego.PrettyPrinter)]{.twikiNewLink
style="background : #FFFFCE;"}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
