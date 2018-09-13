::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
[Home](WebHome){.twikiLink}

**XT Tools**

-   [Reference Docs](ToolReference){.twikiLink}
-   [GPP](GenericPrettyPrinter){.twikiLink}
-   [ATerm](ATermTools){.twikiLink}
-   [SDF](SdfTools){.twikiLink}
-   [AsFix](AsFixTools){.twikiLink}

**Languages**

-   [Stratego](../Stratego/WebHome){.twikiLink}
-   [SDF](../Sdf/WebHome){.twikiLink}
-   [ATerm](ATermFormat){.twikiLink}

**Software**

-   [Stratego/XT](../Stratego/StrategoDownload){.twikiLink}
-   [SDF2 Bundle](../Sdf/SdfBundle){.twikiLink}
-   [KoalaCompiler](KoalaCompiler){.twikiLink}
-   [AutoBundle](AutoBundle){.twikiLink}
-   [AutoBuild](AutoBuild){.twikiLink}
-   [DailyBuildSystem](DailyBuildSystem){.twikiLink}

[![](http://www.program-transformation.org/twiki/pub/rss.gif "RSS 1.0 feed")](http://www.program-transformation.org/twiki/bin/view/Tools/WebRss?skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Tools/SdfToAstConflicts?t=1536825776)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/SdfToAstConflicts)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/SdfToAstConflicts)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/SdfToAstConflicts?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/SdfToAstConflicts?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tools/SdfToAstConflicts?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/SdfToAstConflicts)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/SdfToAstConflicts?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tools/SdfToAstConflicts?template=oopsmore&param1=1.1&param2=1.1)
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
Sdf To Ast Conflicts {#sdf-to-ast-conflicts .twikiTopicTitle}
====================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[]{#Summary} Summary
--------------------

Calculates conflicting patterns in an AST from an SDF syntax definition.

[]{#Description} Description
----------------------------

sdf2ast-conflicts calculates a list of conflicting patterns in an AST by
analyzing the priority and associativity declarations in an SDF syntax
definition. These conflicting patterns can for example be used to insert
parentheses in order to let a pretty-printed AST have the same meaning
as the originating AST. Such a parentheses inserter can be generated
with the [sdf2parenthesize](SdfToParenthesize){.twikiLink} tool, which
uses this sdf2-ast-conflicts tool.

[]{#Example} Example
--------------------

Consider the following SDF syntax definition for simple arithmetic
expressions:

::: {style="margin-left: 2em"}
    definition
    module Main
    exports
      context-free start-symbols Exp

      sorts Exp Id
      context-free syntax
        Id           -> Exp {cons("Var")}
        "(" Exp ")"  -> Exp {bracket}

        Exp "*"   Exp -> Exp  {left, cons("Mul")}
        Exp "/"   Exp -> Exp  {left, cons("Div")}
        Exp "+"   Exp -> Exp  {left, cons("Plus")}
        Exp "-"   Exp -> Exp  {non-assoc, cons("Minus")}

      context-free priorities
        {left:
          Exp "*" Exp -> Exp
          Exp "/" Exp -> Exp
        } 
      > {left:
          Exp "+" Exp -> Exp
          Exp "-" Exp -> Exp
        }

      lexical syntax
        [a-zA-Z\_] [a-zA-Z0-9\_]* -> Id
        [\ \t\n] -> LAYOUT
      
      lexical restrictions
        Id -/- [a-zA-Z0-9\_]

      context-free restrictions
        LAYOUT? -/- [\ \t\n]
:::

Applying the sdf2ast-conflicts tool:

::: {style="margin-left: 2em"}
    $ sdf2ast-conflicts -i Exp.def | pp-aterm
:::

Results in:

::: {style="margin-left: 2em"}
    [ SubtermConflict(Symbol("Mul", 2), 0, Symbol("Plus", 2))
    , SubtermConflict(Symbol("Mul", 2), 1, Symbol("Plus", 2))
    , SubtermConflict(Symbol("Mul", 2), 0, Symbol("Minus", 2))
    , SubtermConflict(Symbol("Mul", 2), 1, Symbol("Minus", 2))
    , SubtermConflict(Symbol("Div", 2), 0, Symbol("Plus", 2))
    , SubtermConflict(Symbol("Div", 2), 1, Symbol("Plus", 2))
    , SubtermConflict(Symbol("Div", 2), 0, Symbol("Minus", 2))
    , SubtermConflict(Symbol("Div", 2), 1, Symbol("Minus", 2))
    , SubtermConflict(Symbol("Div", 2), 1, Symbol("Mul", 2))
    , SubtermConflict(Symbol("Mul", 2), 1, Symbol("Div", 2))
    , SubtermConflict(Symbol("Minus", 2), 1, Symbol("Plus", 2))
    , SubtermConflict(Symbol("Plus", 2), 1, Symbol("Minus", 2))
    , SubtermConflict(Symbol("Mul", 2), 1, Symbol("Mul", 2))
    , SubtermConflict(Symbol("Div", 2), 1, Symbol("Div", 2))
    , SubtermConflict(Symbol("Plus", 2), 1, Symbol("Plus", 2))
    , SubtermConflict(Symbol("Minus", 2), 0, Symbol("Minus", 2))
    , SubtermConflict(Symbol("Minus", 2), 1, Symbol("Minus", 2))
    ]
:::

The `SubtermConflict` indicates that a certain symbol is not allowed as
the direct subterm of another symbol. Currently, the `SubtermConflict`
is the only conflict pattern that is supported by sdf2ast-conflicts.

To explain its meaning, let\'s have a look at the first conflict:

::: {style="margin-left: 2em"}
    SubtermConflict(Symbol("Mul", 2), 0, Symbol("Plus", 2))
:::

The `SubtermConflict` has three children: a `Symbol` (*A*), an integer
(*x*), and another `Symbol` (*B*). A `Symbol` describes a constructor.
The first subterm of a Symbol is the name of the constructor, in this
case `Mul` and `Plus`. This constructor name corresponds to the `cons`
attribute of the corresponding SDF production rule. The second argument
of a `Symbol` is the arity of the symbol, which is 2 for both symbols.
The meaning of a `SubtermConflict` is that the symbol `B` is not allowed
as a subterm at position *x* of the an aterm with symbol `A`. Thus, the
example conflict defines that the term `Mul(Plus(e1, e2), e3)` has a
conflict. Indeed, this expression is a problem. For instance,
`6 + 5 * 3` will parse as `Plus(e1, Mul(e2, e3))`, not as
`Mul(Plus(e1, e2), e3)`. Therefore, parentheses need to be inserted in
this term.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
