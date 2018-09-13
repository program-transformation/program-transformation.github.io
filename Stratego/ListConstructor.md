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
    Page](http://www.program-transformation.org/edit/Stratego/ListConstructor?t=1536825597)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ListConstructor)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ListConstructor)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ListConstructor?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ListConstructor?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Stratego/ListConstructor?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/ListConstructor?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/ListConstructor?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/ListConstructor?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/ListConstructor?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/ListConstructor?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ListConstructor)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ListConstructor?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Stratego/ListConstructor?template=oopsmore&param1=1.5&param2=1.5)
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
List Constructor {#list-constructor .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

In the ATerm representation lists are represented as terms of the form
`[t1,...,tn]`. This is also the syntax for lists in Stratego; extended
with the notation `[t1,...,tn|tl]` for indicating a tail of the list.
This extension is necessary to take construct and deconstruct lists of
arbitrary length.

In the current implementation (upto
[StrategoRelease064](StrategoRelease064){.twikiLink}) lists are
represented internally by means of the contructors `Cons` and `Nil`.
Thus `[t1,...,tn]` is represented internally as
`Cons(t1,...,Cons(tn,Nil))`. As a consequence ATerms are translated at
every interface between internal and external representation (reading
and writing).

In the new [ImplementationScheme](ImplementationScheme){.twikiLink}
introduced in [StrategoRelease06](StrategoRelease06){.twikiLink} it has
become feasible to directly use the ATerm representation for lists. This
should be beneficial for performance.

This requires that lists are only constructed using the ATerm `Cons` and
`Nil` operations. In the old representation it is possible to use other
constructors for constructing lists, such as `Conc`, which can be
useful.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 04 Jan 2002\

Starting with [StrategoRelease07](StrategoRelease07){.twikiLink} lists
will be constructed according to the scheme described above. An attempt
to construct a term of the form `[x | xs]` where `xs` is not a proper
list results in failures.

The special status of lists affects all generic term manipulation
operations such as generic traversal operators and term
explosion/implosion. This special status makes it possible to adapt the
semantics of [ListTraversal](ListTraversal){.twikiLink}, treating lists
as varyadic constructors instead of as constructed with `Nil` and
`Cons`.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 06 Jan 2002

------------------------------------------------------------------------

[CategoryDone[^?^](http://www.program-transformation.org/edit/Stratego/CategoryDone?topicparent=Stratego.ListConstructor)]{.twikiNewLink
style="background : #FFFFCE;"} \| [ToDo](ToDo){.twikiLink} \|
[CompilerImprovements](CompilerImprovements){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.ListConstructor moved from Stratego.ListConstructors on 06 Jan
2002 - 16:31 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}* - [put
it
back](http://www.program-transformation.org/rename/Stratego/ListConstructor?newweb=Stratego&newtopic=ListConstructors&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
