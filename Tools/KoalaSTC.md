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
    Page](http://www.program-transformation.org/edit/Tools/KoalaSTC?t=1536825806)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/KoalaSTC)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/KoalaSTC)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/KoalaSTC?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/KoalaSTC?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tools/KoalaSTC?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/KoalaSTC?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/KoalaSTC?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/KoalaSTC)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/KoalaSTC?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tools/KoalaSTC?template=oopsmore&param1=1.2&param2=1.2)
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
Koala STC {#koala-stc .twikiTopicTitle}
=========

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

The tool koala-stc translates a Koala composition to a composite source
tree. This process is called [Source Tree
Composition](http://www.cs.uu.nl/groups/ST/Merijn/PaperSourceTreeComposition).

The basic idea is that for `koala-stc` Koala modules do not correspond
to C source files but to source distributions (e.g., gzipped tar files).
A composition consists of a source tree containing all unpacked source
distributions, together with an integrated configuration and build
process. This composite source tree can be handled as a unit, such that
building and configuring can be done for the source tree as a whole,
rather than for each subcomponent individually.

More on this topic can be found here:

-   de Jonge, M. (2004). [Multi-level Component
    Composition](http://www.cs.uu.nl/groups/ST/Merijn/PaperMultiLevelComponentComposition).
    Bosch, Jan, Ed. 2nd Groningen Workshop on Software Variability
    Modeling (SVM\'04).
-   de Jonge, M. (2004). [Decoupling Source Trees into Build-Level
    Components](http://www.cs.uu.nl/groups/ST/Merijn/PaperDecouplingSourceTreesIntoBuildLevelComponents).
    Bosch, J. and C. Krueger, Ed. Proceedings: Eighth International
    Conference on Software Reuse. 215\--231. Springer-Verlag.
-   de Jonge, M. (2002). [Source Tree
    Composition](http://www.cs.uu.nl/groups/ST/Merijn/PaperSourceTreeComposition).
    Gacek, Cristina, Ed. Proceedings: Seventh International Conference
    on Software Reuse. 17\--32. Springer-Verlag.

The `koala-stc` tool takes as input a Koala composition and produces as
output a source tree in which all modules are unpacked, and an GNU build
environment that includes a set of Automake Makefiles and an Autoconf
configuration script. The generated files will be stored in the
directory specified with the \'-d\' command line switch (defaults to
current working directory).

    koala-stc -I <directory with Koala components> \
               -i <top-level component> \
               -d <output-dir>

The resulting source tree can now be compiled in the following steps:

       cd <output-dir>
       autoreconf -if
       configure --prefix <installation prefix> -C
       make install

The tool `koala-stc` makes an assumption about variability interfaces.
An interface definition is assumed to be a variability interfaces iff
the interface definition does *not* contain function prototypes. Thus,
an interface definition is a variability interface if it consists solely
of parameters, constants, or defined functions.

Parameters of variability interfaces that are not bound (and become
constants) during the normalization process, become paramters of the
composite bundle. This means that they propagate to top-level Autoconf
configuration switches. These parameters can then be bound at
configuration time. E.g., a parameter `debug` can be bound s follows:

       configure --with-debug=<some value>

The directory `demos/koala-stc` in the source distribution of
[KoalaCompiler](KoalaCompiler){.twikiLink} (see
[HowToObtainKoalaCompiler](http://www.program-transformation.org/Tools/HowToObtainKoalaCompiler){.twikiLink})
contains examples of `koala-stc`

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 22 Dec 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.KoalaSTC moved from Tools.HowToGenerateSoftwareBundles on 22 Dec
2004 - 12:22 by [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink}* -
[put it
back](http://www.program-transformation.org/rename/Tools/KoalaSTC?newweb=Tools&newtopic=HowToGenerateSoftwareBundles&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
