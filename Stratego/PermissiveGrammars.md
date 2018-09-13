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
    Page](http://www.program-transformation.org/edit/Stratego/PermissiveGrammars?t=1536825606)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/PermissiveGrammars)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/PermissiveGrammars)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/PermissiveGrammars?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/PermissiveGrammars?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    21](http://www.program-transformation.org/view/Stratego/PermissiveGrammars?rev=1.21)
    [(diff 20)](http://www.program-transformation.org/rdiff/Stratego/PermissiveGrammars?rev1=1.21&rev2=1.20)
-   [Rev
    20](http://www.program-transformation.org/view/Stratego/PermissiveGrammars?rev=1.20)
    [(diff 19)](http://www.program-transformation.org/rdiff/Stratego/PermissiveGrammars?rev1=1.20&rev2=1.19)
-   [Rev
    19](http://www.program-transformation.org/view/Stratego/PermissiveGrammars?rev=1.19)
    [(diff 18)](http://www.program-transformation.org/rdiff/Stratego/PermissiveGrammars?rev1=1.19&rev2=1.18)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/PermissiveGrammars)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/PermissiveGrammars?template=oopsmore&param1=1.21&param2=1.21)
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
    \...](http://www.program-transformation.org/oops/Stratego/PermissiveGrammars?template=oopsmore&param1=1.21&param2=1.21)
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
The Permissive Grammars Project {#the-permissive-grammars-project .twikiTopicTitle}
===============================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

This page reports on the permissive grammars project. This project is
aimed at adding practical error recovery to the [Java
implementation](JSGLR){.twikiLink} of [SGLR](SGLR){.twikiLink}, for
interactive parsing of stand-alone and composite programming languages
using [SDF](SDF){.twikiLink}.

The base idea of the permissive grammars project is simple: given an
[SDF](SDF){.twikiLink} grammar, we derive a *permissive grammar* \[1\]
that also accepts programs with minor errors (missing brackets, etc.).
These grammars are normal [SDF](SDF){.twikiLink} grammars and can be
tweaked by the language engineer. Using a specialized version of the
[SGLR](SGLR){.twikiLink} algorithm, both syntactically correct and
incorrect programs can be efficiently parsed using these grammars \[1\].
As a refinement of these techniques, we also use indentation to
constrain the search space of error recovery suggestions and to provide
better error recovery suggestions \[2\].

[]{#Implementation} Implementation
----------------------------------

Automatic generation of permissive grammars and use of error recovery in
Eclipse has been integrated to and is automatically supported in the
[Spoofax language workbench](../Spoofax/WebHome){.twikiLink}.

[]{#Presentations} Presentations
--------------------------------

The slides of our OOPSLA 2009 presentation, explaining the core recovery
mechanism, are available here: [Providing Rapid Feedback in Generated
Modular Language
Environments](http://www.lclnet.nl/publications/error-recovery-presentation.pdf).

The presentation of our followup work at SLE 2009 can be downloaded
here: [Natural and Flexible Error Recovery for Generated
Parsers](http://strategoxt.org/pub/Stratego/PermissiveGrammars/natural-and-flexible-error-recovery-presentation.pdf).

[]{#Publications} Publications
------------------------------

 \[2\]
:   [Maartje de
    Jonge](http://swerl.tudelft.nl/bin/view/Main/MaartjeDeJonge), [Emma
    Nilsson-Nyman](http://www.cs.lth.se/home/Emma.Nilsson_Nyman/),
    [Lennart C. L. Kats](../Main/LennartKats){.twikiLink}, [Eelco
    Visser](../Main/EelcoVisser){.twikiLink}. **Natural and Flexible
    Error Recovery for Generated Parsers.** In Mark van den Brand, Jeff
    Gray, editors, *Proceedings of Software Language Engineering ([SLE
    2009](http://planet-sl.org/sle2009/))*, pages 204-223, Lecture Notes
    in Computer Science, Springer, 2009.
    ([abstract](http://www.lclnet.nl/publications/natural-and-flexible-error-recovery))
    ([pdf](http://www.lclnet.nl/publications/TUD-SERG-2009-024.pdf))
    ([bib](http://www.lclnet.nl/publications/JNKV09.bib))

<!-- -->

 \[1\]
:   [Lennart C. L. Kats](../Main/LennartKats){.twikiLink}, [Maartje de
    Jonge](http://swerl.tudelft.nl/bin/view/Main/MaartjeDeJonge), [Emma
    Nilsson-Nyman](http://www.cs.lth.se/home/Emma.Nilsson_Nyman/),
    [Eelco Visser](../Main/EelcoVisser){.twikiLink}. **Providing Rapid
    Feedback in Generated Modular Language Environments. Adding Error
    Recovery to Scannerless Generalized-LR Parsing.** In Gary T.
    Leavens, editor, *Proceedings of the 24th ACM SIGPLAN Conference on
    Object-Oriented Programming, Systems, Languages, and Applications
    ([OOPSLA 2009](http://www.oopsla.org/))*, pages 445-464, ACM, 2009.
    ([abstract](http://www.lclnet.nl/publications/error-recovery))
    ([pdf](http://www.lclnet.nl/publications/TUD-SERG-2009-020.pdf))
    ([bib](http://www.lclnet.nl/publications/KJNV09.bib))

[]{#Downloads} Downloads
------------------------

The test set (input files and grammars), permissive grammar derivation
tool, and stand-alone recovery tool can be found at:

<https://svn.strategoxt.org/repos/StrategoXT/sglr-recovery/trunk>

The implementation of [JSGLR](JSGLR){.twikiLink} has been adapted to
include the error recovery algorithm:

<https://svn.strategoxt.org/repos/StrategoXT/spoofax/trunk>

The components above are applied in the
[Spoofax/IMP](http://strategoxt.org/Stratego/Spoofax-IMP) editor trunk
series at:

<https://svn.strategoxt.org/repos/StrategoXT/spoofax-imp/trunk>

### []{#Grammars_and_Test_Sets} Grammars and Test Sets

We generated a number of grammars for languages including Java,
Stratego, and Stratego-Java. These grammars can be downloaded from this
page:

-   [grammars.zip](http://strategoxt.org/pub/Stratego/PermissiveGrammars//grammars.zip)

The Java test set can also be found here:

-   [java-test-set.zip](http://strategoxt.org/pub/Stratego/PermissiveGrammars//java-test-set.zip)

[]{#Contact_and_Mailing_List} Contact and Mailing List
------------------------------------------------------

Please send questions or feedback to the [users\@strategoxt.org mailing
list](https://mailman.st.ewi.tudelft.nl/listinfo/users) or directly to
the authors (listed above). We\'d be interested in any form of feedback
or discussing ideas of applying these techniques in a different context.
Also, the developers are usually available on IRC at [\#spoofax on
freenode.net](irc://irc.freenode.net/spoofax) ([web
version](http://java.freenode.net/index.php?channel=stratego)). Feel
free to drop by!

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
