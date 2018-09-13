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
    Page](http://www.program-transformation.org/edit/Tools/AddPosInfo?t=1536826214)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/AddPosInfo)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/AddPosInfo)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/AddPosInfo?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/AddPosInfo?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tools/AddPosInfo?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/AddPosInfo)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/AddPosInfo?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tools/AddPosInfo?template=oopsmore&param1=1.1&param2=1.1)
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
Add Pos Info {#add-pos-info .twikiTopicTitle}
============

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[]{#Summary} Summary
--------------------

addPosInfo adds position information to an
[AsFix2ME](AsFix2ME){.twikiLink} parse tree.

[]{#Example} Example
--------------------

The following syntax definition defines a tiny language of assignments
and expressions.

      definition
      module Main
      exports
        context-free start-symbols Stm*

        sorts Id IntConst
        lexical syntax
          [\ \t\n]  -> LAYOUT
          [a-zA-Z]+ -> Id
          [0-9]+    -> IntConst

        sorts Stm
        context-free syntax
          Id ":=" Exp -> Stm {cons("Assign")}

        sorts Exp
        context-free syntax
          Id        -> Exp {cons("Var")}
          IntConst  -> Exp {cons("Int")}

          Exp "+"  Exp -> Exp  {left, cons("Plus")}

Generate a parse table:

      > sdf2table -i Foo.def -o Foo.tbl

Input file:

      x := 5
      y := x + 4
      z := x + y

Parse the input and have a look at the result in abstract syntax:

      > sglr -i foo.txt -p Foo.tbl | addPosInfo -p ./foo.txt -m | implodePT | pp-aterm

Notes:

-   you must specify the path (`-p`) of the input file.
-   sglr must produce Asfix2ME. This happens if you pass no `-2`
    argument.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
