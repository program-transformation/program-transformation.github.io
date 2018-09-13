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
    Page](http://www.program-transformation.org/edit/Tools/RtgToSig?t=1536826225)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/RtgToSig)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/RtgToSig)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/RtgToSig?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/RtgToSig?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tools/RtgToSig?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/RtgToSig?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/RtgToSig?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/RtgToSig)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/RtgToSig?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tools/RtgToSig?template=oopsmore&param1=1.2&param2=1.2)
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
[]{#rtg2sig} rtg2sig
====================

[]{#Summary} Summary
--------------------

Generates a [Stratego
Signature](../Stratego/StrategoSignature){.twikiLink} from an
[RTG](../Stratego/RegularTreeGrammar){.twikiLink}.

[]{#Options} Options
--------------------

       --module n       Generated module has name n
       -i f|--input f   Read input from f
       -o f|--output f  Write output to f

[]{#Example} Example
--------------------

Consider the RTG that is produced by the example in
[sdf2rtg](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-sdf2rtg.html).

      regular tree grammar
        start Exp
        productions
          Exp      -> Minus(Exp,Exp)
          Exp      -> Plus(Exp,Exp)
          Exp      -> Mod(Exp,Exp)
          Exp      -> Div(Exp,Exp)
          Exp      -> Mul(Exp,Exp)
          Exp      -> Int(IntConst)
          Exp      -> Var(Id)
          IntConst -> <string>
          Id       -> <string>

Invoke rtg2sig:

      > rtg2sig -i Exp.rtg -o Exp.str

I you don\'t specify an output file, then you need to specify the
desired module name with the `--module` option.

The result is the following Stratego module:

      module Exp
      imports list-cons option
      signature
        constructors
          Minus : Exp * Exp -> Exp
          Plus  : Exp * Exp -> Exp
          Mod   : Exp * Exp -> Exp
          Div   : Exp * Exp -> Exp
          Mul   : Exp * Exp -> Exp
          Int   : IntConst -> Exp
          Var   : Id -> Exp
                : String -> IntConst
                : String -> Id

This Stratego module can be imported in you Stratego transformation
tool.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
