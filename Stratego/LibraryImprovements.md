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
    Page](http://www.program-transformation.org/edit/Stratego/LibraryImprovements?t=1536825597)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/LibraryImprovements)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/LibraryImprovements)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/LibraryImprovements?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/LibraryImprovements?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    9](http://www.program-transformation.org/view/Stratego/LibraryImprovements?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Stratego/LibraryImprovements?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Stratego/LibraryImprovements?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/LibraryImprovements?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Stratego/LibraryImprovements?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/LibraryImprovements?rev1=1.7&rev2=1.6)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/LibraryImprovements)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/LibraryImprovements?template=oopsmore&param1=1.9&param2=1.9)
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
    \...](http://www.program-transformation.org/oops/Stratego/LibraryImprovements?template=oopsmore&param1=1.9&param2=1.9)
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
Library Improvements {#library-improvements .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Below is a list of ideas for improvements and extensions of the
[Stratego standard
library[^?^](http://www.program-transformation.org/edit/Stratego/StrategoStandardLibrary?topicparent=Stratego.LibraryImprovements)]{.twikiNewLink
style="background : #FFFFCE;"}. Feel free to add items to the list or
even to start new topics.

-   [NewName](NewName){.twikiLink}
-   [BreadthFirstTraversal](BreadthFirstTraversal){.twikiLink}

------------------------------------------------------------------------

-   Document Library: The documentation in the library modules should be
    improved
    -   [ExtendibleDocumentationGenerator](ExtendibleDocumentationGenerator){.twikiLink}

<!-- -->

-   Rationalize the io library; find out if all files that are opened
    are also closed.
    -   [Improve IO Facilities In
        SSL](ImproveIOFacilitiesInSSL){.twikiLink}

<!-- -->

-   Systematization of the library:
    -   define primitives in separate module, e.g., io-prim.r or
        table-prim.r
    -   make subcollections such that not the entire library needs to be
        imported, e.g., sys, list, \...

<!-- -->

-   dtime should count children time as well
    -   time-self: time only self process
    -   time-all: time children as well

<!-- -->

-   better naming scheme for the collect strategies

------------------------------------------------------------------------

[ToDo](ToDo){.twikiLink} \| Contributions by
[EelcoVisser](../Main/EelcoVisser){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
