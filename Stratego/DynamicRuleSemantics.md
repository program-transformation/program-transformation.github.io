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
    Page](http://www.program-transformation.org/edit/Stratego/DynamicRuleSemantics?t=1536825555)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/DynamicRuleSemantics)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/DynamicRuleSemantics)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/DynamicRuleSemantics?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/DynamicRuleSemantics?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/Stratego/DynamicRuleSemantics?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/DynamicRuleSemantics?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Stratego/DynamicRuleSemantics?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/DynamicRuleSemantics?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Stratego/DynamicRuleSemantics?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/DynamicRuleSemantics?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/DynamicRuleSemantics)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/DynamicRuleSemantics?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/Stratego/DynamicRuleSemantics?template=oopsmore&param1=1.8&param2=1.8)
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
Dynamic Rule Semantics {#dynamic-rule-semantics .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[Dynamic rules](DynamicRule){.twikiLink} allow the run-time addition of
rewrite rules. This can be used to model context-sensitive rewriting and
has a host of applications in program transformation.

This page discusses issues in the semantics of [dynamic
rules](DynamicRule){.twikiLink}

------------------------------------------------------------------------

::: {.twikiToc}
-   [Bug: Overlapping left-hand
    sides](DynamicRuleSemantics#Bug_Overlapping_left_hand_sides)
-   [Implementing User-Defined Rules with Dynamic
    Rules?](DynamicRuleSemantics#Implementing_User_Defined_Rules)
-   [Fix: Taking entire left-hand side into
    account](DynamicRuleSemantics#Fix_Taking_entire_left_hand_side)
-   [Bug: Rewriting terms with
    annotations](DynamicRuleSemantics#Bug_Rewriting_terms_with_annotat)
:::

------------------------------------------------------------------------

### []{#Bug_Overlapping_left_hand_sides} Bug: Overlapping left-hand sides

Dynamic rules with the same label share the same mapping from
context-variables in the left-hand side to context-variables in the
right-hand side. That is, the dynamic data in a dynamic rule is
determined by the context-variables in the rule.

For example, consider the following generation of a dynamic rule

      generate =
        ?Context(x,y,z);
        rules( Lab : Pat1(x, es) -> Pat2(y, <op>(z, es)) )

When applying `generate` a mapping from `Keys(x)` to `Defined(y, z)` is
generated. When applying `generate` twice in a context with the same
value for `x`, the second rule overrides the first, i.e., the first will
be invisible.

Two dynamic rules with the same label share the same mapping from values
to keys. If the number of context-variables in the left-hand side of the
rule is the same, subsequent rule generations will shadow earlier ones,
*even when the static part of the dynamic rule is different*.

[MarkusLauer[^?^](http://www.program-transformation.org/edit/Main/MarkusLauer?topicparent=Stratego.DynamicRuleSemantics)]{.twikiNewLink
style="background : #FFFFCE;"} reports an example where this causes
different behaviour than expected. The strategy `gendyn` generates two
rules with label `Dyn`. The idea of the rules is that each time a
section is encountered the section counter is incremented, and that
titles are transformed using the current section counter:

     gendyn = ?n; 
       where( <add>(n,1) => n1 );
       where( 
         rules(
           Dyn : tag("section", _, l) -> l where<gendyn> n1
           Dyn : tag("title", _, l)   -> para(sect(n),l)
         ))

These rules are then used in the following strategy to number titles:

     transform = 
       {| Dyn : 
          where(<gendyn>0);
          rec x({| Dyn : try(Dyn <+ A); all(try(x)) |})
       |}

However, this approach does not work because the mappings of the two
`Dyn` rules overlap; since the rules do not use *any* context variables
in the left-hand side, the mapping generated for the rules is `Keys()`
to `Defined(n1)` (first rule) or `Defined(n)` (second rule). The last
rule to be generated will thus determine the values that both rules get.

A **workaround** in these situations is to use *two* different rule
labels. In the example above the problem is solved by naming the rules
`Dyn1` and `Dyn2`.

     gendyn = ?n; 
       where( <add>(n,1) => n1 );
       where( 
         rules(
           Dyn1 : tag("section", _, l) -> l where <gendyn> n1
           Dyn2 : tag("title", _, l)   -> para(sect(n),l)
         ))

     transform = 
       {| Dyn1, Dyn2 : 
          where(<gendyn>0);
          rec x({| Dyn1, Dyn2 : try(Dyn1 + Dyn2 <+ A); all(try(x)) |})
       |}

Now the question is whether this is **a bug or a feature**. A solution
would be to use the entire static part of the left-hand side to
determine which dynamic rule should be applied. However, that would also
make it more difficult to *use* the shadowing effect of overlapping
context variables. Any opinions on the matter?

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 22 Nov 2001\

I believe this is a bug and not a feature. I would intuitively expect
several dynamic rules with the same name to behave just like normal
rules with the same name. If anyone needs special shadowing effects,
couldn\'t the syntax be extended so that the programmer can specify
that?

Another thing; why do we only have dynamic rules, and not dynamic
strategies?

\-- [OttoSkroveBagge](../Main/OttoSkroveBagge){.twikiLink} - 18 Jan
2002\

### []{#Implementing_User_Defined_Rules}[]{#Implementing_User_Defined_Rules_} Implementing User-Defined Rules with Dynamic Rules?

I\'ve made an implementation of user-defined rules for
[CodeBoost](CodeBoost){.twikiLink}, e.g. the programmer can say,

    void rules()
    {
       X<int> x;

      simplify: f(g(x)) = fg(x);
    }

    int main(int argc, char**argv)
    {
       X<int> x;

       x = f(g(x));
    }

and this is transformed into

    int main(int argc, char**argv)
    {
       X<int> x;

       x = fg(x);
    }

(More or less similar to the \"[Transform.Playing by the
rules](../Transform/PlayingByTheRules){.twikiLink}\...\" paper where
this is done for Haskell)

This was surprisingly easy to do, but I\'ve run into the \"Overlapping
Left-Hand Sides\"-bug in dynamic rules. I\'m still using Stratego 0.6.2
\-- is this fixed in newer versions? If not, is there a smart way of
avoiding the problem?

Basically, what I\'m doing is: 1. extract the user-defined rule
specifications and store them as a list in the AST; 2. when the time
comes to use the user-defined rules for something, the list is
traversed, and dynamic rules are created:

      make-rule' =
       ?Rule("simplify", lhs, rhs, whr);
       rules(simplify: x -> y where <apply-user-rule> (lhs, x, rhs) => y)

Of course, this only works for a predefined set of rule names (and, with
the dynamic rule bug, only for the last rule), and I haven\'t come up
with a meaningful way of specifying \"where\"-clauses yet.
apply-user-rule uses

special match/build strategies with support for user-defined variables
(represented as
[RuleVar[^?^](http://www.program-transformation.org/edit/Stratego/RuleVar?topicparent=Stratego.DynamicRuleSemantics)]{.twikiNewLink
style="background : #FFFFCE;"}(\"name\") in the AST) \-- I\'ll send you
the code when I\'ve tested it more.

\-- [OttoSkroveBagge](../Main/OttoSkroveBagge){.twikiLink} - 18 Jan
2002\

No, this is not an instance of the overlapping left-hand sides problem.

Dynamic rules trigger on the left-hand side. This means that such a rule
is only meaningful if has at least one variable in the left-hand side
that is bound in the context of the rule. This is not the case in your
make-rule\'.

The problem is that you cannot directly employ dynamic rules for this
application. The paper [Scoped Dynamic Rewrite
Rules](ScopedDynamicRewriteRules){.twikiLink} has the following to say
about this issue:

Wadler\'s deforestation algorithm \[18\] can be expressed using rewrite
rules and a simple strategy. Dynamic rules can be used to implement the
folding of recursive occurrences of the function composition being
deforested. However, this requires abstracting over object variables,
which is not supported by the dynamic rules discussed in this papers.
Currently, dynamic rules can only inherit ground terms from their de
nition context. Another application that would need abstraction over
object variables are the rule pragmas of the Glas- gow Haskell Compiler
\[14\] that allow the user to state rewrite rules that should be applied
during compilation in addition to normal optimizations.

What you would like to do is to generate a rule

      rules( simplify : ~lhs -> ~rhs )

where \~t expresses the replacement of object variables with
meta-variables in the term. I don\'t currently know how to do this, but
is on my mind.

Workaround: Store the (lhs, rhs) pairs in a list and trie to match each
in turn.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 18 Jan 2002

### []{#Fix_Taking_entire_left_hand_side} Fix: Taking entire left-hand side into account

The desugaring of dynamic rules has been changed to repair the problems
arising when two dynamic rules with the same name have

different left-hand sides, but the same number of context variables in
the left-hand side (see discussion below). The key that is used for a
dynamic rule is now the entire left-hand side, modulo non-context
variables. The new implementation will also make it easier to define (or
even generate) operations for saving, restoring, and intersecting sets
of dynamic rules, as used in data-flow optimizations.

The bugfix will be available in
[StrategoRelease09](StrategoRelease09){.twikiLink} (beta8).

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 22 Dec 2002

### []{#Bug_Rewriting_terms_with_annotat} Bug: Rewriting terms with annotations

After some hours of debugging my Tiger to C compiler, I\'ve found a
problem in the application of dynamic rules to terms with annotations in
[StrategoXT](StrategoXT){.twikiLink} 0.9.x . A dynamic rule without
annotations in the lhs cannot be applied to a term with annotations.

Of course this is not the behaviour of static rules. This problem breaks
all components that use dynamic rules and annotations extensively (like
my Tiger to C compiler). In the 0.8 releases of Stratego the behaviour
was correct (like static rules).

This works:

    -------------------
    module dyn-test
    imports option dynamic-rules

    strategies

       main =
         rules(DynRule : None() -> Some("Blaat"))
         ; <DynRule> None()
    -------------------

But this results in a rewriting failed:

    -------------------
    module dyn-test
    imports option dynamic-rules

    strategies

       main =
         rules(DynRule : None() -> Some("Blaat"))
         ; <DynRule> None(){"whatever"}
    -------------------

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 29 Jul
2003

The change in behaviour from 0.8 to 0.9.x is due to the change in the
semantics of dynamic rules. (See above) According to this semantics the
**entire** term is relevant for the mapping from left-hand side to
right-hand side. Repairing this requires stripping off the annotations
from a term before doing the lookup in the rule table. (Unless the lhs
contains annotations,of course.) Repair is in the [release
plan](ReleasePlan){.twikiLink} for
[StrategoRelease093](StrategoRelease093){.twikiLink}.

Workaround: explicitly match on the list of annotations:

    -------------------
       test2 =
         rules(DynRule2 : None(){t*} -> Some("Blaat"))
         ; <DynRule2> None(){"whatever"}
         ; <DynRule2> None()
    -------------------

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 29 Jul 2003

------------------------------------------------------------------------

[CategoryBugs[^?^](http://www.program-transformation.org/edit/Stratego/CategoryBugs?topicparent=Stratego.DynamicRuleSemantics)]{.twikiNewLink
style="background : #FFFFCE;"} \|
[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.DynamicRuleSemantics)]{.twikiNewLink
style="background : #FFFFCE;"}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.DynamicRuleSemantics moved from Stratego.DynamicRuleBugs on 03
Feb 2002 - 00:10 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}* -
[put it
back](http://www.program-transformation.org/rename/Stratego/DynamicRuleSemantics?newweb=Stratego&newtopic=DynamicRuleBugs&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
