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
    Page](http://www.program-transformation.org/edit/Stratego/RulesVersusStrategies?t=1536825665)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/RulesVersusStrategies)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/RulesVersusStrategies)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/RulesVersusStrategies?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/RulesVersusStrategies?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/RulesVersusStrategies?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/RulesVersusStrategies)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/RulesVersusStrategies?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/RulesVersusStrategies?template=oopsmore&param1=1.1&param2=1.1)
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
Rules Versus Strategies {#rules-versus-strategies .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

In stratego all information is represented as a ATerm. An ATerm can be
thought of as a structured tree-like representation of the information
that needs to be transformed. ATerms can be used to represent anything.
More specifically also hierarchical formats like parse trees or XML
files lend themselves very well to be represented in ATerms (also called
terms; ATerm refers to the name of a library to work with terms).

\"Strategies\" are operations that operate on terms. In general they
take a term, and return a transformed term. Imperative programmers can
think of a strategy as a function, taking a term as input, and returning
a term as output. (Special build and match strategies exist, however, to
generate new terms without the need for an input term, or to match terms
to patterns, without returning a new term.)

Something that requires some getting used to is the fact that the term
that serves as input to a strategy is not mentioned explicitely as a
parameter to the strategy. Instead it is present implicitely.

Strategies can be used e.g. to specify in what order the nodes of a tree
should be traversed and transformed or analysed.

\"Rules\" replace terms with transformed terms. In fact rules are
syntactic sugar for a specific series of strategy operations. That is,
there is a conceptual difference between strategies and rules, but not
necessarily an implementation difference. (Conceptually a strategy
specifies term traversal, or performs an analysis, while a rule performs
a transformation.)

There is always a \"term under consideration\", but it is not mentioned
explicitely. At start-time this is the term that is loaded from a file
(or typed on the keyboard). New (sub)terms can be builded during
execution, or (sub)terms can be replaced with transformed subterms.
Terms usually contain other terms. This way you get a hierarchical tree
of terms. By matching patterns one can identify interesting areas in the
tree of terms on which to perform certain rewritings.

For example:

    strategies
      main = topdown(try(renamevar))

    rules
      renamevar:
        VarDef(vname,vtype) -> VarDef(vname2,vtype)   
        where new => vname2

Here we specify that the term under consideration will be traversed in a
topdown way, and at each node of the term tree we will try to apply
strategy renamevar. renamevar in its turn is specified as a strategy
that compares the current term under consideration with a `VarDef(,)`
node. (The notation \"\_\" means that anything could be standing there.)
If that succeeds, a new name is created, and the variable is renamed to
the new name.

Second example:

Suppose we start on term

    Program(
      ImportFileList(["file.txt","file2.txt"]),
      VarDefList([VarDef("v1","int"),
             VarDef("v2","bool")]),
      StatementList([If(Int("0"),
              StatementList(),
              StatementList()),
           Return(Int("1"))])
    )

First renamevar is tried on `Program(,,_)`. This obviously fails because
`Program(,,_)` is not `VarDef(,)`. Because the renamevar is surrounded
by a try statement, execution can still continue. Next it is tried on
`ImportFileList(_)`. This fails. Next it is tried on the list
`["file1.txt","file2.txt"]`, and later on each of the elements of the
list, which also fails. Next it is tried on `VarDefList(_)`, but this
fails. Next it is tried on `[VarDef(),VarDef()]` but it fails.

It is then tried on `VarDef("v1","int")`. This is the first time the
match rule `?VarDef(vname,vtype)` succeeds. The `vname` parameter in the
`renamevar` rule gets the value `"v1"`, the vtype parameter gets the
value `"int"`. Now the `where(new => v2)` is executed. `where(s)` is a
strategy operator that executes strategy `s`, but returns the original
term, even if `s` changed the term. Any side-effects (assignments to
term variables) are kept, though. So the `where(new => v2)` assigns the
result of executing strategy new to `v2`, but returns the
`VarDef("v1","int")` as result. Next the strategy
`!VarDef(vname2,vtype)` is executed. This takes the term
`VarDef("v1","int")` and returns the term `VarDef("a_0","int")`, where
`a_0` is a new name generated by strategy new. Because the renamevar
strategy succeeded completely (since each substrategy succeeded), the
result is committed, and the original `VarDef("v1","int")` term is
replaced with `VarDef("a_0","int")`.

Applying a strategy to a term either succeeds or fails. It also returns
a transformed term. Depending on success or failure, different other
strategies can be activated (see later). This is how conditional
execution of strategies can be implemented.

The input to a strategy is the current term under consideration, unless
you use the strategy application angles. E.g. if you just execute `s`,
you will apply s to the current term under consideration. If you execute
`< s > t` , you will apply `s` to the term contained in term variable t.

The result of a strategy becomes the current term under consideration,
unless you perform the strategy in a `where()` -clause or a `test()`
clause (see later), or you assign the result of the strategy to a (term)
variable using the `=>` operator (see later). In the latter case `t`
contains the result of the strategy application and the current term
under consideration is unchanged.

Strategies can be parameterized with other strategies, thus forming
strategy operators. E.g. in the strategy `topdown(s)`, there is a
parameter `s`, which is a strategy that specifies the actions that
should be done on the terms encountered during the top-down traversal.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
