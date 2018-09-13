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
    Page](http://www.program-transformation.org/edit/Tools/KoalaToolsCompiler?t=1536826792)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/KoalaToolsCompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/KoalaToolsCompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/KoalaToolsCompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/KoalaToolsCompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Tools/KoalaToolsCompiler?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Tools/KoalaToolsCompiler?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Tools/KoalaToolsCompiler?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Tools/KoalaToolsCompiler?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Tools/KoalaToolsCompiler?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tools/KoalaToolsCompiler?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/KoalaToolsCompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/KoalaToolsCompiler?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Tools/KoalaToolsCompiler?template=oopsmore&param1=1.6&param2=1.6)
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
Koala Tools Compiler {#koala-tools-compiler .twikiTopicTitle}
====================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

**Description**

The Koala compiler toolkit forms a generic framework for component
composition. The framework works as follows:

1.  Components and compositions are expressed in the Koala component
    definition language
2.  The tool `koala-compiler` is used to synthesize an abstract
    composition. The combination of `koala-pack`, `implode-asfix`,
    `koala-wire`, and `koala-compiler` is called the *first-phase*
    composition.
3.  Composition type-specific tools then perform a specific composition
    of components. The combination of tools for a particular composition
    type is called the *second-phase* composition.

**First phase composition**

Given the component `koala-bundle` as showed in
[PackKoala](PackKoala){.twikiLink}, the first phase composition can be
performed with the folllowing tool chain:

       pack-koala -I ./koala-pb -i koala-tools-bundle \
       | implode-asfix \
       | koala-wire \
       | koala-compiler

This produces an
[AbstractCompositionDefinition](AbstractCompositionDefinition){.twikiLink},
describing the ingredients of the composition, its structure, as well as
relations between modules and components in the composition.

**Second phase composition**

The second phase composition depends on the particular
*composition-type*. Below we explain how [Source Tree
Composition](http://www.cs.uu.nl/groups/ST/Merijn/PaperSourceTreeComposition)
can be performed as second phase composition.

[Source Tree
Composition](http://www.cs.uu.nl/groups/ST/Merijn/PaperSourceTreeComposition)
consists of

1.  Determining the build order of the components in the composition.
    This is performed by the tools `koala-tred` and `koala-build-order`.
    The first tool replaces transitive references (m1-\>C1-\>C2-\>m2) by
    direct references (m1-\>m2). The second tool reorders modules such
    that if a module is referenced, it occurs before the referencing
    module.
2.  Obtaining and integrating source trees. This is achieved with the
    tool `koala-tree-composer`. This tool produces a shell script that,
    when executed creates a directory hierarchy in which it unpacks the
    source trees of all components.
3.  Synthesizing a build and configuration process. This is achieved
    with the tool `koala-build-composer`. This tool creates in the
    constructed directory hierarchy a top-level Autoconf `configure`
    scripts as well as Automake `Makefiles`.

The second phase composition therefore consists of the following tool
invocations:

       koala-tred \
       | koala-buildorder \
       | koala-tree-composer -o <prefix> > composer.sh
       sh ./composer.sh

       koala-tred \
       | koala-buildorder \
       | koala-build-composer -o <prefix>

The location where the source tree is produced is denoted with
`<prefix>`.

You can now compile the generated composition:

       cd <prefix>
       sh ./bootstrap.sh
       ./configure
       make install

We started developing some other second phase composition tools,
including a petri-net composer and a graph composer.

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 17 Feb 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.KoalaToolsCompiler moved from Tools.KoalaCompiler on 22 Dec 2004
- 08:48 by [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tools/KoalaToolsCompiler?newweb=Tools&newtopic=KoalaCompiler&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
