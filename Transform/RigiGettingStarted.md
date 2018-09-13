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
    Page](http://www.program-transformation.org/edit/Transform/RigiGettingStarted?t=1536826553)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/RigiGettingStarted)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/RigiGettingStarted)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/RigiGettingStarted?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/RigiGettingStarted?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    9](http://www.program-transformation.org/view/Transform/RigiGettingStarted?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Transform/RigiGettingStarted?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Transform/RigiGettingStarted?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Transform/RigiGettingStarted?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Transform/RigiGettingStarted?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/RigiGettingStarted?rev1=1.7&rev2=1.6)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/RigiGettingStarted)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/RigiGettingStarted?template=oopsmore&param1=1.9&param2=1.9)
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
    \...](http://www.program-transformation.org/oops/Transform/RigiGettingStarted?template=oopsmore&param1=1.9&param2=1.9)
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
Rigi Getting Started {#rigi-getting-started .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Information if you are new to Rigi:

### []{#Purpose} Purpose

Rigi is a [ReverseEngineering](ReverseEngineering){.twikiLink}
environment. It consists of a set of tools: parsers, command-line
utilities, and an interactive graph editor. The core of the system is
the graph editor, [RigiEdit](RigiEdit){.twikiLink}, and most people that
are interested in Rigi are actually interested in the graph editor. (In
fact, the parsers are no longer supported.)

Rigi is a system for understanding large information spaces such as
software programs, documentation, and the World Wide Web. This is done
through a reverse engineering approach that models the system by
extracting artifacts from the information space, organizing them into
higher level abstractions such as components, and presenting the model
graphically with [RigiEdit](RigiEdit){.twikiLink}.The choice of
abstraction depends on its intended function, the intended audience, the
application area, and the goals of the modeling exercise.

If you want to dive deeper, check out the
[RigiPublications](RigiPublications){.twikiLink}. A good starting point
is ***Structural redocumentation: a case study***
([IEEE](IEEE){.twikiLink} Software, January 1995):

-   /pub/Transform/RigiGettingStarted/WTMS-IEEESW-95.pdf
-   <http://rigi.cs.uvic.ca/downloads/papers/pdf/ieee-software-sr.pdf>
-   <http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=363166>

### []{#Downloading_Rigi_and_Getting_the} Downloading Rigi and Getting the Rigi User Manual

To try out Rigi you can download a precompiled version of Rigi; look at
[RigiReleases](RigiReleases){.twikiLink}. To play around with Rigi and
to run some demos you only need [RigiEdit](RigiEdit){.twikiLink}. If you
are a developer and work with the sources look at
[RigiDevelopment](RigiDevelopment){.twikiLink}.

Also download the [RigiUserManual](RigiUserManual){.twikiLink}!

### []{#Installing_Rigi} Installing Rigi

Installing [RigiEdit](RigiEdit){.twikiLink} basically means that you
have to extract the contents of the archive (ZIP, tar, etc.) into a new
directory. This directory is referred to as `$RIGI`.

See [RigiInstall](RigiInstall){.twikiLink} for additional help if you
run into problems.

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

  [Variable](RigiGettingStarted@sortcol=0&table=1&up=0#sorted_table "Sort by this column")   [Example](RigiGettingStarted@sortcol=1&table=1&up=0#sorted_table "Sort by this column")
  ------------------------------------------------------------------------------------------ -----------------------------------------------------------------------------------------
  RIGI                                                                                       C:\\Rigi
  TCL\_LIBRARY                                                                               \%RIGI%\\lib\\tcl8.4
  TK\_LIBRARY                                                                                \%RIGI%\\lib\\tk8.4
  Path                                                                                       \%RIGI%\\bin

You can include the following lines into the `autoexec.bat`:

    rem following lines are related to RIGI
    set RIGI=c:/rigi
    set TCL_LIBRARY=%RIGI%/lib/tcl7.4
    set TK_LIBRARY=%RIGI%/lib/tk4.0
    path=%path%;%RIGI%\bin

### []{#Running_Rigi} Running Rigi

The binary of [RigiEdit](RigiEdit){.twikiLink} is located at
`$RIGI/bin/rigiedit`.

If you execute the binary, you should initially see the Rigi Workbench
window and an empty root window.

![img3.gif](http://www.rigi.cs.uvic.ca/downloads/rigi/doc/img3.gif)
![img5.gif](http://www.rigi.cs.uvic.ca/downloads/rigi/doc/img5.gif)

When you start up [RigiEdit](RigiEdit){.twikiLink}, it checks for the
configuration file `rigicfg.env` in the current working directory. If
the file does not exist [RigiEdit](RigiEdit){.twikiLink} creates the
file with the default settings.

**Linux:**

    > cd $RIGI/bin/
    > ./rigiedit &
    Welcome to RigiEdit Version 12-Jan-2003
    Copyright 1986-1998,
    H.A. Muller, University of Victoria, All rights reserved
    Configuration used: .../bin/rigicfg.env
    > cat rigicfg.env

**Windows:**

Start [RigiEdit](RigiEdit){.twikiLink} by opening up the [\"Run\...\"
dialog](http://en.wikipedia.org/wiki/Run_command) and then typing in
`rigiedit`. This will only work if the `path` system environment
variable is set correctly (see above).

Alternatively, you use the Explorer to navigate to the `rigiedit` binary
and double-click on it.

### []{#Rigi_s_Demos} Rigi\'s Demos

The easiest way to get a first understanding of Rigi\'s capabilities is
running the built-in demos. In the Rigi Workbench use the \"Demo\"
drop-down menu to select between three demos. More details are in the
[RigiUserManual](RigiUserManual){.twikiLink}, Chapter 2.

------------------------------------------------------------------------

[CategoryRigi](CategoryRigi){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
