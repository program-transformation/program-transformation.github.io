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
    Page](http://www.program-transformation.org/edit/Stratego/BreadthFirstTraversal?t=1536825565)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/BreadthFirstTraversal)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/BreadthFirstTraversal)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/BreadthFirstTraversal?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/BreadthFirstTraversal?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/BreadthFirstTraversal?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/BreadthFirstTraversal?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/BreadthFirstTraversal?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/BreadthFirstTraversal)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/BreadthFirstTraversal?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/BreadthFirstTraversal?template=oopsmore&param1=1.2&param2=1.2)
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
Breadth First Traversal {#breadth-first-traversal .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[JoostVisser](../Transform/JoostVisser){.twikiLink} and I have looked at
a breadth first for [Tools.JJTraveler](../Tools/JJTraveler){.twikiLink}.
The breadth first in the Stratego library is incorrect:

-   It doesn\'t apply s to the root (and hence not to any node);
-   It\'s not overall breadht-first, only breadth-first per node.

\-- [ArieVanDeursen](../Transform/ArieVanDeursen){.twikiLink}; 25 Nov
2001.

It is indeed not a correct implementation of breadth first, but it does
actually apply transformations. Consider the definition:

      breadth-first(s) = 
        rec x(all(s); all(x))

This first applies `s` to all direct subterms of the root, and then
recursively applies `x` to the direct sub-terms. The difference with
topdown is that all subterms are visited, before visiting subterms
recursively. What is a better name for this strategy? `kids-first`
maybe?

An implementation of proper breadth-first should employ a global queue
data structure to which terms to be visited should be added. It is also
interesting to consider using
[TermAnnotation](TermAnnotation){.twikiLink} to let a term point to the
next term in a breadth-first traversal.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 09 Dec 2001

------------------------------------------------------------------------

[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.BreadthFirstTraversal)]{.twikiNewLink
style="background : #FFFFCE;"} \| [ToDo](ToDo){.twikiLink} \|
[LibraryImprovements](LibraryImprovements){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
