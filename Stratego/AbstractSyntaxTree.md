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
    Page](http://www.program-transformation.org/edit/Stratego/AbstractSyntaxTree?t=1536825563)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/AbstractSyntaxTree)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/AbstractSyntaxTree)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/AbstractSyntaxTree?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/AbstractSyntaxTree?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/AbstractSyntaxTree?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/AbstractSyntaxTree?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/AbstractSyntaxTree?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/AbstractSyntaxTree)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/AbstractSyntaxTree?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/AbstractSyntaxTree?template=oopsmore&param1=1.2&param2=1.2)
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
Abstract Syntax Tree {#abstract-syntax-tree .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#Description} Description
----------------------------

An abstract syntax tree is a tree representation of a source program. It
abstracts more from the source program than a [parse
tree[^?^](http://www.program-transformation.org/edit/Stratego/ParseTree?topicparent=Stratego.AbstractSyntaxTree)]{.twikiNewLink
style="background : #FFFFCE;"}. Usually it doesn\'t contain layout
information and comments.

In [StrategoXT](StrategoXT){.twikiLink} the
[ATerm[^?^](http://www.program-transformation.org/edit/Stratego/ATerm?topicparent=Stratego.AbstractSyntaxTree)]{.twikiNewLink
style="background : #FFFFCE;"} format is used to exchange abstact syntax
trees between transformation tools. [Stratego
signatures](StrategoSignature){.twikiLink} desribe the [abstract
syntax](AbstractSyntax){.twikiLink} of a language.

[]{#Example} Example
--------------------

The expression `1 + 2 * a` might be represented in an abstract syntax
tree in the ATerm format as:

      Plus(
        Int("1")
      , Mul(
          Int("2")
        , Var("a")
        )
      )

As a more interesting example consider the following Tiger program:

      let function fact(n : int) : int =
            if n < 1 then 1 else (n * fact(n - 1))
       in printint(fact(10))
      end

In the [Tiger compiler](../Tiger/WebHome){.twikiLink} this program is
represented as:

      Let(
        [ FunDecs(
          [ FunDec("fact", [FArg("n",Tp(Tid("int")))]
            , Tp(Tid("int"))
            , If(
                Lt(Var("n"), Int("1"))
              , Int("1")
              , Seq([
                  Times(Var("n"), Call(Var("fact"),[Minus(Var("n"),Int("1"))]))
                ])
              )
            )
          ])
        ]
      ,[ Call(
           Var("printint")
         , [ Call(Var("fact"),[Int("10")]) ]
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
