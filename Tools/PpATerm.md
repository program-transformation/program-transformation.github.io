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
    Page](http://www.program-transformation.org/edit/Tools/PpATerm?t=1536825774)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/PpATerm)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/PpATerm)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/PpATerm?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/PpATerm?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tools/PpATerm?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/PpATerm)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/PpATerm?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tools/PpATerm?template=oopsmore&param1=1.1&param2=1.1)
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
Pp ATerm {#pp-aterm .twikiTopicTitle}
========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

The pp-aterm tool adds layout to an ATerm to make its structure more
clear.

Example:

The following Tiger program

      let function fact(n : int) : int =
            if n < 1 then 1 else (n * fact(n - 1))
       in printint(fact(10))
      end

is represented in abstract syntax by:

      Let([FunDecs([FunDec("fact",[FArg("n",Tp(Tid("int")))],Tp(Tid("int")),
      If(Lt(Var("n"),Int("1")),Int("1"),Seq([Times(Var("n"),Call(
      Var("fact"),[Minus(Var("n"),Int("1"))]))])))])],[Call(
      Var("printint"),[Call(Var("fact"),[Int("10")])])])

pp-aterm rewrites this ATerm to:

    Let(
      [ FunDecs(
          [ FunDec(
              "fact"
            , [FArg("n", Tp(Tid("int")))]
            , Tp(Tid("int"))
            , If(
                Lt(Var("n"), Int("1"))
              , Int("1")
              , Seq(
                  [ Times(
                      Var("n")
                    , Call(
                        Var("fact")
                      , [Minus(Var("n"), Int("1"))]
                      )
                    )
                  ]
                )
              )
            )
          ]
        )
      ]
    , [ Call(
          Var("printint")
        , [Call(Var("fact"), [Int("10")])]
        )
      ]
    )

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
