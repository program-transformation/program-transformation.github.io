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
    Page](http://www.program-transformation.org/edit/Stratego/PatternMatching?t=1536825605)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/PatternMatching)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/PatternMatching)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/PatternMatching?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/PatternMatching?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/PatternMatching?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/PatternMatching?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/PatternMatching?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/PatternMatching?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/PatternMatching?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/PatternMatching?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/PatternMatching)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/PatternMatching?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/PatternMatching?template=oopsmore&param1=1.4&param2=1.4)
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
Pattern Matching {#pattern-matching .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#Patterns} Patterns
----------------------

The match strategy (`?`) Compares the current term to a pattern. A
pattern is a term that might contain variables. If a variable in a term
pattern is already bound to a term , then the variable in the pattern
will be replaced with this value. If variables in term are not yet
bound, then these variables will be bound to the actual values in the
current term to which the pattern is applied.

For example, `?FunDef(Id(fn),fb)`

-   succeeds when applied to `FunDef(Id("decode"),Return(Int(0)))`
    -   `fn` will have the value `"decode"`
    -   `fb` will have the value `Return(Int(0))`

<!-- -->

-   fails when applied to e.g. term `VarDef(Id("i"),TypeDecl(Int))`

[]{#Matching_on_lists} Matching on lists
----------------------------------------

Explained using some examples:

      0: ?[x | xs] applied to [] will fail
      1: ?[x | xs] applied to [1] will yield x = 1, xs = []
      2: ?[x | xs] applied to [1,2] will yield x = 1, xs = [2]
      3: ?[x | xs] applied to [1,2,3,4] will yield x = 1, xs = [2,3,4]

      4: ?[x , xs] applied to [] will fail
      5: ?[x , xs] applied to [1] will fail 
      6: ?[x , xs] applied to [1,2] will yield x = 1, xs = 2
      7: ?[x , xs] applied to [1,2,3,4] will fail

      ?[] will only succeed on an empty list []

[]{#Special_Patterns} Special Patterns
--------------------------------------

Pattern matching is not restricted to terms containing variables. Some
special matching operators exist. The generic term (de)construction
pattern `#` is explained in [Generic Term
Deconstruction](GenericTermDeconstruction){.twikiLink}.

The pattern `@` allows takes a variable (`v`) at its left-hand side and
a pattern `p` at the right-hand side. The current term will be matched
against the pattern `p` and in addition the current will be bound to
`v`. Thus, `?x@p` is equal to `?p; ?x` and `?x; ?p`.

[]{#See_also} See also
----------------------

-   [Term projection](TermProject){.twikiLink}
-   [Contextual pattern
    matching[^?^](http://www.program-transformation.org/edit/Stratego/ContextualPatternMatching?topicparent=Stratego.PatternMatching)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [Generic Term Deconstruction](GenericTermDeconstruction){.twikiLink}
-   [Variable
    Scope[^?^](http://www.program-transformation.org/edit/Stratego/VariableScope?topicparent=Stratego.PatternMatching)]{.twikiNewLink
    style="background : #FFFFCE;"}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
