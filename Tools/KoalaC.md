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
    Page](http://www.program-transformation.org/edit/Tools/KoalaC?t=1536825806)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/KoalaC)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/KoalaC)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/KoalaC?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/KoalaC?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tools/KoalaC?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/KoalaC?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/KoalaC?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/KoalaC)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/KoalaC?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tools/KoalaC?template=oopsmore&param1=1.2&param2=1.2)
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
Koala C {#koala-c .twikiTopicTitle}
=======

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

The tool `koala-c` translates the bindings defined in a Koala
composition to C. The program takes as input a Koala composition and
produces as output a set of .c/.h files, and a Makefile. This tool
corresponds to the combination of `koala` / `koalamaker` tools of the
original Philips Koala compiler.

The generated files will be stored in the directory specified with the
\'-d\' command line switch (defaults to current working directory).

       koala-c -I <directory with Koala components> \
               -i <top-level component> \
               -d <output-dir>

The C-source source files can now be compiled into an executable program
`a.out` by running `make` in the output directory:

       cd <output-dir>
       make
       ./a.out

All non-generated compilation units (i.e., all source files
corresponding to Koala modules), should be stored in the same location
as the corresponding component definition file. This is how `koala-c`
knows where source files can be located and how source files are
referenced in generated Makefiles. This is based on Philips\' Koala
implementation.

The name of the output program (i.e., the result of running `make`), can
be specified with the \'-p\' switch:

       koala-c -I <directory with Koala components> \
               -i <top-level component> \
               -d <output-dir> \
               -p hello-world

The name of the generated Makefile can be specified with the \'-m-\'
switch:

       koala-c -I <directory with Koala components> \
               -i <top-level component> \
               -d <output-dir> \
               -p hello-world  \
               -m Mymake

Compiling and running the resulting program can now be performed as
follows:

       cd <output-dir>
       make -f Mymake
       ./hello-world

The generated Makefile contains two additional targets. These are:

-   *clean* to remove files generated during the invocation of =make
-   *allclean* to also remove the files generated by `koala-c`

The directory `demos/koala-c` in the source distribution of
[KoalaCompiler](KoalaCompiler){.twikiLink} (see
[HowToObtainKoalaCompiler](http://www.program-transformation.org/Tools/HowToObtainKoalaCompiler){.twikiLink})
contains examples of `koala-c` \--
[MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 22 Dec 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.KoalaC moved from Tools.HowToGenerateCCode on 22 Dec 2004 - 12:21
by [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tools/KoalaC?newweb=Tools&newtopic=HowToGenerateCCode&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
