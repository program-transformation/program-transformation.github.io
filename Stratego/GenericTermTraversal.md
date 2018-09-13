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
    Page](http://www.program-transformation.org/edit/Stratego/GenericTermTraversal?t=1536825584)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/GenericTermTraversal)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/GenericTermTraversal)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/GenericTermTraversal?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/GenericTermTraversal?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/GenericTermTraversal?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/GenericTermTraversal?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/GenericTermTraversal?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/GenericTermTraversal?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/GenericTermTraversal?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/GenericTermTraversal?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/GenericTermTraversal)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/GenericTermTraversal?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/GenericTermTraversal?template=oopsmore&param1=1.4&param2=1.4)
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
Generic Term Traversal {#generic-term-traversal .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

A *generic* [term traversal](TermTraversal){.twikiLink} is a traversal
strategy that is parameterized with the transformation or
transformations that should be applied when visiting subterms.

The generic term traversal strategies defined in the [Stratego Standard
Library[^?^](http://www.program-transformation.org/edit/Stratego/StrategoStandardLibrary?topicparent=Stratego.GenericTermTraversal)]{.twikiNewLink
style="background : #FFFFCE;"} can be divided into two main categories:

-   [One pass
    traversals[^?^](http://www.program-transformation.org/edit/Stratego/OnePassTraversals?topicparent=Stratego.GenericTermTraversal)]{.twikiNewLink
    style="background : #FFFFCE;"} do one (possibly partial) traversal
    over a term
-   [Fixpoint
    traversals[^?^](http://www.program-transformation.org/edit/Stratego/FixpointTraversals?topicparent=Stratego.GenericTermTraversal)]{.twikiNewLink
    style="background : #FFFFCE;"} keep traversing a term until no more
    applications of the specified strategy can be found

[Generic term traversal
operators](GenericTermTraversalOperators){.twikiLink} support the
definition of [generic term traversal](GenericTermTraversal){.twikiLink}
strategies such as `topdown` and `bottomup`.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
