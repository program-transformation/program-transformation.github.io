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
    Page](http://www.program-transformation.org/edit/Tools/HowToKoalaCompilerFramework?t=1536825807)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/HowToKoalaCompilerFramework)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/HowToKoalaCompilerFramework)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/HowToKoalaCompilerFramework?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/HowToKoalaCompilerFramework?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tools/HowToKoalaCompilerFramework?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tools/HowToKoalaCompilerFramework?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tools/HowToKoalaCompilerFramework?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/HowToKoalaCompilerFramework)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/HowToKoalaCompilerFramework?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tools/HowToKoalaCompilerFramework?template=oopsmore&param1=1.2&param2=1.2)
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
How To Koala Compiler Framework {#how-to-koala-compiler-framework .twikiTopicTitle}
===============================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

The [KoalaCompiler](KoalaCompiler){.twikiLink} is developed as a
component-based system using
[StrategoXT](../Stratego/StrategoXT){.twikiLink}:

-   The system is implemented as a set of program transformation tools.
-   Different pieces are implemented as separate tool components
    (executable programs).
-   Each tool component is implemented in the
    [Stratego](../Stratego/WebHome){.twikiLink} programming language.
-   Tool components are connected through the [ATerm](ATerm){.twikiLink}
    exchange format.
-   All tool components are *syntax-driven*:
    -   Syntax definitions are defined in
        [SDF](../Sdf/WebHome){.twikiLink}.
    -   From a syntax definition a pretty-printer, abstract syntax
        definition, and libraries are generated.
    -   All transformations operate on abstract syntax trees .
-   Compositions of tool components are created with the Transformation
    Tool Composition framework [XTC](../Stratego/XTC){.twikiLink}.

The Koala compilation process consists of three phases:

1.  *Parsing*. During this phase a top-level Koala component definition
    is located and parsed. Subsequently, all contained elements are
    recursively located and parsed. The result of parsing is a single
    abstract syntax tree (AST) that contains exactly *all* elements of
    the Koala composition.
2.  *Normalization*. In this phase the AST from phase 1 is reduced to
    normal form. This involves several simplification steps, constant
    propagation, function inlining, reachability analysis, switch
    reduction, transitive wiring, and component pruning. The result is
    again an AST, that may serve for analysis or realization.
3.  *Realization*. In this phase the normalized Koala composition is
    realized for some target. Traditionally, realization is only
    performed for the C programming language (which we support through
    [KoalaC](KoalaC){.twikiLink}). Other realizations are:
    pretty-printing (see [KoalaText](KoalaText){.twikiLink}) or
    vizualization (see [KoalaDot](KoalaDot){.twikiLink}). Additional
    realization components can simply be connected to the compiler
    framework (e.g., see [KoalaSTC](KoalaSTC){.twikiLink}).

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 22 Dec 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
