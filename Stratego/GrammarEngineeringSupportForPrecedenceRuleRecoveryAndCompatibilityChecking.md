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
    Page](http://www.program-transformation.org/edit/Stratego/GrammarEngineeringSupportForPrecedenceRuleRecoveryAndCompatibilityChecking?t=1536825427)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/GrammarEngineeringSupportForPrecedenceRuleRecoveryAndCompatibilityChecking)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/GrammarEngineeringSupportForPrecedenceRuleRecoveryAndCompatibilityChecking)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/GrammarEngineeringSupportForPrecedenceRuleRecoveryAndCompatibilityChecking?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/GrammarEngineeringSupportForPrecedenceRuleRecoveryAndCompatibilityChecking?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/GrammarEngineeringSupportForPrecedenceRuleRecoveryAndCompatibilityChecking?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/GrammarEngineeringSupportForPrecedenceRuleRecoveryAndCompatibilityChecking)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/GrammarEngineeringSupportForPrecedenceRuleRecoveryAndCompatibilityChecking?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/GrammarEngineeringSupportForPrecedenceRuleRecoveryAndCompatibilityChecking?template=oopsmore&param1=1.1&param2=1.1)
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
Grammar Engineering Support for Precedence Rule Recovery and Compatibility Checking {#grammar-engineering-support-for-precedence-rule-recovery-and-compatibility-checking .twikiTopicTitle}
===================================================================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[Eric Bouwers](http://ericbouwers.blogspot.com), [Martin
Bravenboer](http://martin.bravenboer.name), and [Eelco
Visser](http://www.cs.uu.nl/wiki/Visser/WebHome). **Grammar Engineering
Support for Precedence Rule Recovery and Compatibility Checking**. In
*Proceedings of [LDTA\'07](http://www.di.uminho.pt/ldta07/), Seventh
Workshop on Language Descriptions, Tools and Applications at ETAPS\'07*,
Braga, Portugal, March 2007.
([pdf](http://martin.bravenboer.name/docs/ldta07.pdf),
[implementation](http://www.stratego-language.org/Stratego/GrammarEngineeringTools))

### []{#Abstract} Abstract

A wide range of parser generators are used to generate parsers for
programming languages. The grammar formalisms that come with parser
generators provide different approaches for defining operator
precedence. Some generators (e.g. YACC) support precedence declarations,
others require the grammar to be unambiguous, thus encoding the
precedence rules. Even if the grammar formalism provides precedence
rules, a particular grammar might not use it.

The result is grammar variants implementing the same language. For the C
language, the GNU Compiler uses YACC with precedence rules, the
C-Transformers uses [SDF](SDF){.twikiLink} without priorities, while the
[SDF](SDF){.twikiLink} library does use priorities. For PHP, Zend uses
YACC with precedence rules, whereas PHP-front uses
[SDF](SDF){.twikiLink} with priority and associativity declarations.

The variance between grammars raises the question if the precedence
rules of one grammar are compatible with those of another. This is
usually not obvious, since some languages have complex precedence rules.
Also, for some parser generators the semantics of precedence rules is
defined operationally, which makes it hard to reason about their effect
on the defined language.

We present a method and tool for comparing the precedence rules of
different grammars and parser generators. Although it is undecidable
whether two grammars define the same language, this tool provides
support for comparing and recovering precedence rules, which is
especially useful for reliable migration of a grammar from one grammar
formalism to another. We evaluate our method by the application to
non-trivial mainstream programming languages, such as PHP and C.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
