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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRegular?t=1536825679)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRegular)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRegular)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRegular?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRegular?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    22](http://www.program-transformation.org/view/Stratego/StrategoRegular?rev=1.22)
    [(diff 21)](http://www.program-transformation.org/rdiff/Stratego/StrategoRegular?rev1=1.22&rev2=1.21)
-   [Rev
    21](http://www.program-transformation.org/view/Stratego/StrategoRegular?rev=1.21)
    [(diff 20)](http://www.program-transformation.org/rdiff/Stratego/StrategoRegular?rev1=1.21&rev2=1.20)
-   [Rev
    20](http://www.program-transformation.org/view/Stratego/StrategoRegular?rev=1.20)
    [(diff 19)](http://www.program-transformation.org/rdiff/Stratego/StrategoRegular?rev1=1.20&rev2=1.19)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRegular)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRegular?template=oopsmore&param1=1.22&param2=1.22)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRegular?template=oopsmore&param1=1.22&param2=1.22)
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
Stratego Regular {#stratego-regular .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#Introduction} Introduction
------------------------------

Stratego Regular is a package of tools for working with tree languages.
A tree language is a set of trees define by a tree grammar. Stratego
Regular defines the [concrete](ConcreteSyntax){.twikiLink} and [abstract
syntax](AbstractSyntax){.twikiLink} of **RTG**, a language for [regular
tree grammars](RegularTreeGrammar){.twikiLink}. The RTG language is used
to define tree languages.

[]{#Tools} Tools
----------------

-   [sdf2rtg](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/ref-sdf2rtg.html)
    \-- generates an abstract syntax definition in
    [RTG](RegularTreeGrammar){.twikiLink} from an [SDF](SDF){.twikiLink}
    syntax definition.
-   [rtg2sig](../Tools/RtgToSig){.twikiLink} \-- generates a [Stratego
    signature](StrategoSignature){.twikiLink} from an abstract syntax
    definition in [RTG](RegularTreeGrammar){.twikiLink}.
-   [format-check](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/format-checking.html)
    \-- Check if an ATerm is part of the language defined by an
    [RTG](RegularTreeGrammar){.twikiLink}.
-   [rtg2typematch](../Tools/RtgToTypeMatch){.twikiLink} \-- Generates a
    duck-typing based strategy that checks if an ATerm is of a type
    defined in an [RTG](RegularTreeGrammar){.twikiLink}.

[]{#Download_and_Installation} Download and Installation
--------------------------------------------------------

Stratego Regular is part of [StrategoXT](StrategoXT){.twikiLink} from
[release 0.10](StrategoRelease010){.twikiLink}.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
