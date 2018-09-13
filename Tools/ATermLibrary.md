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
    Page](http://www.program-transformation.org/edit/Tools/ATermLibrary?t=1536825867)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/ATermLibrary)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/ATermLibrary)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/ATermLibrary?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/ATermLibrary?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Tools/ATermLibrary?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Tools/ATermLibrary?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Tools/ATermLibrary?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/ATermLibrary?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Tools/ATermLibrary?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/ATermLibrary?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/ATermLibrary)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/ATermLibrary?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Tools/ATermLibrary?template=oopsmore&param1=1.5&param2=1.5)
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
ATerm Library {#aterm-library .twikiTopicTitle}
=============

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

ATerm libraries implement the internal representation of the [ATerm
Format](ATermFormat){.twikiLink} in some programming language and the
conversion between the external and the internal representation.

[]{#C} C
--------

-   Implements garbage collection of ATerms
-   Ensures maximal subterm sharing
-   Supports the efficient Binary ATerm Format (BAF) in which complete
    sharing of subterms is maintained.

Visit the [official
homepage](http://www.cwi.nl/htbin/sen1/twiki/bin/view/SEN1/ATermLibrary)
for more information and downloads.

[]{#Java} Java
--------------

-   Ensures maximal subterm sharing.
-   Does not support the Binary ATerm Format (BAF)

As far as I know there is no offical homepage for the ATerm library for
Java. The software can be downloaded from the [package base at the
CWI](http://www.cwi.nl/htbin/sen1/twiki/bin/view/SEN1/PackageBase). The
name of the package is `aterm-java`.

[]{#Haskell} Haskell
--------------------

-   [official
    homepage](http://www.cwi.nl/htbin/sen1/twiki/bin/view/SEN1/HaskellATermLibrary)

[]{#Scheme} Scheme
------------------

-   <http://planet.plt-scheme.org/#aterm.plt>

[]{#Publications} Publications
------------------------------

-   [Efficient Annotated
    Terms](../Transform/EfficientAnnotatedTerms){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
