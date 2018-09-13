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
    Page](http://www.program-transformation.org/edit/Stratego/ReferenceCard?t=1536825555)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ReferenceCard)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ReferenceCard)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ReferenceCard?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ReferenceCard?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ReferenceCard?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ReferenceCard?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ReferenceCard?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ReferenceCard)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ReferenceCard?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/ReferenceCard?template=oopsmore&param1=1.2&param2=1.2)
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
Reference Card {#reference-card .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The data-flow diagram below shows the main tools from the
[StrategoXT](StrategoXT){.twikiLink} and SDF2 packages. The red edges
indicate the standard composition of a transformation system consisting
of a parser, a transformation component (`trafo`), and a pretty-printer
for programs in language `Lang`. The blue edges show the generation of
components for this transformation system. The black edges show other
tools.

Composition of a transformation system using files

-   `sglri -p Lang.tbl -i file.lang -o file.ast`
-   `trafo -i file.ast -o file-trafo.ast`
-   `ast2text -p Lang.pp -i file-trafo.ast -o file-trafo.lang`

using pipes

-   `sglri -p Lang.tbl -i file.lang | trafo | ast2text -p Lang.pp -o file-trafo.lang`

![refcard.gif](http://www.stratego-language.org/refcard.gif)

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 11 Jan 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
