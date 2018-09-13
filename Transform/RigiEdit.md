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
    Page](http://www.program-transformation.org/edit/Transform/RigiEdit?t=1536826552)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/RigiEdit)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/RigiEdit)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/RigiEdit?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/RigiEdit?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/RigiEdit?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/RigiEdit?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/RigiEdit?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/RigiEdit?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/RigiEdit?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/RigiEdit?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/RigiEdit)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/RigiEdit?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/RigiEdit?template=oopsmore&param1=1.4&param2=1.4)
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
Rigi Edit {#rigi-edit .twikiTopicTitle}
=========

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

The Rigi user interface is a graph editor, called
[RigiEdit](RigiEdit){.twikiLink} (`rigiedit`), which is used to browse,
analyze, and modify a graph that models a given system. This graph is
simplified by hierarchically clustering related artifacts into
subsystems that, in turn, are clustered into larger subsystems.

![img3.gif](http://www.rigi.cs.uvic.ca/downloads/rigi/doc/img3.gif)

If your Rigi environment is setup:

-   executable is located at `$RIGI/bin/rigiedit`

------------------------------------------------------------------------

**Configuration Variables**

[RigiEdit](RigiEdit){.twikiLink} can be configured at the Workbench
window: Options-\> Configuration. The configuration is stored in to the
`rigicfg.env` file.

`WEBBROWSER`:

-   See [RigiFAQ](RigiFAQ){.twikiLink}
-   For Netscape see
    <http://home.netscape.com/newsref/std/x-remote.html>
-   See <http://www.javaworld.com/javaworld/javatips/jw-javatip66.html>
    -   Unix: netscape -remote openURL(<http://>\...)
    -   Windoze: rundll32 url.dll,FileProtocolHandler <http://>\...

Default settings of the the `rigicfg.env` file:

    # RigiEdit configuration file
    # File:    .../rigicfg.env
    # Created: ...

    CANVASCOLOR = 
    DBDIR = $RIGI/Rigi/db
    DBREFDIR = $RIGI/Rigi/db
    DEMOFONT = -*-helvetica-bold-r-normal--*-120-*-*-*-*-*-*
    GRAPHFONT = -*-helvetica-medium-r-normal--*-100-*-*-*-*-*-*
    ICONDIR = $RIGI/Rigi/icons
    MAXCANVASDIM = 1280 1024
    MESSAGEFONT = -*-helvetica-bold-r-normal--*-120-*-*-*-*-*-*
    NUMBACKSTORES = 2
    RIGIBIN = $RIGI/bin
    RIGIDBHOST = 
    RIGIDBPORT = 0
    RIGIDOMAIN = c
    RIGIINIT = $RIGI/Rigi/domain
    RIGILIB = $RIGI/Rigi
    RIGIRCL = $RIGI/Rigi/rcl/rc.rcl
    RIGISTY = $RIGI/Rigi/rcl/sty/rigi.rcl
    RIGITITLE = Rigi Visual Editor - RigiEdit
    RIGIURCL = 
    RIGIUSER = ~
    RIGIUSTY = 
    ROOTFRAMEDIM = 529 456
    ROOTLOCATION = 0 185
    ROOTWINDOWDIM = 500 400
    SRCDIR = $RIGI/Rigi/icons
    TEXTEDITOR = xterm -e vi +%d
    TEXTFONT = -*-courier-medium-r-normal--*-100-*-*-*-*-*-*
    TMPDIR = /tmp
    WEBBROWSER = netscape -remote openURL(%s)
    WEBROOT = http://
    WORKBENCHFONT = -*-helvetica-bold-r-normal--*-120-*-*-*-*-*-*

------------------------------------------------------------------------

[CategoryRigi](CategoryRigi){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
