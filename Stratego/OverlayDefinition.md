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
    Page](http://www.program-transformation.org/edit/Stratego/OverlayDefinition?t=1536825603)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/OverlayDefinition)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/OverlayDefinition)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/OverlayDefinition?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/OverlayDefinition?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/OverlayDefinition?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/OverlayDefinition?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/OverlayDefinition?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/OverlayDefinition)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/OverlayDefinition?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/OverlayDefinition?template=oopsmore&param1=1.2&param2=1.2)
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
Overlay Definition {#overlay-definition .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

### []{#Abstracting_over_Term_Patterns_w} Abstracting over Term Patterns with Overlays

Overlays are abstractions over term patterns that can be used just like
ordinary term constructors.

Overlays can be used to abstract from complex term patterns.

For example, the following overlays define a term language on top of
`AsFixTerms`:

      signature
        sorts AsFixTerm
        constructors
          layout : Sort
          lit   : String -> Sort
          sort   : String -> Sort
          lex   : Sort ->; Sort
          prod   : List(Sort) * Sort * List(Attr) -> Prod
          appl   : Prod * List(AsFixTerm) -> AsFixTer
      overlays
        DefaultLayout = " "
        BinOp(o) = 
          prod([sort("E"), layout, lit(o), layout, sort("E")], sort("E"), [])
        BinExp(x, l1, o, l2, y) = 
          appl(BinOp(o), [x, l1, lit(o), l2, y])
        Add(x, l1, l2, y) = BinExp(x, l1, "+", l2, y) 
        Mul(x, l1, l2, y) = BinExp(x, l1, "*", l2, y) 
        Var(x) = appl(prod([lex(sort("Id"))], sort("E"), []), [x])

This makes it possible to write rules over `AsFixTerms` in terms of
these higher level pseudo constructors:

      rules
        Dist : Mul(x, l1, l2, Add(y, l3, l4, z)) ->
               Add(Mul(x, l1, l2, y), l3, l4, Mul(x, z))

Note that `AsFixTerms` preserve layout from the source code and that the
rule Dist defines how to preserve layout through transformations.

Two limitations of overlays have been resolved:

Overlays can be overloaded and can define default build terms. In the
example above, we would like to further abstract and also provide pseudo
constructors that do not care about layout:

      overlays 
        Add(x, y) = BinExp(x, "+", y)
        Mul(x, y) = BinExp(x, "*", y)

So that we can write

      rules
        Dist : Mul(x, Add(y, z)) -> Add(Mul(x, y), Mul(x, z))

This is now possible because overlays can be overloaded, i.e., overlays
with the same name but different arity can be defined.

To define `BinExp/3` it is necessary to do something with the layout,
for example:

      overlays
        BinExp(x, o, y) =   
          appl(BinOp(o), [x, DefaultLayout, lit(o), DefaultLayout, y])

This requires that all layout has the form `DefaultLayout` (i.e., \" \")
when matching and traversing the term with a congruence.

Overlays can use build default terms to indicate subterms that can be
ignored during matching and in traversal, but need a default value when
constructing an instance.

      BinExp(x, o, y) =   
        appl(BinOp(o), [x, _ DefaultLayout, lit(o), _ DefaultLayout, y])

The last definition uses the pattern \_ `DefaultLayout` to indicate that
the terms at those positions can be ignored during matching and during
congruence traversal. That is, the overlay definition has the following
meaning

      ?BinExp(x, o, y) ->
       ?appl(BinOp(o), [x, _, lit(o), _, y])

      !BinExp(x, o, y) ->
       !appl(BinOp(o), [x, DefaultLayout, lit(o), DefaultLayout, y])

      BinExp(x, o, y) -> // as congruence
       appl(BinOp(o), [x, id, lit(o), id, y])

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
