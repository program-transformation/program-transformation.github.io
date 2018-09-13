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
    Page](http://www.program-transformation.org/edit/Stratego/ConcreteSyntax?t=1536825552)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ConcreteSyntax)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ConcreteSyntax)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ConcreteSyntax?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ConcreteSyntax?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/ConcreteSyntax?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/ConcreteSyntax?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/ConcreteSyntax?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/ConcreteSyntax?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ConcreteSyntax?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ConcreteSyntax?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ConcreteSyntax)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ConcreteSyntax?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/ConcreteSyntax?template=oopsmore&param1=1.4&param2=1.4)
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
Concrete Syntax {#concrete-syntax .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[Abstract syntax](AbstractSyntax){.twikiLink} written using prefix
constructor terms can become rather unreadable when patterns become
large. Therefore it is attractrive to write [transformation
rules](TransformationRule){.twikiLink} using the concrete syntax of the
object language instead of its abstract syntax. For example, to write

      PlusZero :
         |[ e + 0 ]| -> |[ e ]|

instead of

      PlusZero :
         Plus(e, Int(0)) -> e

Starting with [StrategoRelease08](StrategoRelease08){.twikiLink}
concrete syntax is supported by Stratego. For a full account of this new
feature and its implementation see the paper [Meta Programming with
Concrete Object
Syntax](MetaProgrammingWithConcreteObjectSyntax){.twikiLink}.

------------------------------------------------------------------------

The techniques for handling embedded syntax in a meta-language have now
been generalized and are implemented in the `parse-cs` tool in the
[concrete syntax package](ConcreteSyntaxPackage){.twikiLink} in the
[StrategoXT](StrategoXT){.twikiLink} distribution. This tool has been
used in the embedding of concrete syntax in Prolog implemented in the
[Prolog tools](PrologTools){.twikiLink} package.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 28 Nov 2003

------------------------------------------------------------------------

[CategoryConcreteObjectSyntax](CategoryConcreteObjectSyntax){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
