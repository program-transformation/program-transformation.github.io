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
    Page](http://www.program-transformation.org/edit/Tools/HowToInstallKoalaCompiler?t=1536825805)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/HowToInstallKoalaCompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/HowToInstallKoalaCompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/HowToInstallKoalaCompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/HowToInstallKoalaCompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tools/HowToInstallKoalaCompiler?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/HowToInstallKoalaCompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/HowToInstallKoalaCompiler?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tools/HowToInstallKoalaCompiler?template=oopsmore&param1=1.1&param2=1.1)
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
How To Install Koala Compiler {#how-to-install-koala-compiler .twikiTopicTitle}
=============================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

Assuming that all required packages are installed (see
[HowToObtainKoalaCompiler](http://www.program-transformation.org/Tools/HowToObtainKoalaCompiler){.twikiLink}),
the source distribution of [KoalaCompiler](KoalaCompiler){.twikiLink}
can be installed in the following steps:

**Unpacking**

        tar zxvf koala-compiler-0.1.tar.gz
        cd koala-compiler-0.1

**Configuration**

If all required packages are installed in the same location, proceed as
follows:

        ./configure --with-xt=<location of strategoxt> \
                    --prefix=<installation prefix>

Otherwise, specify all locations separately:

        ./configure --with-strategoxt=<location of strategoxt> \
                    --with-sdf-tools=<location of sdf-tools> \
                    --with-aterm=<location of aterms> \
                    --prefix=<installation prefix>

**Compilation/Installation**

        make
        make check
        make install

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 22 Dec 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
