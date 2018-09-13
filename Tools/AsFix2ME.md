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
    Page](http://www.program-transformation.org/edit/Tools/AsFix2ME?t=1536826785)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/AsFix2ME)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/AsFix2ME)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/AsFix2ME?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/AsFix2ME?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tools/AsFix2ME?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/AsFix2ME?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/AsFix2ME?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/AsFix2ME)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/AsFix2ME?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tools/AsFix2ME?template=oopsmore&param1=1.2&param2=1.2)
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
As Fix 2 ME {#as-fix-2-me .twikiTopicTitle}
===========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

AsFix2ME is a more compact variant of
[AsFix2[^?^](http://www.program-transformation.org/edit/Tools/AsFix2?topicparent=Tools.AsFix2ME)]{.twikiNewLink
style="background : #FFFFCE;"}. See the [AsFix](AsFix){.twikiLink} topic
for a general overview of [AsFix](AsFix){.twikiLink}. This topic
describes the difference between AsFix2 and AsFix2ME in more detail.

[]{#Literals_in_AsFix2ME} Literals in AsFix2ME
----------------------------------------------

Consider the syntax definition

------------------------------------------------------------------------

      definition
      module Exp
      exports
        sorts Exp
        context-free syntax
          "nil" -> Exp

        lexical syntax
          [\t\n\r\ ] -> LAYOUT

------------------------------------------------------------------------

Representation in AsFix2ME:

------------------------------------------------------------------------

      appl(
        prod([lit("nil")], cf(sort("Exp")), no-attrs)
      , [lit("nil")]
      )

------------------------------------------------------------------------

Representation in AsFix2:

------------------------------------------------------------------------

      appl(
        prod([lit("nil")], cf(sort("Exp")), no-attrs)
      , [ appl(
            prod(
              [char-class([110]), char-class([105]), char-class([108])]
            , lit("nil")
            , no-attrs
            )
          , [110, 105, 108]
          )
        ]
      )

------------------------------------------------------------------------

[]{#Layout_in_AsFix2ME} Layout in AsFix2ME
------------------------------------------

[]{#Lexical_syntax_in_AsFix2ME} Lexical syntax in AsFix2ME
----------------------------------------------------------

Consider the syntax definition

------------------------------------------------------------------------

      definition
      module Exp
      hiddens
        sorts IntConst

      exports
        sorts Exp
      
        lexical syntax
          [\ \t\n]  -> LAYOUT
          [0-9]+    -> IntConst
      
        context-free syntax
          IntConst  -> Exp {cons("Int")}

------------------------------------------------------------------------

Producing a parse table:

      sdf2table -i Exp-tiny.def.def -o Exp-tiny.tbl -m Exp

Stratego Script to extract the tree related to the context-free symbol
IntConst:

      import simple-traversal ;;
      oncetd(?appl(prod(_, cf(sort("IntConst")), _), _); ?x) ;;
      !x ;;

Parse the expression \"12\" to
[AsFix2[^?^](http://www.program-transformation.org/edit/Tools/AsFix2?topicparent=Tools.AsFix2ME)]{.twikiNewLink
style="background : #FFFFCE;"}

    echo "1" | sglr -2 -p Exp-tiny.tbl | stratego-shell --script extract-lex.srts | pp-aterm

------------------------------------------------------------------------

    appl(
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
                [ lex(iter(char-class([range(48, 57)])))
                , lex(iter(char-class([range(48, 57)])))
                ]
              , lex(iter(char-class([range(48, 57)])))
              , attrs([assoc(left)])
              )
            , [ appl(
                  prod(
                    [char-class([range(48, 57)])]
                  , lex(iter(char-class([range(48, 57)])))
                  , no-attrs
                  )
                , [49]
                )
              , appl(
                  prod(
                    [char-class([range(48, 57)])]
                  , lex(iter(char-class([range(48, 57)])))
                  , no-attrs
                  )
                , [50]
                )
              ]
            )
          ]
        )
      ]
    )

------------------------------------------------------------------------

Parsing the same expression to [AsFix2ME](AsFix2ME){.twikiLink}:

      echo "12" | sglr -m -p Exp-tiny.tbl | stratego-shell --script extract-cf.strs | pp-aterm

------------------------------------------------------------------------

    appl(
      prod(
        [lex(sort("IntConst"))]
      , cf(sort("IntConst"))
      , no-attrs
      )
    , [ appl(
          list(iter-star(char-class([range(0, 255)])))
        , [49, 50]
        )
      ]
    )

------------------------------------------------------------------------

-   **Note**: If we add a constructor to the IntConst production the
    constructor name will be lost.

Now consider the syntax definition:

------------------------------------------------------------------------

      definition
      module Exp
      hiddens
        sorts DecConst

      exports
        sorts Exp
      
        lexical syntax
          [\ \t\n]  -> LAYOUT
          [0-9]+ "." [0-9]+ -> DecConst {cons("DecConst")}
      
        context-free syntax
          DecConst  -> Exp

------------------------------------------------------------------------

Parsing to AsFix2ME:

      echo "13.25" | sglr -m -p Exp-tiny.tbl | stratego-shell --script extract-cf.strs | pp-aterm

------------------------------------------------------------------------

    appl(
      prod(
        [lex(sort("DecConst"))]
      , cf(sort("DecConst"))
      , no-attrs
      )
    , [ appl(
          list(iter-star(char-class([range(0, 255)])))
        , [49, 51, 46, 50, 53]
        )
      ]
    )

------------------------------------------------------------------------

[]{#Syntax_in_AsFix2ME} Syntax in AsFix2ME
------------------------------------------

Consider the syntax definition

------------------------------------------------------------------------

      definition
      module Exp
      hiddens
        sorts DecConst

      exports
        sorts Exp
        context-free syntax
          DecConst  -> Exp

        syntax
          [0-9]+ "." [0-9]+ -> DecConst {cons("DecConst")}
          DecConst -> <DecConst-CF>

        lexical syntax
          [\t\n\r\ ] -> LAYOUT

------------------------------------------------------------------------

In this case the DecConst application is represented as a tree in
AsFix2ME, just like in AsFix2.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
