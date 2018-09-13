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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoPrettyPrinter?t=1536825678)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoPrettyPrinter)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoPrettyPrinter)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoPrettyPrinter?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoPrettyPrinter?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/StrategoPrettyPrinter?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/StrategoPrettyPrinter?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/StrategoPrettyPrinter?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/StrategoPrettyPrinter?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoPrettyPrinter?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoPrettyPrinter?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoPrettyPrinter)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoPrettyPrinter?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoPrettyPrinter?template=oopsmore&param1=1.4&param2=1.4)
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
Stratego Pretty Printer {#stratego-pretty-printer .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The definition of the [Stratego syntax](StrategoSyntax){.twikiLink} in
[StrategoXT 0.9](StrategoRelease09){.twikiLink} provides a pretty-print
table for Stratego programs. It does not yet support layout preservation
and is not always very pretty. It should be adequate for pretty-printing
generated Stratego code.

You can pretty print [Stratego abstract
syntax](StrategoAbstractSyntax){.twikiLink} with the StrategoXT
[XTC](XTC){.twikiLink} tools library. The module `stratego-xt-xtc-tools`
contains a strategy `xtc-pp-astratego`, which is defined as

      xtc-pp-astratego =
          xtc-stratego-ensugar
        ; xtc-ast2abox(!["Stratego-pretty.pp"])
        ; xtc-abox2text

You should prefer this strategy over your own composition because in the
future this strategy will solve priority and associativity problems.

------------------------------------------------------------------------

[CategoryPrettyPrint[^?^](http://www.program-transformation.org/edit/Stratego/CategoryPrettyPrint?topicparent=Stratego.StrategoPrettyPrinter)]{.twikiNewLink
style="background : #FFFFCE;"} \|
[MetaStratego](MetaStratego){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
