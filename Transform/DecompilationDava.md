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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationDava?t=1536826457)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationDava)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationDava)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationDava?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationDava?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    35](http://www.program-transformation.org/view/Transform/DecompilationDava?rev=1.35)
    [(diff 34)](http://www.program-transformation.org/rdiff/Transform/DecompilationDava?rev1=1.35&rev2=1.34)
-   [Rev
    34](http://www.program-transformation.org/view/Transform/DecompilationDava?rev=1.34)
    [(diff 33)](http://www.program-transformation.org/rdiff/Transform/DecompilationDava?rev1=1.34&rev2=1.33)
-   [Rev
    33](http://www.program-transformation.org/view/Transform/DecompilationDava?rev=1.33)
    [(diff 32)](http://www.program-transformation.org/rdiff/Transform/DecompilationDava?rev1=1.33&rev2=1.32)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationDava)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationDava?template=oopsmore&param1=1.35&param2=1.35)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationDava?template=oopsmore&param1=1.35&param2=1.35)
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
Decompilation Dava {#decompilation-dava .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#McGill_s_Dava_Java_Decompiler} McGill\'s \"Dava\" Java Decompiler
=====================================================================

::: {.twikiToc}
-   [McGill\'s \"Dava\" Java
    Decompiler](DecompilationDava#McGill_s_Dava_Java_Decompiler)
    -   [Making Dava](DecompilationDava#Making_Dava)
    -   [About Dava](DecompilationDava#About_Dava)
:::

-   -   [Dava tests](DecompilationDavaTest){.twikiLink}

The [Sable](http://www.sable.mcgill.ca) group at [McGill
University](http://www.mcgill.ca), under the leadership of Professor
[Laurie Hendren](http://www.sable.mcgill.ca/~hendren), are working on a
framework called [Soot](http://www.sable.mcgill.ca/soot) for analysing
and optimising Java bytecode. An offshoot of this work, though not
described directly on the Soot page, is the Dava decompiler. This is
mostly the work of Jerome Miecznikowski, whose [masters
thesis](http://www.sable.mcgill.ca/publications/thesis/#jeromeMastersThesis)
is available. A
[paper](http://www.sable.mcgill.ca/publications/#wcre2001) published at
the [Decompilation Workshop](http://reengineer.org/wcre2001/Decomp) at
[WCRE](WCRE){.twikiLink} [2001](http://reengineer.org/wcre2001)
describes the restructuring algorithm used. See also their [tech
report](http://www.sable.mcgill.ca/publications/#report2001-1)
*Decompiling Java Bytecode: Problems, Traps and Pitfalls*. Also of
interest to decompilation researchers is their
[paper](http://www.sable.mcgill.ca/publications/#sas2000) on types:
*Efficient Inference of Static Types for Java Bytecode*. You can get a
working version (with a little effort) from the website. See
[DecompilationDavaTest](DecompilationDavaTest){.twikiLink} for tests.

[]{#Making_Dava} Making Dava
----------------------------

There is a version of Dava in the latest release of Soot (but it is
undocumented, and predates some enhancements mentioned in their paper).
According to the author, the new version is ready, it just needs
integration into a current version of Soot. This version was supposed to
happen early 2003. These instructions and tests relate to the old
version.

Extremely brief installation instructions can be found in the main
author\'s (Jerome Miecznikowski\'s) web page, which was at
<http://www.sable.mcgill.ca/~jerome/public>, in the file INSTALL (still
accessable
[here](http://web.archive.org/web/20031216005420/www.sable.mcgill.ca/~jerome/public/INSTALL)
from [archive.org](http://www.archive.org)). So to use Dava, you just
install Soot, and use some special command line options. You can
download the full source version (5MB), or the version with just the
`classes` directory (2MB). Note that the Jasmin needed is a modification
of the standard Jasmin \"assembler for Java\", so make sure you use the
one provided.

The main problem I had in getting it going is to set the CLASSPATH
environment variable correctly. This worked for me: 1) current directory
(.), 2) path to the `rt.jar` file (include `rt.jar` in this path), 3)
path to the Soot classes directory, and 4) path to the jasmin classes
directory.

To use Dava, alter the CLASSPATH is set up as above, cd to the directory
with the top level .class file to be decompiled, and

    % java soot.Main --dava foo     or
    % java soot.Main --dava --app foo

as per the INSTALL instructions. Note: if you get warnings about phantom
library classes, you probably need to get your CLASSPATH right. There is
more about the `rt.jar` file in the [Soot
tutorial](http://www.sable.mcgill.ca/soot/tutorial). Note: you should
not need to unjar the `rt.jar` file. I found it convenient to set up a
shell program to set the classpath and add the `soot.Main --dava` part
automatically. Mine looks like this (all on one line):

    java -Xmx128M -cp .:/usr/java/jre/lib/rt.jar:
    /home/44/emmerik/soot-1.2.4/soot/classes/:
    /home/44/emmerik/soot-1.2.4/jasmin/classes:. soot.Main --dava $@

[]{#About_Dava} About Dava
--------------------------

As you can read in the various papers, in particular [Decompiling Java
Bytecode: Problems, Traps and
Pitfalls](http://www.sable.mcgill.ca/publications/papers/#cc2002-2), not
all Java decompilers are created equal. In particular, 4 of the most
popular ones completely failed when faced with optimised bytecode (you
can use soot as an optimiser, as well as its many other uses). Also,
Dava is tested on bytecode generated by relatively exotic languages,
such as Haskell, Eiffel, ML, Ada, and even Fortran. A good Java
decompiler should be able to produce correct, compilable code for any
verifyable bytecode, and they claim that Dava comes close to this
(certainly a lot closer than the other decompilers they tested,
including two commercial decompilers). However, the more recent open
source decompiler [JODE](DecompilationJodeTest){.twikiLink} seems to
fare better than the decompilers they tested, and a little better than
Dava as well.

The main problems that good decompilers solve are

-   Finding the types of local variables (including references to
    objects),
-   creating \"stack variables\" as needed, and
-   sorting out the control flow issues associated with gotos, breaks,
    and the like, so that these can be implemented in pure Java.

There are other problems, associated with exceptions, class literals,
package and class resolution, etc, which they have solved along the way.

------------------------------------------------------------------------

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
