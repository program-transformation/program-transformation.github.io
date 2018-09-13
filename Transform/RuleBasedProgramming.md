::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

[![](../pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Transform/RuleBasedProgramming?t=1536826557)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/RuleBasedProgramming)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/RuleBasedProgramming)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/RuleBasedProgramming?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/RuleBasedProgramming?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    13](http://www.program-transformation.org/view/Transform/RuleBasedProgramming?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/Transform/RuleBasedProgramming?rev1=1.13&rev2=1.12)
-   [Rev
    12](http://www.program-transformation.org/view/Transform/RuleBasedProgramming?rev=1.12)
    [(diff 11)](http://www.program-transformation.org/rdiff/Transform/RuleBasedProgramming?rev1=1.12&rev2=1.11)
-   [Rev
    11](http://www.program-transformation.org/view/Transform/RuleBasedProgramming?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/Transform/RuleBasedProgramming?rev1=1.11&rev2=1.10)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/RuleBasedProgramming)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/RuleBasedProgramming?template=oopsmore&param1=1.13&param2=1.13)
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
    \...](http://www.program-transformation.org/oops/Transform/RuleBasedProgramming?template=oopsmore&param1=1.13&param2=1.13)
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
Rule Based Programming {#rule-based-programming .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Definitions**

Here are some attempts at definitions of rule-based programming. Feel
free to comment or add your own.

-   The rule-based programming paradigm is characterized by the
    repeated, usually exhaustive, localized transformations of a shared
    data object (e.g., term, graph, proof, constraint store, \...). The
    transformations are described by *rules* which seperate the
    description of the (sub-) object to be replaced (the *pattern*) from
    the calculation of the replacement; optionally, *conditional rules*
    can have further conditions that restrict their applicability. The
    transformations are controlled by explicit or implicit *strategies*.

A rule-based program consists of a collection of rules.

A rule consists of a pattern that describes how it can be applied and an
action that describes what should be done when the rule is applied.

Optionally, a rule can have further conditions that restrict the
applicability of the rule.

An implicit strategy exhaustively applies rules.

**Ingredients**

Here are some typical ingredients of rule-based systems

-   three-level decomposition:
    -   strategy control: which rule to test/apply where
    -   application control: test for rule applicability is seperated
        from performed calculation
    -   calculation

<!-- -->

-   variation can occur on all three levels: built-in vs.
    (meta-)programmed strategies, term rewriting vs. graph rewriting,
    functional vs. imperative calculation

<!-- -->

-   computation is performed on a shared datastructure (term to be
    normalized, program to be transformed, constraint store,
    theorem,\...); however, each rule application is localized / usually
    affects only a part of the datastructure

<!-- -->

-   rule-based computation is communication-free, i.e., no
    message-passing; everything is exchanged via the shared
    datastructure

<!-- -->

-   rule-based computation has no explicit control flow (done by the
    strategy)

<!-- -->

-   rules are oriented (as opposed to equations) and usually memory-less

<!-- -->

-   the order of rules does not matter

<!-- -->

-   rules compose (easily), either as union of consequences, or as union
    of rule sets

**Application Areas**

-   Document transformation and presentation ([XML](XML){.twikiLink})

<!-- -->

-   Software building (Make)
-   Agent systems

<!-- -->

-   [ProgramTransformation](ProgramTransformation){.twikiLink}
-   Software configuration (Linux kernel)
-   Expert systems
-   Parsing (context-free grammars)
-   Pretty-printing ([GPP](../Tools/GPP){.twikiLink})
-   Theorem proving
-   Tree automata
-   E-Mail address normalization
-   Semantics
-   Transition systems

**Formalims**

-   [TermRewriting](TermRewriting){.twikiLink}
-   [LogicProgramming[^?^](http://www.program-transformation.org/edit/Transform/LogicProgramming?topicparent=Transform.RuleBasedProgramming)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [RewritingStrategies](RewritingStrategy){.twikiLink}
-   [RewritingLogic[^?^](http://www.program-transformation.org/edit/Transform/RewritingLogic?topicparent=Transform.RuleBasedProgramming)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [ContextFreeGrammars](ContextFreeGrammar){.twikiLink}
-   [PrettyPrintTables[^?^](http://www.program-transformation.org/edit/Transform/PrettyPrintTables?topicparent=Transform.RuleBasedProgramming)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [AttributeGrammars](AttributeGrammar){.twikiLink}

**Languages and Systems**

Specific systems for rule-based programming

-   [ELAN](ELAN){.twikiLink}:
    [RewritingStrategies](RewritingStrategy){.twikiLink}
-   Prolog:
    [LogicProgramming[^?^](http://www.program-transformation.org/edit/Transform/LogicProgramming?topicparent=Transform.RuleBasedProgramming)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   Stratego: [RewritingStrategies](RewritingStrategy){.twikiLink}
-   Mathematica
-   Maude
-   OBJ
-   Claire
-   [ASFandSDF](ASFandSDF){.twikiLink}
-   [LRR](LRR){.twikiLink}
-   [IlogRules](IlogRules){.twikiLink}
-   [EclipseLanguage](EclipseLanguage){.twikiLink}

Collections of rule-based programming systems

-   [RuleBasedProgrammingSystems](RuleBasedProgrammingSystems){.twikiLink}
-   [TermRewritingSystems](TermRewritingSystems){.twikiLink}
-   [TransformationSystems](TransformationSystems){.twikiLink}

**Issues in Rule Based Programming**

-   Control over application of rules
-   Strategies
-   Context-dependent rules
-   Dynamic rules

<!-- -->

-   Algorithmic complexity
-   Optimization of rule-based programs
-   Semantics
-   Compilation and interpretation

**Workshops and conferences**

-   [WorkshopOnRuleBasedProgramming](WorkshopOnRuleBasedProgramming){.twikiLink}
-   [WorkshopOnRuleBasedConstraintReasoningAndProgramming](WorkshopOnRuleBasedConstraintReasoningAndProgramming){.twikiLink}

**Books**

-   [Rule-Based Programming](http://www.wkap.nl/prod/b/0-7923-9769-X) by
    [ThaddeusKowalski[^?^](http://www.program-transformation.org/edit/Transform/ThaddeusKowalski?topicparent=Transform.RuleBasedProgramming)]{.twikiNewLink
    style="background : #FFFFCE;"} and
    [LeonLevy[^?^](http://www.program-transformation.org/edit/Transform/LeonLevy?topicparent=Transform.RuleBasedProgramming)]{.twikiNewLink
    style="background : #FFFFCE;"}

------------------------------------------------------------------------

[CategoryParadigm](CategoryParadigm){.twikiLink} \|
[CategoryRuleBased[^?^](http://www.program-transformation.org/edit/Transform/CategoryRuleBased?topicparent=Transform.RuleBasedProgramming)]{.twikiNewLink
style="background : #FFFFCE;"} \| Contributions by
[EelcoVisser](../Main/EelcoVisser){.twikiLink},
[BerndFischer](../Main/BerndFischer){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
