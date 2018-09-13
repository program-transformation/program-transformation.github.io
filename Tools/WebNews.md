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
    Page](http://www.program-transformation.org/edit/Tools/WebNews?t=1536825760)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/WebNews)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/WebNews)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/WebNews?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/WebNews?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    9](http://www.program-transformation.org/view/Tools/WebNews?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Tools/WebNews?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Tools/WebNews?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Tools/WebNews?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Tools/WebNews?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Tools/WebNews?rev1=1.7&rev2=1.6)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/WebNews)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/WebNews?template=oopsmore&param1=1.9&param2=1.9)
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
    \...](http://www.program-transformation.org/oops/Tools/WebNews?template=oopsmore&param1=1.9&param2=1.9)
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
Web News {#web-news .twikiTopicTitle}
========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**News about XT** *Version 1.0*

-   Released: Jun 14, 2002
-   Bundles the most recent versions of XT\'s sub-component\'s. See the
    file [SOFTWARE XT
    1\_0[^?^](http://www.program-transformation.org/edit/Tools/SOFTWAREXT1_0?topicparent=Tools.WebNews)]{.twikiNewLink
    style="background : #FFFFCE;"} for the complete list of packages
    bundled by XT and their version numbers.
-   List of most significant changes since version 0.9:
    -   [XT[^?^](http://www.program-transformation.org/edit/Tools/XT?topicparent=Tools.WebNews)]{.twikiNewLink
        style="background : #FFFFCE;"} now runs on Windows platform
        using
        [CygWin[^?^](http://www.program-transformation.org/edit/Tools/CygWin?topicparent=Tools.WebNews)]{.twikiNewLink
        style="background : #FFFFCE;"}.
    -   The [GraphViz](GraphViz){.twikiLink} package from AT&T is no
        longer bundled with
        [XT[^?^](http://www.program-transformation.org/edit/Tools/XT?topicparent=Tools.WebNews)]{.twikiNewLink
        style="background : #FFFFCE;"}. You can download it yourselve
        from <http://www.graphviz.org>.
    -   Stratego:
        -   Support for \`native\' ATerm lists and tuples
        -   List traversal: lists considered as varyadic constructors
        -   Global choice operators ++ and \<++ support global
            backtracking
        -   Bagof returns list of all possible results for ++ and \<++
        -   Guarded left choice s1 \< s2 + s3 commits after s1 succeeds
        -   Support for term annotations t1{t2}
        -   Many new library strategies
        -   Constant term caching in the compiler
    -   Grammar Base:
        -   New grammars:
            -   Java\_1\_1.1
            -   fdl.1
            -   asfix2me.1
            -   asf.1
            -   sdf.2.4
            -   stratego.0.7
    -   [GPP](GPP){.twikiLink}:
        -   Added support for layout preserving pretty-printing.
    -   SDF-Tools:
        -   Added fdl2sdf which transforms a feature description written
            in the Feature Description Language (FDL) to SDF.
        -   sdf-bracket: Generalized and improved bracket insertion
            algorithm.

*Version 0.9*

-   released: Nov 29, 2001
-   Bundles the most recent versions of XT\'s sub-component\'s. See the
    file
    [SOFTWARExt09[^?^](http://www.program-transformation.org/edit/Tools/SOFTWARExt09?topicparent=Tools.WebNews)]{.twikiNewLink
    style="background : #FFFFCE;"} for the complete list of packages
    bundled by XT and their version numbers.

**2001-11-12**

-   The wiki pages of this site are now individually bookmarkable.

*Version 0.8*

-   released: Sep 21, 2001
-   Bundles the most recent versions of XT\'s sub-component\'s. See the
    file
    [SOFTWARExt08[^?^](http://www.program-transformation.org/edit/Tools/SOFTWARExt08?topicparent=Tools.WebNews)]{.twikiNewLink
    style="background : #FFFFCE;"} for the complete list of packages
    bundled by XT and their version numbers.

*Version 0.7*

-   released: Jun 1, 2001
-   Updated pkg-list and dev-pkg-list to bundle the most recent versions
    of XT\'s sub-component\'s. See the file
    [SOFTWARExt07[^?^](http://www.program-transformation.org/edit/Tools/SOFTWARExt07?topicparent=Tools.WebNews)]{.twikiNewLink
    style="background : #FFFFCE;"} for the complete list of packages
    bundled by XT and their version numbers.

*Version 0.6*

-   released: February 21, 2000
-   Updated pkg-list and dev-pkg-list to bundle the most recent versions
    of XT\'s sub-component\'s. See the file
    [SOFTWARExt06[^?^](http://www.program-transformation.org/edit/Tools/SOFTWARExt06?topicparent=Tools.WebNews)]{.twikiNewLink
    style="background : #FFFFCE;"} for the complete list of packages
    bundled by XT and their version numbers.

*Version 0.5*

-   Released on December 1, 2000
-   Updated pkg-list and dev-pkg-list to bundle the most recent versions
    of XT\'s sub-component\'s. See the file SOFTWARE for the complete
    list of packages bundled by XT and their version numbers.

*Version 0.4*

-   Released on November 12, 2000
-   XT now uses [AutoBundle](AutoBundle){.twikiLink} software.
-   Support added for creating patches (\"gmake diff\") and for building
    packages (\"gmake pkg\").
-   JJForester added to the package list.

*Version 0.3*

-   Released on September 1, 2000
-   Upgraded to use newest versions of constituent software packages
    (see file SOFTWARE for details).
-   Integration tests have been added.
-   The new XT site is at: <http://www.program-transformation.org/xt/>.

*2000-08-25*

-   The web site has been moved to
    <http://www.program-transformation.org/xt>
-   The wiki pages are now editable for any visitor of the site.

*Version 0.2*

-   XT now uses automake and configure to configure and build all
    constituents. On top of this XT offers a script that takes care of
    collecting (downloading or checking-out) all constituent packages.
-   A wiki site for XT was created: <http://www.cs.uu.nl/~visser/xt/>.
-   The generic pretty-printer ([GPP](GPP){.twikiLink}) has been added
    to the distribution.

*Version 0.1.1* : released: January 24, 2000

-   Added asource to the distribution

*Version 0.1* : released: January 21, 2000

-   This is the first (experimental) release of XT, a bundle of
    transformation tools.

**See also**

-   [WebChanges](WebChanges){.twikiLink}
-   [XtDownload](XtDownload){.twikiLink}
-   [XTDocumentation](XTDocumentation){.twikiLink}
-   [XTTaskList[^?^](http://www.program-transformation.org/edit/Tools/XTTaskList?topicparent=Tools.WebNews)]{.twikiNewLink
    style="background : #FFFFCE;"}.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.WebNews moved from Tools.XTNews on 11 Nov 2001 - 23:46 by
[EelcoVisser](../Main/EelcoVisser){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tools/WebNews?newweb=Tools&newtopic=XTNews&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
