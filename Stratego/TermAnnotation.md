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
    Page](http://www.program-transformation.org/edit/Stratego/TermAnnotation?t=1536825713)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/TermAnnotation)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/TermAnnotation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/TermAnnotation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/TermAnnotation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Stratego/TermAnnotation?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/TermAnnotation?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Stratego/TermAnnotation?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/TermAnnotation?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/TermAnnotation?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/TermAnnotation?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/TermAnnotation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/TermAnnotation?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Stratego/TermAnnotation?template=oopsmore&param1=1.7&param2=1.7)
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
Term Annotation {#term-annotation .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#Introduction} Introduction
------------------------------

Stratego uses terms to represent the abstract syntax of programs or
documents. A term consists of a constructor and a list of argument
terms. Sometimes it is useful to record additional information about a
term without adapting its structure, i.e., creating a constructor with
additional arguments. For this purpose terms can be annotated. Support
for [TermAnnotations](TermAnnotation){.twikiLink} has been available
from [StrategoRelease07](StrategoRelease07){.twikiLink}.

In Stratego a term always has a list of annotations. This is the empty
list if a term doesn\'t have any annotations. term annotation uses the
syntax

      t1 { a1 }

where term a1 is an annotation of term t1. If you want to add more
annotations to a term you can use the same syntax you would use for the
content of a list:

      t1 { a1, a2, a3 }

[]{#Annotations_in_match_and_build} Annotations in match and build
------------------------------------------------------------------

The annotations of a term can be retrieved in a pattern match and set in
a build. For example the following build will create a term `Plus(1, 2)`
with the term `Int` as the only annotation.

      !Plus(1, 2){Int}

Naturally the annotation syntax can also be used in a match:

      ?Plus(1, 2){Int}

Note however that this match only accepts `Plus(1, 2)` terms with just
one annotation, which should be the empty contstructor application
`Int`. This match will thus not allow other annotations.

[]{#Annotations_in_RewriteRules} Annotations in [RewriteRules](RewriteRule){.twikiLink}
---------------------------------------------------------------------------------------

Because a [RewriteRule](RewriteRule){.twikiLink} is just sugar for a
[StrategyDefinition](StrategyDefinition){.twikiLink}, the usage of
annotations in rules is just as you would expect. The following rule
checks that the two subterms of the Plus have annotation Int and then
attaches the annotation Int to the whole term:

      TypeCheck :
        Plus(e1{Int}, e2{Int}) -> Plus(e1, e2){Int}

[]{#Annotations_in_CongruenceOperato} Annotations in [CongruenceOperators](CongruenceOperator){.twikiLink}
----------------------------------------------------------------------------------------------------------

Also congruences over annotations are supported. Thus, if `s1` and `s2`
are strategies, then `s1{s2}` is also a strategy, which applies s1 to
the term and s2 to its annotations. Notice that s2 is applied to the
`annotations`. Therefor you have to use a list congruence `[s3]` if you
want to apply s3 to the only annotation of s3. If you want to apply a
strategy to all annotations, you can use a map.

Some examples:

       <id{[inc]}>      Plus(1, 2){3}       => Plus(1, 2){4}
       <id{[inc, inc]}> Plus(1, 2){3, 4}    => Plus(1, 2){4, 5}
       <id{map(inc)}>   Plus(1, 2){3, 4, 5} => Plus(1, 2){4, 5, 6}

[]{#Frequent_problems} Frequent problems
----------------------------------------

### []{#Annotation_is_list} Annotation is list

Remember that if you apply a `!Plus(1, 2){x}`, the term x will be the
only annotation. This is also the case if x is a list. Example:

       SomeRule: xs -> Plus(5, 6){xs}

       <SomeRule> ["a", "b", "c"] => Plus(5, 6){["a", "b", "c"]}

Notice that in this example the result is not
`Plus(5, 6){"a", "b", "c"}`. The Plus term will have just one
annotation, which is the list `["a", "b", "c"]`. You can use
[ListMatching](ListMatching){.twikiLink} to solve this problem:

       SomeRule: [xs*] -> Plus(5, 6){xs*}

       <SomeRule> ["a", "b", "c"] => Plus(5, 6){"a", "b", "c"}

You can also use [ListMatching](ListMatching){.twikiLink} inside the
annotation part of a match:

       Incr: Int(x){as*} -> Int(<inc> x){as*}

       <Incr> Int(5){Int} => Int(6){Int}

### []{#Preserving_annotations} Preserving annotations

Because annotations are not part of the structure there is a huge risk
of losing them. For example the following
[RewriteRule](RewriteRule){.twikiLink} will already drop the annotations
of the Int term.

       Incr: Int(x) -> Int(<inc> x)

You can create a strategy into an annotation preserving strategy with
`preserve-annos` in the annotations module of the
[StrategoStandardLibrary[^?^](http://www.program-transformation.org/edit/Stratego/StrategoStandardLibrary?topicparent=Stratego.TermAnnotation)]{.twikiNewLink
style="background : #FFFFCE;"}.

The [GenericTermTraversal](GenericTermTraversal){.twikiLink} operators
`all`, `some` and `one` and
[CongruenceOperators](CongruenceOperator){.twikiLink} preserve
annotations. If the `Incr` rule is implemented as congruence, the
annotations will be preserved:

       Incr = Int(inc)

       <Incr> Int(5){Int} => Int(6){Int}

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 25 Jan
2003

------------------------------------------------------------------------

[CategoryGlossary](CategoryGlossary){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.TermAnnotation moved from Stratego.TermAnnotations on 06 Jan
2002 - 16:34 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}* - [put
it
back](http://www.program-transformation.org/rename/Stratego/TermAnnotation?newweb=Stratego&newtopic=TermAnnotations&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
