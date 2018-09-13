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
    Page](http://www.program-transformation.org/edit/Tools/ATermFormat?t=1536825757)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/ATermFormat)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/ATermFormat)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/ATermFormat?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/ATermFormat?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Tools/ATermFormat?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Tools/ATermFormat?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Tools/ATermFormat?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/ATermFormat?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/ATermFormat?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/ATermFormat)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/ATermFormat?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Tools/ATermFormat?template=oopsmore&param1=1.3&param2=1.3)
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
ATerm Format {#aterm-format .twikiTopicTitle}
============

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

[]{#Introduction} Introduction
------------------------------

The ATerm (Annotated Term) Format is a format for exchanging structured
data between tools. The ATerm format is a generic internal and external
representation of data by means of simple prefix terms.

[]{#Abstract_Data_Type} Abstract Data Type
------------------------------------------

An ATerm is an expression according to the following grammar:

      t  := bt                 -- basic term
           | bt { t }          -- annotated term

      bt := C                  -- constant
           | C(t1,...,tn)      -- n-ary constructor
           | (t1,...,tn)       -- n-ary tuple
           | [t1,...,tn]       -- list
           | "ccc"             -- quoted string
           | int               -- integer
           | real              -- floating point number
           | blob              -- binary large object

Here `C` is a constructor name, which is either an identifier or a
quoted string.

[]{#Format} Format
------------------

ATerms can be exchanged in several formats:

-   The Binary ATerm Format (BAF) is an efficient format that preserves
    maximal sharing.
-   The Textual ATerm Format (TAF) preserves maximal sharing but is not
    as efficient as BAF.
-   The plain text format (TEXT) is a textual format that does not
    preserve maximal sharing.

The `baffle` tool in the [ATerm Library](ATermLibrary){.twikiLink} can
be used to convert the formats.

[]{#Library} Library
--------------------

The ATerm Format is supported by [ATerm
Libraries](ATermLibrary){.twikiLink} for C, Java, and Haskell.

[]{#Application} Application
----------------------------

The ASF+SDF Meta Environment operates on [AsFix](AsFix){.twikiLink}
representations of source code in the ATerm format.

The [Stratego](../Stratego/WebHome){.twikiLink} program transformation
language uses ATerms to represent abstract syntax trees:

-   Specification defines transformation of ATerms
-   ATerm library is used in implementation of terms
-   Exchange of syntax trees as ATerms

[]{#Publications} Publications
------------------------------

The ATerm format is described in the following publication:

-   M. G. J. van den Brand, H. A. de Jong, P. Klint, and P. A. Olivier.
    [Efficient Annotated
    Terms](../Transform/EfficientAnnotatedTerms){.twikiLink}.
    *Software - Practice \\& Experience*, 30:259-291, 2000.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
