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
    Page](http://www.program-transformation.org/edit/Tools/AbstractCompositionDefinition?t=1536826785)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/AbstractCompositionDefinition)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/AbstractCompositionDefinition)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/AbstractCompositionDefinition?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/AbstractCompositionDefinition?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tools/AbstractCompositionDefinition?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/AbstractCompositionDefinition)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/AbstractCompositionDefinition?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tools/AbstractCompositionDefinition?template=oopsmore&param1=1.1&param2=1.1)
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
Abstract Composition Definition {#abstract-composition-definition .twikiTopicTitle}
===============================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Description**

An abstract composition definition is a definition of a composition that
is independent of the type of components. It describes the components in
the composition, the relation between components, the structure of the
composition, and it contains URLs to locations where different component
types are stored.

Types of components can be *build-level* components, *source files*,
petri nets, etc.

**Example**

Below is an example of an abstract composition definition for the
composition described at [KoalaCompiler](KoalaCompiler){.twikiLink}.

------------------------------------------------------------------------

    component koala-bundle (BUNDLE)
    {
       path = koala-bundle
    }
    {
    }

    component asfix-tools (ASFIX-TOOLS)
    {
       path = koala-bundle/asfix-tools
       url = file:///home/mdejonge/pkgs
    }
    {
       IbinASFIX-TOOLS : asfix-tools -> koala-bundle/asfix-tools/asfix-tools-1_0
       IlibATERM : aterm -> koala-bundle/aterm
       IlibXTC : xtc -> koala-bundle/stratego
       IlibSRTS : srts -> koala-bundle/stratego
    }

    module asfix-tools-1_0
    {
       path = koala-bundle/asfix-tools/asfix-tools-1_0
       url = file:///home/mdejonge/pkgs
    }
    {
       IlibATERM : aterm -> koala-bundle/asfix-tools
       IlibXTC : xtc -> koala-bundle/asfix-tools
       IlibSRTS : srts -> koala-bundle/asfix-tools
    }

    component aterm (ATerm)
    {
       path = koala-bundle/aterm
       url = file:///home/mdejonge/pkgs
    }
    {
       IlibATERM : aterm -> koala-bundle/aterm/aterm-1_0
    }

    module aterm-1_0
    {
       path = koala-bundle/aterm/aterm-1_0
       url = file:///home/mdejonge/pkgs
    }
    {
    }

    component gpp (GPP)
    {
       path = koala-bundle/gpp
       url = file:///home/mdejonge/pkgs
    }
    {
       IbinGPP : gpp -> koala-bundle/gpp/gpp-1_0
       IlibATERM : aterm -> koala-bundle/aterm
       IbinASFIX-TOOLS : asfix-tools -> koala-bundle/asfix-tools
       IbinSGLR : sglr -> koala-bundle/sglr
       IbinGRAPH-TOOLS : graph-tools -> koala-bundle/graph-tools
       IlibSRTS : srts -> koala-bundle/stratego
       IlibXTC : xtc -> koala-bundle/stratego
    }

    module gpp-1_0
    {
       path = koala-bundle/gpp/gpp-1_0
       url = file:///home/mdejonge/pkgs
    }
    {
       IlibATERM : aterm -> koala-bundle/gpp
       IbinASFIX-TOOLS : asfix-tools -> koala-bundle/gpp
       IbinSGLR : sglr -> koala-bundle/gpp
       IbinGRAPH-TOOLS : graph-tools -> koala-bundle/gpp
       IlibSRTS : srts -> koala-bundle/gpp
       IlibXTC : xtc -> koala-bundle/gpp
    }

    component graph-tools (GRAPH-TOOLS)
    {
       path = koala-bundle/graph-tools
       url = file:///home/mdejonge/pkgs
    }
    {
       IbinGRAPH-TOOLS : graph-tools -> koala-bundle/graph-tools/graph-tools-1_0
       IlibATERM : aterm -> koala-bundle/aterm
       IlibSRTS : srts -> koala-bundle/stratego
       IlibXTC : xtc -> koala-bundle/stratego
    }

    module graph-tools-1_0
    {
       path = koala-bundle/graph-tools/graph-tools-1_0
       url = file:///home/mdejonge/pkgs
    }
    {
       IlibATERM : aterm -> koala-bundle/graph-tools
       IlibXTC : xtc -> koala-bundle/graph-tools
       IlibSRTS : srts -> koala-bundle/graph-tools
    }

    component sglr (mySGLR)
    {
       path = koala-bundle/sglr
       url = file:///home/mdejonge/pkgs
    }
    {
       IbinSGLR : sglr -> koala-bundle/sglr/sglr-1_0
       IlibPT-SUPPORT : pt-support -> koala-bundle/sglr/pt-support-1_0
       IlibTOOLBUS-LIB : toolbus-lib -> koala-bundle/sglr/toolbus-lib-1_0
       IlibATERM : aterm -> koala-bundle/aterm
    }

    module sglr-1_0
    {
       path = koala-bundle/sglr/sglr-1_0
       url = file:///home/mdejonge/pkgs
    }
    {
       IlibPT-SUPPORT : pt-support -> koala-bundle/sglr
       IlibTOOLBUS-LIB : toolbus-lib -> koala-bundle/sglr
       IlibATERM : aterm -> koala-bundle/sglr
    }

    module pt-support-1_0
    {
       path = koala-bundle/sglr/pt-support-1_0
       url = file:///home/mdejonge/pkgs
    }
    {
       IlibTOOLBUS-LIB : toolbus-lib -> koala-bundle/sglr
       IlibATERM : aterm -> koala-bundle/sglr
    }

    module toolbus-lib-1_0
    {
       path = koala-bundle/sglr/toolbus-lib-1_0
       url = file:///home/mdejonge/pkgs
    }
    {
       IlibATERM : aterm -> koala-bundle/sglr
    }

    component stratego (Stratego)
    {
       path = koala-bundle/stratego
    }
    {
       IlibSRTS : srts -> koala-bundle/stratego/my_srts
       IlibXTC : xtc -> koala-bundle/stratego/my_xtc
       IlibATERM : aterm -> koala-bundle/aterm
    }

    component my_xtc (XTC)
    {
       path = koala-bundle/stratego/my_xtc
       url = file:///home/mdejonge/pkgs
    }
    {
       IlibXTC : xtc -> koala-bundle/stratego/my_xtc/xtc-1_0
       IlibATERM : aterm -> koala-bundle/stratego
       IlibSRTS : srts -> koala-bundle/stratego
    }

    module xtc-1_0
    {
       path = koala-bundle/stratego/my_xtc/xtc-1_0
       url = file:///home/mdejonge/pkgs
    }
    {
       IlibATERM : aterm -> koala-bundle/stratego/my_xtc
       IlibSRTS : srts -> koala-bundle/stratego/my_xtc
    }

    component my_srts (SRTS)
    {
       path = koala-bundle/stratego/my_srts
       url = file:///home/mdejonge/pkgs
    }
    {
       IlibSRTS : srts -> koala-bundle/stratego/my_srts/srts-1_0
       IlibATERM : aterm -> koala-bundle/stratego
    }

    module srts-1_0
    {
       path = koala-bundle/stratego/my_srts/srts-1_0
       url = file:///home/mdejonge/pkgs
    }
    {
       IlibATERM : aterm -> koala-bundle/stratego/my_srts
    }

    component koala (KOALA)
    {
       path = koala-bundle/koala
       url = file:///home/mdejonge/pkgs
    }
    {
       IbinKOALA : koala -> koala-bundle/koala/koala-1_0
       IbinGPP : gpp -> koala-bundle/gpp
       IbinSGLR : sglr -> koala-bundle/sglr
       IlibSRTS : srts -> koala-bundle/stratego
       IlibXTC : xtc -> koala-bundle/stratego
       IlibATERM : aterm -> koala-bundle/aterm
    }

    module koala-1_0
    {
       path = koala-bundle/koala/koala-1_0
       url = file:///home/mdejonge/pkgs
    }
    {
       IbinGPP : gpp -> koala-bundle/koala
       IbinSGLR : sglr -> koala-bundle/koala
       IlibSRTS : srts -> koala-bundle/koala
       IlibXTC : xtc -> koala-bundle/koala
       IlibATERM : aterm -> koala-bundle/koala
    }

------------------------------------------------------------------------

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 18 Feb 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
