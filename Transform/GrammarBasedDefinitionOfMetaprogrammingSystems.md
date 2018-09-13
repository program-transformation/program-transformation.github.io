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
    Page](http://www.program-transformation.org/edit/Transform/GrammarBasedDefinitionOfMetaprogrammingSystems?t=1536826400)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/GrammarBasedDefinitionOfMetaprogrammingSystems)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/GrammarBasedDefinitionOfMetaprogrammingSystems)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/GrammarBasedDefinitionOfMetaprogrammingSystems?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/GrammarBasedDefinitionOfMetaprogrammingSystems?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/GrammarBasedDefinitionOfMetaprogrammingSystems?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/GrammarBasedDefinitionOfMetaprogrammingSystems)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/GrammarBasedDefinitionOfMetaprogrammingSystems?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/GrammarBasedDefinitionOfMetaprogrammingSystems?template=oopsmore&param1=1.1&param2=1.1)
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
Grammar Based Definition Of Metaprogramming Systems {#grammar-based-definition-of-metaprogramming-systems .twikiTopicTitle}
===================================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[Robert
Cameron[^?^](http://www.program-transformation.org/edit/Transform/RobertCameron?topicparent=Transform.GrammarBasedDefinitionOfMetaprogrammingSystems)]{.twikiNewLink
style="background : #FFFFCE;"} and [Robert
Ito[^?^](http://www.program-transformation.org/edit/Transform/RobertIto?topicparent=Transform.GrammarBasedDefinitionOfMetaprogrammingSystems)]{.twikiNewLink
style="background : #FFFFCE;"}. **Grammar-Based Definition of
Metaprogramming Systems**. *ACM Transactions on Programming Languages
and Systems* Vol. 6, No. 1, January 1984, Pages 20-54. ([ACM Digital
Library](http://portal.acm.org/citation.cfm?id=357233.357235&coll=portal&dl=ACM&idx=J783&part=transaction&WantType=transaction&title=ACM%20Transactions%20on%20Programming%20Languages%20and%20Systems%20%28TOPLAS%29&CFID=2999757&CFTOKEN=28486623))

### []{#Summary} Summary

This paper describes the [GRAMPS](GRAMPS){.twikiLink} method for
meta-programming. [GRAMPS](GRAMPS){.twikiLink} stands for GRAmmar-based
[MetaProgramming](MetaProgramming){.twikiLink} Scheme. The method
basically describes how [abstract syntax
tree[^?^](http://www.program-transformation.org/edit/Transform/AbstractSyntaxTree?topicparent=Transform.GrammarBasedDefinitionOfMetaprogrammingSystems)]{.twikiNewLink
style="background : #FFFFCE;"} manipulation can be done in a
general-purpose programming language. Given an [API](API){.twikiLink}
for analyzing and constructing syntax trees, transformations can be
expressed. For example, the transformation

      repeat statement-list until true   ===>   begin statement-list end

is programmed as

      if NodeType(stmt) = RepeatLoop then
         if TrueQ(TerminatingExpressionOf(stmt)) then
           Replace(stmt, MakeCompoundstatement(LabelOf(stmt), StatementsOf(stmt)))

At various points in the paper this style is described as \`fairly
simple and reasonably elegant\'.

The paper illustrates the approach with a number of example
transformations, including [expression
simplification[^?^](http://www.program-transformation.org/edit/Transform/ExpressionSimplification?topicparent=Transform.GrammarBasedDefinitionOfMetaprogrammingSystems)]{.twikiNewLink
style="background : #FFFFCE;"}, [loop
unrolling[^?^](http://www.program-transformation.org/edit/Transform/LoopUnrolling?topicparent=Transform.GrammarBasedDefinitionOfMetaprogrammingSystems)]{.twikiNewLink
style="background : #FFFFCE;"}, and [inaccessible statement
elimination[^?^](http://www.program-transformation.org/edit/Transform/InaccessibleStatementElimination?topicparent=Transform.GrammarBasedDefinitionOfMetaprogrammingSystems)]{.twikiNewLink
style="background : #FFFFCE;"}.

The abstract syntax [API](API){.twikiLink} is based on a grammatical
specification of the object programming language. How the
[API](API){.twikiLink} is derived from the specification seems more a
matter of methodology than generation.

Along the way the paper discusses all kinds of problems that have to be
addressed by a meta-programming system.

The use of [concrete
syntax[^?^](http://www.program-transformation.org/edit/Transform/ConcreteSyntax?topicparent=Transform.GrammarBasedDefinitionOfMetaprogrammingSystems)]{.twikiNewLink
style="background : #FFFFCE;"} in meta-programs is considered, but
deemed too difficult for a first stab at designing a meta-programming
system. Potential problems in this area that are mentioned include: how
to deal with comments and whitespace, how to control the appearance of
the resulting program text, and how tto deal with abstract syntax that
does not directly correspond to the grammatical structure, for example,
as a result of removing parentheses and [de
sugaring[^?^](http://www.program-transformation.org/edit/Transform/DeSugaring?topicparent=Transform.GrammarBasedDefinitionOfMetaprogrammingSystems)]{.twikiNewLink
style="background : #FFFFCE;"}.

The paper dismisses schema or rule-based meta-programming. Rules would
not be capable of dealing with the complex side-conditions involved in
determining whether a transformation applies. Also the implementation of
pattern matching is deemed as innefficient and impractical.

In relation to the problems caused by the dangling-else construct of
Pascal, the authors mention that [ease of
transformation[^?^](http://www.program-transformation.org/edit/Transform/EaseOfTransformation?topicparent=Transform.GrammarBasedDefinitionOfMetaprogrammingSystems)]{.twikiNewLink
style="background : #FFFFCE;"} should be a criterion in language design.

The paper does not mention [tree
traversals[^?^](http://www.program-transformation.org/edit/Transform/TreeTraversals?topicparent=Transform.GrammarBasedDefinitionOfMetaprogrammingSystems)]{.twikiNewLink
style="background : #FFFFCE;"} as a source of overhead in [meta
programs[^?^](http://www.program-transformation.org/edit/Transform/MetaPrograms?topicparent=Transform.GrammarBasedDefinitionOfMetaprogrammingSystems)]{.twikiNewLink
style="background : #FFFFCE;"}, let alone introduce [generic
traversals[^?^](http://www.program-transformation.org/edit/Transform/GenericTraversals?topicparent=Transform.GrammarBasedDefinitionOfMetaprogrammingSystems)]{.twikiNewLink
style="background : #FFFFCE;"}, as introduced for example in [strategic
programming](StrategicProgramming){.twikiLink}.

In conclusion: This paper is an early attempt at getting to grips with
the construction of meta-programming systems. The paper touches upon
many of the issues that one encounters building such systems,

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 20 Jun 2002\

------------------------------------------------------------------------

[CategoryPaper](CategoryPaper){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
