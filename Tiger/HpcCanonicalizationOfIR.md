::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![Stratego
logo](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)

------------------------------------------------------------------------

***Tiger in Stratego***

------------------------------------------------------------------------

**[WebHome](WebHome){.twikiLink}**\
[Tiger Compiler](TigerCompiler){.twikiLink}\
[Architecture](CompilerArchitecture){.twikiLink}\
[Packages](CompilerPackages){.twikiLink}\
[Components](CompilerComponent){.twikiLink}\
[Glossary](WebGlossary){.twikiLink}

[Download](DownloadAndInstallation){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Tiger/HpcCanonicalizationOfIR?t=1536826697)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/HpcCanonicalizationOfIR)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/HpcCanonicalizationOfIR)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/HpcCanonicalizationOfIR?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/HpcCanonicalizationOfIR?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tiger/HpcCanonicalizationOfIR?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/HpcCanonicalizationOfIR)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/HpcCanonicalizationOfIR?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tiger/HpcCanonicalizationOfIR?template=oopsmore&param1=1.1&param2=1.1)
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
Hpc Canonicalization Of IR {#hpc-canonicalization-of-ir .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

**Canonicalization of IR Programs**

This is the third set of [HpcExercises](HpcExercises){.twikiLink}. The
final goal of this set of exercises is the definition of a
transformation that brings IR expressions in a canonical form.

1.  Setup module IR-Canonicalize.r in directory trans/ with as start an
    identity transformation. Extend the Makefile.am with appropriate
    rules for compiling this new component. Compile, install and test by
    transforming some programs in xmpl/ using the target %.cir (for
    canonicalized ir).

<!-- -->

1.  Define a
    [RecursivePattern[^?^](http://www.program-transformation.org/edit/Tiger/RecursivePattern?topicparent=Tiger.HpcCanonicalizationOfIR)]{.twikiNewLink
    style="background : #FFFFCE;"} that describes IR expressions in
    canonical form in module sig/CIR-Format.r. Compile it and define an
    appropriate target in xmpl/make-rules to check %.cir files.

<!-- -->

1.  Extend IR-Canonicalize with transformation rules for linearizing an
    IR expression.

<!-- -->

1.  Define a strategy to apply the linearization rules.

<!-- -->

1.  Define a strategy for extracting basic blocks.

<!-- -->

1.  Define a strategy for covering the program with traces.

------------------------------------------------------------------------

**Notes**

You can pretty-print the IR tree with the program PP-IR (target
%.ir.txt), which can also be used for canonicalized IR trees (target
%.cir.txt).\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
