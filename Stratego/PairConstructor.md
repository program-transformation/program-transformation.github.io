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
    Page](http://www.program-transformation.org/edit/Stratego/PairConstructor?t=1536825604)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/PairConstructor)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/PairConstructor)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/PairConstructor?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/PairConstructor?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/PairConstructor?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/PairConstructor?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/PairConstructor?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/PairConstructor?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/PairConstructor?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/PairConstructor?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/PairConstructor)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/PairConstructor?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/PairConstructor?template=oopsmore&param1=1.4&param2=1.4)
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
Pair Constructor {#pair-constructor .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The `Pair` constructor `Pair(x, y)` was used in `thread` and traversals
for distribution of environments during traversal.

The `Pair` constructor has become obsolete with the introduction of
[FixedLengthTuple](FixedLengthTuple){.twikiLink} in
[StrategoRelease07](StrategoRelease07){.twikiLink}.

Until [StrategoRelease071](StrategoRelease071){.twikiLink} the `Pair`
constructor will be defined as an overlay

    overlays
      Pair(x, y) = (x, y)

After that it will be removed from the library.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 06 Jan 2002\

------------------------------------------------------------------------

[CategoryDone[^?^](http://www.program-transformation.org/edit/Stratego/CategoryDone?topicparent=Stratego.PairConstructor)]{.twikiNewLink
style="background : #FFFFCE;"}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
