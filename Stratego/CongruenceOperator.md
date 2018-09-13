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
    Page](http://www.program-transformation.org/edit/Stratego/CongruenceOperator?t=1536825572)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/CongruenceOperator)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/CongruenceOperator)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/CongruenceOperator?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/CongruenceOperator?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/CongruenceOperator?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/CongruenceOperator?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/CongruenceOperator?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/CongruenceOperator?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/CongruenceOperator?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/CongruenceOperator)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/CongruenceOperator?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/CongruenceOperator?template=oopsmore&param1=1.3&param2=1.3)
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
Congruence Operator {#congruence-operator .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

A term consisting of a constructor C and subterms ti:

    C(t1, t2, ..., tn)

defines a congruence operator

    C(s1, s2, ..., sn)

This is an operator that first matches a term `C(t1, t2,...,tn)`, then
applies `s1` to `t1`, `s2` to `t2`, \..., `sn` to `tn`. This is used
e.g. in conjunction with the recursive traversal operator to define
specific data structure traversals.

For example, using the congruence strategy `FunCall(s1,s2)` is
equivalent to applying

    R :
      FunCall(a,b) -> FunCall(newa,newb) 
      where
        <s1> a => newa
      ; <s2> b => newb

which is equivalent to

    {a, b, newa, newb :
      ?FunCall(a,b)
      ; where(    
          <s1> a => newa
        ; <s2> b => newb
        )
      ; !FunCall(newa,newb)
    }

This equivalent specification uses [match](MatchStrategy){.twikiLink}
and [build
strategies[^?^](http://www.program-transformation.org/edit/Stratego/BuildStrategies?topicparent=Stratego.CongruenceOperator)]{.twikiNewLink
style="background : #FFFFCE;"}, and [variable
scopes[^?^](http://www.program-transformation.org/edit/Stratego/VariableScopes?topicparent=Stratego.CongruenceOperator)]{.twikiNewLink
style="background : #FFFFCE;"} indicated by `{}`.

`FunCall(s1,s2)` is also equivalent to:

    R:
      FunCall(a,b) -> FunCall(<s1> a, <s2> b)

This specification uses a rewriting rule and [term
projection[^?^](http://www.program-transformation.org/edit/Stratego/TermProjection?topicparent=Stratego.CongruenceOperator)]{.twikiNewLink
style="background : #FFFFCE;"}.

[]{#More_exotic_congruences} More exotic congruences
----------------------------------------------------

Tuple congruences `(s1,s2,...,sn)`

List congruences `[s1,s2,...,sn]`

A special list congruence is \[\] which \"visits\" the empty list

### []{#Distributing_congruences} Distributing congruences

    c^D(s1, s2, ..., sn)

`c` is term constructor `^D` syntax to denote distributing congruence
`s1, ..., sn` are strategies.

The meaning is given by

    c^D(s1, ..., sn):
      (c(x1, ..., xn), env) -> c(y1, ..., yn)
      where
        <s1> (x1, env) => y1
      ; <s2> (x2, env) => y2
      ; ...
      ; <sn> (xn, env) => yn

### []{#Threading_congruences} Threading congruences

    c^T(s1, s2, ..., sn)

`c` is term constructor `^T` is syntax to denote threading congruence

The meaning is given by:

    c^T(s1, ..., sn):
      (c(x1, ..., xn), e-first) -> (c(y1, ..., yn), e-last))
      where
        <s1> (x1, e-first) => (y1, e2)
      ; <s2> (x2, e2) => (y2, e3)
      ; ...
      ; <sn> (xn, en) => (yn, e-last)

------------------------------------------------------------------------

[CategoryGlossary](CategoryGlossary){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
