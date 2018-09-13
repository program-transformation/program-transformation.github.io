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
    Page](http://www.program-transformation.org/edit/Transform/RigiInstall?t=1536826553)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/RigiInstall)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/RigiInstall)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/RigiInstall?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/RigiInstall?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Transform/RigiInstall?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/RigiInstall?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Transform/RigiInstall?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/RigiInstall?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/RigiInstall?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/RigiInstall?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/RigiInstall)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/RigiInstall?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Transform/RigiInstall?template=oopsmore&param1=1.7&param2=1.7)
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
Rigi Install {#rigi-install .twikiTopicTitle}
============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

This topic provides information for users of Rigi binary distributions.
See also [RigiDevelopment](RigiDevelopment){.twikiLink} if you work with
Rigi\'s source code.

Installing [RigiEdit](RigiEdit){.twikiLink} basically means that you
have to extract the contents of the archive (ZIP, tar, etc.) into a new
directory. This directory is referred to as `$RIGI`.

**Linux with (ba)sh:**

    > mkdir rigibase
    > cd rigibase
    > export RIGI=`pwd`
    > export PATH=$RIGI/bin:$PATH
    > wget http://www.rigi.cs.uvic.ca/downloads/rigi/ix86-linux2/rigiedit-12-Jan-2003-bin.tar.gz
    > gunzip rigiedit-12-Jan-2003-bin.tar.gz
    > tar xvf rigiedit-12-Jan-2003-bin.tar

To set the environment variables RIGI and [PATH](PATH){.twikiLink} for
tcsh, replace the above two lines with:

    > setenv RIGI `pwd`
    > set path=($RIGI/bin$path)

**Windows:**

You need to set the following system environment variables:

  [Variable](RigiInstall@sortcol=0&table=1&up=0#sorted_table "Sort by this column")   [Example](RigiInstall@sortcol=1&table=1&up=0#sorted_table "Sort by this column")
  ----------------------------------------------------------------------------------- ----------------------------------------------------------------------------------
  RIGI                                                                                C:\\Rigi
  TCL\_LIBRARY                                                                        \%RIGI%\\lib\\tcl8.4
  TK\_LIBRARY                                                                         \%RIGI%\\lib\\tk8.4
  Path                                                                                \%RIGI%\\bin

You can include the following lines into the `autoexec.bat`:

    rem following lines are related to RIGI
    set RIGI=c:/rigi
    set TCL_LIBRARY=%RIGI%/lib/tcl7.4
    set TK_LIBRARY=%RIGI%/lib/tk4.0
    path=%path%;%RIGI%\bin

------------------------------------------------------------------------

**General Troubleshooting**

-   (No problems reported yet.)

**Troubleshooting for Windows**

-   Make sure that the path where you install Rigi does not contain
    white spaces. If white spaces are in the path you see an error
    message such as the following:

<!-- -->

    C:\...>rigiedit
    Welcome to RigiEdit Version 12-Jan-2003
    Copyright 1986-1998,
    H.A. Muller, University of Victoria, All rights reserved
    Configuration used: C:/...path with white spaces.../rigicfg.env
    rigiedit error: failure to evaluate RIGISTY
    rigiedit error: wrong # args: should be "source fileName"
    rigiedit error: exec_command(canvas_build .window1 1 "" 500 400 1280 1024 0 185)
    ...

**Troubleshooting for Linux**

-   (No problems reported yet.)

------------------------------------------------------------------------

[CategoryRigi](CategoryRigi){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
