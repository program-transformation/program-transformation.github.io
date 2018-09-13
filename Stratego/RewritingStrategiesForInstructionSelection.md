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
    Page](http://www.program-transformation.org/edit/Stratego/RewritingStrategiesForInstructionSelection?t=1536825430)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/RewritingStrategiesForInstructionSelection)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/RewritingStrategiesForInstructionSelection)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/RewritingStrategiesForInstructionSelection?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/RewritingStrategiesForInstructionSelection?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/RewritingStrategiesForInstructionSelection?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/RewritingStrategiesForInstructionSelection?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/RewritingStrategiesForInstructionSelection?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/RewritingStrategiesForInstructionSelection?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/RewritingStrategiesForInstructionSelection?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/RewritingStrategiesForInstructionSelection?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/RewritingStrategiesForInstructionSelection)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/RewritingStrategiesForInstructionSelection?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/RewritingStrategiesForInstructionSelection?template=oopsmore&param1=1.4&param2=1.4)
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
M. Bravenboer and E. Visser. **Rewriting Strategies for Instruction
Selection.** In S. Tison, editor, Rewriting Techniques and Applications
(RTA\'02), volume 2378 of Lecture Notes in Computer Science, pages
237\--251, Copenhagen, Denmark, July 2002. Springer-Verlag.
([pdf](http://www.cs.uu.nl/~visser/ftp/BV02.pdf)).

### []{#Abstract} Abstract

Instruction selection (mapping IR trees to machine instructions) can be
expressed by means of rewrite rules. Typically, such sets of rewrite
rules are highly ambiguous. Therefore, standard rewriting engines based
on fixed, exhaustive strategies are not appropriate for the execution of
instruction selection. Code generator generators use special purpose
implementations employing dynamic programming. In this paper we show how
rewriting strategies for instruction selection can be encoded concisely
in Stratego, a language for program transformation based on the paradigm
of programmable rewriting strategies. This embedding obviates the need
for a language dedicated to code generation, and makes it easy to
combine code generation with other optimizations.

### []{#Bibtex} Bibtex

    @inproceedings{BV02,
      author    = {Martin Bravenboer and Eelco Visser},
      title     = {Rewriting Strategies for Instruction Selection},
      booktitle = {Rewriting Techniques and Applications (RTA'02)},
      pages     = {237-251},
      year      = 2002,
      editor    = {S. Tison},
      volume    = 2378,
      series    = {Lecture Notes in Computer Science},
      address   = {Copenhagen, Denmark},
      month     = {July},
      publisher = {Springer-Verlag},
      urlpdf    = {http://www.cs.uu.nl/people/visser/ftp/BV02.pdf},
      pubcat    = {conference},
    }

------------------------------------------------------------------------

[CategoryPaper](../Transform/CategoryPaper){.twikiLink} \|
[StrategoPublications](StrategoPublications){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
