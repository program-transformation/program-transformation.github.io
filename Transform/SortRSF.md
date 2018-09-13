::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

[![](../pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Transform/SortRSF?t=1536826570)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/SortRSF)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/SortRSF)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/SortRSF?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/SortRSF?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/SortRSF?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/SortRSF?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/SortRSF?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/SortRSF?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/SortRSF?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/SortRSF)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/SortRSF?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/SortRSF?template=oopsmore&param1=1.3&param2=1.3)
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
Sort [RSF](RSF){.twikiLink} {#sort-rsf .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

`sortrsf` is a command line program that is part of the
[RigiSystem](RigiSystem){.twikiLink}.

If your Rigi environment is setup:

-   documentation is located at `$RIGI/doc/rigiutils/sortrsf.html`
-   executable is located at `$RIGI/bin/sortrsf`

This tool is part of `rigiutils`, see
[RigiReleases](RigiReleases){.twikiLink}.

Actually, `sortrsf` and [HtmlRSF](HtmlRSF){.twikiLink} are mostly
equivalent in functionality, except for htmlrsf\'s ability to create
[HTML](HTML){.twikiLink} files.

------------------------------------------------------------------------

Typical usage scenarios:

To transform a file from 4-tuple unstructured [RSF](RSF){.twikiLink} to
(3-tuple) unstructured [RSF](RSF){.twikiLink}:

-   `sortrsf < in.rsf > out.rsf`

(As a side effect, the file gets sorted and duplicate entries get
reomoved!)

To sort a 4-tuple unstructured [RSF](RSF){.twikiLink} (and to keep the
format):

-   `sortrsf -4 < in.rsf > out.rsf`

------------------------------------------------------------------------

[CategoryRigi](CategoryRigi){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::