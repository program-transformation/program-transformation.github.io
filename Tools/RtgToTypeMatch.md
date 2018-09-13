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
    Page](http://www.program-transformation.org/edit/Tools/RtgToTypeMatch?t=1536826226)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/RtgToTypeMatch)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/RtgToTypeMatch)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/RtgToTypeMatch?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/RtgToTypeMatch?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Tools/RtgToTypeMatch?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Tools/RtgToTypeMatch?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Tools/RtgToTypeMatch?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/RtgToTypeMatch?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/RtgToTypeMatch?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/RtgToTypeMatch?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/RtgToTypeMatch)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/RtgToTypeMatch?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Tools/RtgToTypeMatch?template=oopsmore&param1=1.5&param2=1.5)
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
Rtg To Type Match {#rtg-to-type-match .twikiTopicTitle}
=================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[]{#Introduction} Introduction
------------------------------

`rtg2typematch` is a tool for generating a duck-typing-based strategies
that check if an ATerm is of a type as defined in an
[RTG[^?^](http://www.program-transformation.org/edit/Tools/RegularTreeGrammar?topicparent=Tools.RtgToTypeMatch)]{.twikiNewLink
style="background : #FFFFCE;"}. An example will make this more clear.

[]{#Example} Example
--------------------

Let\'s take the RTG produced by the example in the manual page of
[sdf2rtg](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/chunk-chapter/ref-sdf2rtg.html):

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

Apply rtg2typematch:

      > rtg2typematch -i Exp.rtg -o Exp-typematch.str

will result in the module

      module Exp-typematch
      strategies
        is-Exp =
          ?Minus(_, _)
          + ?Plus(_, _)
            + ?Mod(_, _)
              + ?Div(_, _)
                + ?Mul(_, _)
                  + ?Int(_)
                    + ?Var(_)

        is-IntConst =
          is-string

        is-Id =
          is-string

You can call `is-Exp` to check whether a term is of sort Exp. Notice
that the generated code only looks at the name of the constructor. If
the same constructor can be used to produce different sorts, the
typematch strategy of all these sort will accept a term that is an
application of this constructor.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.RtgToTypeMatch moved from Stratego.SignatureToTypeMatch on 29 Jun
2004 - 08:09 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tools/RtgToTypeMatch?newweb=Stratego&newtopic=SignatureToTypeMatch&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
