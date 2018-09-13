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
    Page](http://www.program-transformation.org/edit/Transform/TreeRewriting?t=1536826584)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/TreeRewriting)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/TreeRewriting)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/TreeRewriting?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/TreeRewriting?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/TreeRewriting?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/TreeRewriting?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/TreeRewriting?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/TreeRewriting?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/TreeRewriting?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/TreeRewriting?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/TreeRewriting)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/TreeRewriting?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/TreeRewriting?template=oopsmore&param1=1.4&param2=1.4)
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
Tree Rewriting {#tree-rewriting .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Tree rewriting is a synonym for [term
rewriting](TermRewriting){.twikiLink}, i.e., the process of transforming
trees ([tree structured
data[^?^](http://www.program-transformation.org/edit/Transform/TreeStructuredData?topicparent=Transform.TreeRewriting)]{.twikiNewLink
style="background : #FFFFCE;"}) into other trees by applying rewriting
rules.

[Bottomup tree
rewriting[^?^](http://www.program-transformation.org/edit/Transform/BottomupTreeRewriting?topicparent=Transform.TreeRewriting)]{.twikiNewLink
style="background : #FFFFCE;"} is a special case of tree rewriting that
is used in [code generation](CodeGeneration){.twikiLink} to select
instructions for subtrees of an expression tree. The paper [Rewriting
Strategies for Instruction
Selection](../Stratego/RewritingStrategiesForInstructionSelection){.twikiLink}
explains the formalization of [instruction
selection](InstructionSelection){.twikiLink} by means of [rewrite
rules](RewriteRule){.twikiLink} and different strategies that might be
employed to apply these rules.

In [graph
rewriting[^?^](http://www.program-transformation.org/edit/Transform/GraphRewriting?topicparent=Transform.TreeRewriting)]{.twikiNewLink
style="background : #FFFFCE;"} possibly cyclic graphs are transformed.
However, tree [rewriting
systems[^?^](http://www.program-transformation.org/edit/Transform/RewritingSystems?topicparent=Transform.TreeRewriting)]{.twikiNewLink
style="background : #FFFFCE;"} are often implemented using a mild form
of graphs, i.e, [directed acyclic
graphs[^?^](http://www.program-transformation.org/edit/Transform/DirectedAcyclicGraphs?topicparent=Transform.TreeRewriting)]{.twikiNewLink
style="background : #FFFFCE;"} (or
[DAG[^?^](http://www.program-transformation.org/edit/Transform/DAG?topicparent=Transform.TreeRewriting)]{.twikiNewLink
style="background : #FFFFCE;"}s) in which it is possible for subtrees to
be shared by several supertrees. This is necessary for implementations
to be efficient; pure tree rewriting requires making a complete copy of
a tree whenever it is bound to a variable which is used more than once
in a right-hand side of rewrite rule.

Tree rewrite rules can be implemented in any language that supports
hierarchical data structures.

Google on [tree
rewriting](http://www.google.nl/search?q=tree+rewriting&hl=en&lr=)

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 08 Jun 2002

------------------------------------------------------------------------

Tree rewriting is [TermRewriting](TermRewriting){.twikiLink} extended to
allow rewriting of arbitrary syntactic forms, typically specified using
a context-free grammar.

The pattern and replacement of a rewriting rule are expressed as
sentential forms of a given nonterminal of the grammar, with pattern
variables bound to deeper nonterminals in a by-example style.

An example ( [TXL](TXL){.twikiLink} ) tree rewriting rule over the Java
grammar appears below. In this notation nonterminal types of the grammar
(in this case the Java grammar) appear in square brackets \[\]. Words
beginning with a capital letter are pattern variable names. A pattern
variable name followed by a nonterminal type denotes a binding
occurrence of the variable; a pattern variable name appearing without a
type denotes the variable\'s previously bound value.

        rule nestedIfToElseIf
            replace [statement]

                    if ( E1 [expression] ) 
                        S1 [statement]
                    else {
                        if ( E2 [expression] )
                            S2 [statement]
                        Else2 [opt else_clause]
                    }

            by
                    if ( E1 ) 
                        S1 
                    else if ( E2 )
                        S2
                    Else2
        end rule 

Tree rewriting rules are applied to parse trees of the grammar (their
*scope*) searching for instances of the nonterminal they rewrite (their
*target*) under control of a
[RewritingStrategy](RewritingStrategy){.twikiLink}, typically attribute
evaluation or functional programming.

\-- [JamesCordy](JamesCordy){.twikiLink}

Tree rewriting and [term rewriting](TermRewriting){.twikiLink} are
usually identified, since terms are isomorphic to trees. The
presentation of rewrite rules using [concrete
syntax[^?^](http://www.program-transformation.org/edit/Transform/ConcreteSyntax?topicparent=Transform.TreeRewriting)]{.twikiNewLink
style="background : #FFFFCE;"} is orthogonal to the definition of rules.
In the paper [Meta Programming with Concrete Object
Syntax](../Stratego/MetaProgrammingWithConcreteObjectSyntax){.twikiLink}
it is shown how a language based on rewriting [abstract syntax
trees[^?^](http://www.program-transformation.org/edit/Transform/AbstractSyntaxTrees?topicparent=Transform.TreeRewriting)]{.twikiNewLink
style="background : #FFFFCE;"} can be extended to use concrete syntax
trees.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 08 Jun 2002

------------------------------------------------------------------------

[CategorySystem](CategorySystem){.twikiLink} \|
[TransformationSystems](TransformationSystems){.twikiLink} \|
Contributions by [JamesCordy](JamesCordy){.twikiLink},
[EelcoVisser](../Main/EelcoVisser){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
