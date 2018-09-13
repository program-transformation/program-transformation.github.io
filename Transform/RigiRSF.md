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
    Page](http://www.program-transformation.org/edit/Transform/RigiRSF?t=1536826554)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/RigiRSF)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/RigiRSF)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/RigiRSF?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/RigiRSF?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Transform/RigiRSF?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/RigiRSF?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Transform/RigiRSF?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/RigiRSF?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/RigiRSF?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/RigiRSF?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/RigiRSF)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/RigiRSF?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Transform/RigiRSF?template=oopsmore&param1=1.7&param2=1.7)
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
Rigi [RSF](RSF){.twikiLink} {#rigi-rsf .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Specification: [RigiRSFSpecification](RigiRSFSpecification){.twikiLink}

*Errata:* In a `source-location` the elements are separated with comma,
not semicolon.

*Errata for \"Appendix: Tool Support\":* `rigiedit` can also read
Stuctured [RSF](RSF){.twikiLink}.

The specification discusses the following [RSF](RSF){.twikiLink}
formats:

-   (3-tuple) Unstructured [RSF](RSF){.twikiLink}
-   Partly structured [RSF](RSF){.twikiLink}
-   Stuctured [RSF](RSF){.twikiLink}
-   4-tuple unstructured [RSF](RSF){.twikiLink}

You have to be careful about the format transformation that the tools
perform. *If you run `htmlrsf` and `sortrsf` without command line args,
they change 4-tuple unstructured [RSF](RSF){.twikiLink} to (3-tuple)
unstructured [RSF](RSF){.twikiLink}!*

See also [RigiUserManual](RigiUserManual){.twikiLink}, Section 4.7.1.

See also <http://calla.ics.uci.edu/reveng/toolbase/moin.cgi/RSF>.

------------------------------------------------------------------------

Typically an [RSF](RSF){.twikiLink} file adheres to a certain schema.
For example, an [RSF](RSF){.twikiLink} file generated with `cparse` will
adhere to the *cparse* schema.

The schema is documented in 3 files:

-   `Riginode`: The node types
-   `Rigiarc`: The arc types
-   `Rigiattr`: The node and arc attributes

`rigiedit` expects a directory with the name of the domain containing
these files at `$RIGI/Rigi/domain`.

See [RigiUserManual](RigiUserManual){.twikiLink}, Section 4.4.

(There is a bit more information in Scott Tilleys Ph.D. Thesis
\"Domain-Retargetable Reverse Engineering\", Section A.2.3, page 126f.)

------------------------------------------------------------------------

**Sample [RSF](RSF){.twikiLink} Files**

Unstructured [RSF](RSF){.twikiLink}:

-   Mozilla:
    <http://www.rigi.csc.uvic.ca/rigi/mozilla/mozilla.rsf.sorted.gz>
    (cparse domain)
-   gnuplot:
    <http://www.cs.ubc.ca/~murphy/cpsc507/winter01/schedule/gnuplot.rsf>
    (cparse domain)
-   Linux: <http://plg1.cs.uwaterloo.ca/~itbowman/rsf/> (extracted with
    cfx, unknown domain)

Structured [RSF](RSF){.twikiLink}:

-   List demo: `$RIGI/Rigi/db/list-d/rsf` (c domain)
-   Ray demo: `$RIGI/Rigi/db/ray-d/rsf` (c domain)
-   SQL/DS demo: `$RIGI/Rigi/db/arixi-d/rsf` (plas domain)

------------------------------------------------------------------------

**RSF Generators**

-   from C++
    -   Columbus/CAN
        -   <http://www.frontendart.com>
        -   <http://calla.ics.uci.edu/reveng/toolbase/moin.cgi/Columbus_2fCAN>
    -   `vacppparse` based on IBM
        [VisualAge[^?^](http://www.program-transformation.org/edit/Transform/VisualAge?topicparent=Transform.RigiRSF)]{.twikiNewLink
        style="background : #FFFFCE;"} C++
-   from Java
    -   [SHriMP](SHriMP){.twikiLink} Java Extractor
    -   jCosmo
        -   <http://www.cwi.nl/projects/renovate/javaQA/instructions.html>
        -   <http://calla.ics.uci.edu/reveng/toolbase/moin.cgi/jCosmo>

------------------------------------------------------------------------

**RSF Querying and Manipulation**

The structure of [RSF](RSF){.twikiLink} enables easy manipulation with
standard UNIX text processing tools.

For more formal manipulation of [RSF](RSF){.twikiLink} you can use Dirk
Beyer\'s [CrocoPat](CrocoPat){.twikiLink} tool:
<http://www.cs.sfu.ca/~dbeyer/CrocoPat/>

------------------------------------------------------------------------

[CategoryRigi](CategoryRigi){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
