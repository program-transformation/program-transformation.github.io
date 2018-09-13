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
    Page](http://www.program-transformation.org/edit/Stratego/ExtendingDynamicRules?t=1536825425)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ExtendingDynamicRules)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ExtendingDynamicRules)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ExtendingDynamicRules?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ExtendingDynamicRules?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ExtendingDynamicRules?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ExtendingDynamicRules?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/ExtendingDynamicRules?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ExtendingDynamicRules)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ExtendingDynamicRules?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/ExtendingDynamicRules?template=oopsmore&param1=1.2&param2=1.2)
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
Extending Dynamic Rules {#extending-dynamic-rules .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

A. van Dam. **Extending Dynamic Rules. An Application-Oriented Study
into Stratego\'s new Dynamic Rules.** Master\'s thesis, Utrecht
University, Utrecht, The Netherlands, February 2004. INF/SCR-04-25
([pdf](http://www.cs.uu.nl/~visser/ftp/Dam04.pdf)).

### []{#From_the_Introduction} From the Introduction

The research described in this thesis is part of ongoing work in the
development of the Stratego system \[VBT98, Vis00, Vis04a\]. Focus lies
on the concept of dynamic rules that allow the use of context
information in rewrite rules, thus making more sophisticated rewriting
possible. Dynamic rules were introduced in Stratego 0.6, and had some
occasional improvements up to and including Stratego 0.9.3. We will
sometimes refer to this 0.9.3 release as the old-style dynamic rules. In
Stratego 0.9.4 the extend rules feature was already silently introduced,
but a major redesign including many new features was released in
Stratego 0.10, followed by some small internal optimizations in 0.11. At
the time of writing Stratego 0.11 reflects the current state of our
research.

### []{#Outline} Outline

To describe the context in which this research was performed, Chapter 2
introduces the key parts of the Stratego language. Readers who are
already familiar with the Stratego language constructs may skip this
chapter, although the formal semantics described within will come back
in the semantics of dynamic rules. Appendix A contains all formal
semantics in one overview. Chapter 3 further explains the need for
context-aware rewriting and describes the dynamic rule constructs that
were available in the old-style dynamic rules, i.e. as in Stratego 0.9.3
and before.

Chapters 4, 5 and 6 describe three cases where dynamic rules are used in
some optimizing transformation. Starting the reasoning from the
old-style dynamic rules, undesirable or missing features of these
dynamic rules are identified, and a solution described. Chapter 4
introduces a small lambda calculus and a shrinking optimizer, based on
an article by Andrew Appel and Trevor Jim \[AJ97\]. Basic rule
definition and rule scoping is of importance here. Chapter 5 describes
constant propagation in the Tiger language. Previous work on this matter
was done by Olmos and Visser \[OV02\], but new dynamic rules enable a
cleaner implementation of constant propagation. Rule undefining, dynamic
scoping and proper handling of control flow (i.e. forking and meeting of
dynamic rule environments) are the important issues here. Chapter 6 is a
study built around the deforestation algorithm for first-order
functional languages described by Philip Wadler \[Wad90\].
Implementation of the deforestation algorithm shows the need for
extending rule sets an higher-order matching. Within the same study,
also a type inferencer was implemented, which allows for a comparison
between type inferencing using attribute grammars (e.g. as implemented
\[DS01\] in the UUAG system) and type inferencing using dynamic rule
sets. Both implementations are based on the W algorithm by Milner
\[Mil78, DM82\]. To keep the original chapter focused on deforestation,
the type inferencer is described separately in Appendix B. Each case
thus introduces one or more improvements or new features of dynamic
rules in Stratego, and altogether they form the new set of dynamic rule
constructs as they were initially released in Stratego 0.10.

Most new features of dynamic rules have been made possible by a smarter
representation of rule sets and scopes. Chapter 7 describes how stacks
of hash tables provide the appropriate functionality and efficiency. The
supposed efficiency of the new rule set representation has been
benchmarked. Chapter 8 describes these benchmarks, compares the results
to the expected qualitative costs behavior and concludes which
constructs are the most costly.

Chapters 9 and 10 describe related and future work and Chapter 11
concludes.

### []{#BibTeX} [BibTeX](BibTeX){.twikiLink}

    @mastersthesis{Dam04,
      author  = {Arthur van Dam},
      title   = {Extending Dynamic Rules. {A}n Application-Oriented Study into {Stratego's} new Dynamic Rules},
      school  = {Utrecht University},
      year    = 2004,
      address = {Utrecht, The Netherlands},
      month   = {February},
      note    = {INF/SCR-04-25},
      urlpdf  = {http://www.cs.uu.nl/~visser/ftp/Dam04.pdf},
      project = {Stratego},
    }

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
