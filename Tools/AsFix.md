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
    Page](http://www.program-transformation.org/edit/Tools/AsFix?t=1536825772)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/AsFix)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/AsFix)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/AsFix?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/AsFix?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Tools/AsFix?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Tools/AsFix?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Tools/AsFix?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Tools/AsFix?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Tools/AsFix?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Tools/AsFix?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/AsFix)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/AsFix?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Tools/AsFix?template=oopsmore&param1=1.7&param2=1.7)
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
As Fix {#as-fix .twikiTopicTitle}
======

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[]{#Description} Description
----------------------------

[AsFix](AsFix){.twikiLink} (ASF+SDF fixed format) is a format for
representing [parse trees](../Transform/ParseTree){.twikiLink} in the
ATerm format.

Currently two versions of [AsFix](AsFix){.twikiLink} are in used:
[AsFix2ME](AsFix2ME){.twikiLink} and AsFix2. AsFix2 is extremely verbose
since layout and literals have a structured representation in AsFix2.
AsFix2ME is a more concise since lists, layout and literals are
flattened. This is the parse tree format that is used in the ASF+SDF
Meta-Environment.

[]{#Application} Application
----------------------------

The SGLR parser outputs the result of parsing an input in the AsFix
format. The most recent versions of SGLR produce AsFix2ME by default.
SGLR produces AsFix2 when the `-2` flag is used.

In [StrategoXT](../Stratego/StrategoXT){.twikiLink} program
transformation systems usually operate on [abstract syntax
trees](../Stratego/AbstractSyntaxTree){.twikiLink}. The AsFix2 output of
[SGLR](../Sdf/SGLR){.twikiLink} is transformed into an abstract syntax
tree by
[implode-asfix](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-implode-asfix.html).

[]{#Format_Internals} Format Internals
--------------------------------------

Usually you don\'t actually want to see an AsFix2 or AsFix2ME parse
tree. AsFix takes the job of representing the result of parsing an input
very serious. It includes all information required to reproduce the
original input. This unparsing is implemented by the
[asfix-yield](AsFixYield){.twikiLink} tool. The AsFix format exactly
describes what kind of productions are applied. An AsFix representation
is self-contained: all grammar information needed to interpret a term is
also included.

[]{#Example} Example
--------------------

Consider the following [SDF](../Sdf/WebHome){.twikiLink} syntax
definition.

      definition
      module Exp
      exports
        sorts Exp

        lexical syntax
          [\ \t\n]  -> LAYOUT
          [a-zA-Z]+ -> Id
          [0-9]+    -> IntConst

        context-free syntax
          Id        -> Exp {cons("Var")}
          IntConst  -> Exp {cons("Int")}

          Exp "*"  Exp -> Exp  {left, cons("Mul")}
          Exp "/"  Exp -> Exp  {left, cons("Div")}
          Exp "%"  Exp -> Exp  {left, cons("Mod")}

          Exp "+"  Exp -> Exp  {left, cons("Plus")}
          Exp "-"  Exp -> Exp  {left, cons("Minus")}

        context-free priorities
          {left:
            Exp "*"  Exp -> Exp
            Exp "/"  Exp -> Exp
            Exp "%"  Exp -> Exp
          }
        > {left:
            Exp "+"  Exp -> Exp
            Exp "-"  Exp -> Exp
          }

PGEN\'s `sdf2table` produces an SGLR parse table from this syntax
definition:

      sdf2table -m Exp -i Exp.def -o Exp.tbl

### []{#Parsing_to_AsFix2ME} Parsing to AsFix2ME

Parsing the expression `1 + a` to the compact [AsFix](AsFix){.twikiLink}
variant AsFix2ME using:

      echo "1 + a" | sglr -m -A -p Exp.tbl | pp-aterm

produces the following parse tree:

    parsetree(
      appl(
        prod(
          [cf(opt(layout)), cf(sort("Exp")), cf(opt(layout))]
        , sort("<START>")
        , no-attrs
        )
      , [ appl(prod([], cf(opt(layout)), no-attrs), [])
        , appl(
            prod(
              [ cf(sort("Exp"))
              , cf(opt(layout))
              , lit("+")
              , cf(opt(layout))
              , cf(sort("Exp"))
              ]
            , cf(sort("Exp"))
            , attrs([assoc(left), term(cons("Plus"))])
            )
          , [ appl(
                prod(
                  [cf(sort("IntConst"))]
                , cf(sort("Exp"))
                , attrs([term(cons("Int"))])
                )
              , [ appl(
                    prod(
                      [lex(sort("IntConst"))]
                    , cf(sort("IntConst"))
                    , no-attrs
                    )
                  , [ appl(
                        list(iter-star(char-class([range(0, 255)])))
                      , [49]
                      )
                    ]
                  )
                ]
              )
            , appl(
                prod([cf(layout)], cf(opt(layout)), no-attrs)
              , [32]
              )
            , lit("+")
            , appl(
                prod([cf(layout)], cf(opt(layout)), no-attrs)
              , [32]
              )
            , appl(
                prod(
                  [cf(sort("Id"))]
                , cf(sort("Exp"))
                , attrs([term(cons("Var"))])
                )
              , [ appl(
                    prod(
                      [lex(sort("Id"))]
                    , cf(sort("Id"))
                    , no-attrs
                    )
                  , [ appl(
                        list(iter-star(char-class([range(0, 255)])))
                      , [97]
                      )
                    ]
                  )
                ]
              )
            ]
          )
        , appl(
            prod([cf(layout)], cf(opt(layout)), no-attrs)
          , [10]
          )
        ]
      )
    , 0
    )

### []{#Parsing_to_AsFix2} Parsing to AsFix2

Parsing the same expression to AsFix2:

      echo "1 + a" | sglr -2 -A -p Exp.tbl | pp-aterm

results in:

    parsetree(
      appl(
        prod(
          [cf(opt(layout)), cf(sort("Exp")), cf(opt(layout))]
        , sort("<START>")
        , no-attrs
        )
      , [ appl(prod([], cf(opt(layout)), no-attrs), [])
        , appl(
            prod(
              [ cf(sort("Exp"))
              , cf(opt(layout))
              , lit("+")
              , cf(opt(layout))
              , cf(sort("Exp"))
              ]
            , cf(sort("Exp"))
            , attrs([assoc(left), term(cons("Plus"))])
            )
          , [ appl(
                prod(
                  [cf(sort("IntConst"))]
                , cf(sort("Exp"))
                , attrs([term(cons("Int"))])
                )
              , [ appl(
                    prod(
                      [lex(sort("IntConst"))]
                    , cf(sort("IntConst"))
                    , no-attrs
                    )
                  , [ appl(
                        prod(
                          [lex(iter(char-class([range(48, 57)])))]
                        , lex(sort("IntConst"))
                        , no-attrs
                        )
                      , [ appl(
                            prod(
                              [char-class([range(48, 57)])]
                            , lex(iter(char-class([range(48, 57)])))
                            , no-attrs
                            )
                          , [49]
                          )
                        ]
                      )
                    ]
                  )
                ]
              )
            , appl(
                prod([cf(layout)], cf(opt(layout)), no-attrs)
              , [ appl(
                    prod([lex(layout)], cf(layout), no-attrs)
                  , [ appl(
                        prod(
                          [char-class([range(9, 10), 32])]
                        , lex(layout)
                        , no-attrs
                        )
                      , [32]
                      )
                    ]
                  )
                ]
              )
            , appl(
                prod([char-class([43])], lit("+"), no-attrs)
              , [43]
              )
            , appl(
                prod([cf(layout)], cf(opt(layout)), no-attrs)
              , [ appl(
                    prod([lex(layout)], cf(layout), no-attrs)
                  , [ appl(
                        prod(
                          [char-class([range(9, 10), 32])]
                        , lex(layout)
                        , no-attrs
                        )
                      , [32]
                      )
                    ]
                  )
                ]
              )
            , appl(
                prod(
                  [cf(sort("Id"))]
                , cf(sort("Exp"))
                , attrs([term(cons("Var"))])
                )
              , [ appl(
                    prod(
                      [lex(sort("Id"))]
                    , cf(sort("Id"))
                    , no-attrs
                    )
                  , [ appl(
                        prod(
                          [ lex(
                              iter(
                                char-class([range(65, 90), range(97, 122)])
                              )
                            )
                          ]
                        , lex(sort("Id"))
                        , no-attrs
                        )
                      , [ appl(
                            prod(
                              [char-class([range(65, 90), range(97, 122)])]
                            , lex(
                                iter(
                                  char-class([range(65, 90), range(97, 122)])
                                )
                              )
                            , no-attrs
                            )
                          , [97]
                          )
                        ]
                      )
                    ]
                  )
                ]
              )
            ]
          )
        , appl(
            prod([cf(layout)], cf(opt(layout)), no-attrs)
          , [ appl(
                prod([lex(layout)], cf(layout), no-attrs)
              , [ appl(
                    prod(
                      [char-class([range(9, 10), 32])]
                    , lex(layout)
                    , no-attrs
                    )
                  , [10]
                  )
                ]
              )
            ]
          )
        ]
      )
    , 0
    )

### []{#Producing_an_Abstract_Syntax_Tre} Producing an Abstract Syntax Tree

Applying
[implode-asfix](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-implode-asfix.html)
to reduce this to an abstract syntax tree:

      echo "1 + a" | sglr -2A -p Exp.tbl | implode-asfix | pp-aterm

results in:

      Plus(Int("1"), Var("a"))

[implode-asfix](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-implode-asfix.html)
only accepts AsFix2. The [implodePT](ImplodeParseTree){.twikiLink} (part
of the pt-support package, which is in the
[sdf2-bundle](../Stratego/Sdf2Bundle){.twikiLink}) implements the same
implosion for AsFix2ME.

      echo "1 + a" | sglr -mA -p Exp.tbl | implodePT | pp-aterm

produces

      Plus(Int("1"), Var("a"))

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.AsFix moved from Stratego.AsFix on 17 Feb 2004 - 09:35 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tools/AsFix?newweb=Stratego&newtopic=AsFix&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
