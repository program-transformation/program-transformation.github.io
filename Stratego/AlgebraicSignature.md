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
    Page](http://www.program-transformation.org/edit/Stratego/AlgebraicSignature?t=1536825563)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/AlgebraicSignature)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/AlgebraicSignature)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/AlgebraicSignature?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/AlgebraicSignature?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Stratego/AlgebraicSignature?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/AlgebraicSignature?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/AlgebraicSignature?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/AlgebraicSignature?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/AlgebraicSignature?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/AlgebraicSignature)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/AlgebraicSignature?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Stratego/AlgebraicSignature?template=oopsmore&param1=1.3&param2=1.3)
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
Algebraic Signature {#algebraic-signature .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

An *algebraic signature* describes the structure of a set of terms. A
signature introduces one or more *AlgebraicSorts*, i.e., collections of
terms. Sorts are inhabited by declaring *TermConstructors*. A
constructor has a name and zero or more subterms. A constructor is
declared by stating its name, the list of sorts of its direc subterms
and the sort of the constructed term. Constructor names may be
overloaded. The sorts `String` and `Int` are predefined.

A typical example of a signature is the following description of
[LambdaCalculus[^?^](http://www.program-transformation.org/edit/Stratego/LambdaCalculus?topicparent=Stratego.AlgebraicSignature)]{.twikiNewLink
style="background : #FFFFCE;"} expressions.

    signature
      sorts Exp 
      constructors
        Var : String -> Exp
        App : Exp * Exp -> Exp
        Abs : String * Exp -> Exp

### []{#Term_Injections} Term Injections

A term injection is a constructor-less constructor in a signature.

Example:

    signature
      sorts Var Exp
      constructors
        Var : String -> Var
            : Var -> Exp
        Abs : Var * Exp -> Exp

Issues

-   [FixedLengthTuple](FixedLengthTuple){.twikiLink}
-   [TermAnnotation](TermAnnotation){.twikiLink}
-   [PolymorphicTypes[^?^](http://www.program-transformation.org/edit/Stratego/PolymorphicTypes?topicparent=Stratego.AlgebraicSignature)]{.twikiNewLink
    style="background : #FFFFCE;"}

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 09 Dec 2001\

------------------------------------------------------------------------

[CategoryGlossary](CategoryGlossary){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
