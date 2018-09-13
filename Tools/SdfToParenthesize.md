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
    Page](http://www.program-transformation.org/edit/Tools/SdfToParenthesize?t=1536825776)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/SdfToParenthesize)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/SdfToParenthesize)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/SdfToParenthesize?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/SdfToParenthesize?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tools/SdfToParenthesize?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/SdfToParenthesize)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/SdfToParenthesize?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tools/SdfToParenthesize?template=oopsmore&param1=1.1&param2=1.1)
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
Sdf To Parenthesize {#sdf-to-parenthesize .twikiTopicTitle}
===================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[]{#Introduction} Introduction
------------------------------

`sdf2parenthesize` generates a Stratego transformation tool that adds
the necessary parentheses to an abstract syntax tree. The information is
obtained from an SDF syntax definition.

[]{#Example} Example
--------------------

For example, if Plus is declared to left associative, then the following
rule will be generated:

      ExpParenthesize :
        Plus(q_15, Plus(o_15, p_15)) -> Plus(q_15, Parenthetical(Plus(o_15, p_15)))

A relative priority related example:

      ExpParenthesize :
        Mul(Plus(v_2, w_2), u_2) -> Mul(Parenthetical(Plus(v_2, w_2)), u_2)

      ExpParenthesize :
        Mul(t_2, Plus(v_2, w_2)) -> Mul(t_2, Parenthetical(Plus(v_2, w_2)))

The tool supports:

#### []{#Relative_priorities} Relative priorities

        Exp "&&"  Exp -> Exp
      > Exp "||"  Exp -> Exp

#### []{#Groups_of_associative_production} Groups of associative productions

        {left:
           Exp "*" Exp -> Exp
           Exp "/" Exp -> Exp
        }
      > {left:
           Exp "+" Exp -> Exp
           Exp "-" Exp -> Exp
        }

#### []{#Associativity_attributes_non_ass} Associativity attributes: non-assoc, assoc, left, right.

      Exp "+"   Exp -> Exp  {left, cons("Plus")}

#### []{#Kernel_SDF_associativities} Kernel SDF associativities

      prod1 assoc prod2

[]{#Open_Issues} Open Issues
----------------------------

Does this solve all the parentheses related problems? No, unfortunately
not. The tool does not support {prefer} attributes, which are for
example used in the dangling else problem.

So, if you want to make sure that

      IfThenElse(_, IfThen(_, _, _), _)

is pretty-printed correctly as:

      if a then (if b then c) else d

then you still need to implement this be hand. Notice that you can
import the generated rules in this handwritten tool. I don\'t have a
clue now I could automate these issues in the generator, since the
`{prefer}` attributes are not really declarative.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
