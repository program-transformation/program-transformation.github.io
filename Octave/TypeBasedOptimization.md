::: {#content}
::: {#header}
![Stratego
Logo](http://stratego.insanity.nl/StrategoLogoTextlessWhite-100px.png)

<div>

[Octave](WebHome){.twikiLink} {#web-title}
=============================

Octave-Compiler.org

</div>
:::

::: {#main}
::: {#main2}
Type Based Optimization {#type-based-optimization .topic-header}
=======================

::: {.topic-text}
Typed based optimizations are optimizations that can be performed based
on information from the type inferencer, e.g.

### []{#Function_call_evaluation_using_t} Function call evaluation using type information

    a = [ 1 2 ; 3 4 ]
    b = ismatrix(a)

The type inferencer can determine that a is of type matrix. Therefore,
we can rewrite this to,

    a = [ 1 2 ; 3 4 ]
    b = true
:::
:::
:::

::: {#sidebar}
::: {.box}
::: {.box2}
[Home](WebHome){.twikiLink} {#home .sidebar-title}
---------------------------

-   [About](AboutOctaveCompiler){.twikiLink}
-   [News](OctaveCompilerNews){.twikiLink}
-   [Documentation](OctaveCompilerDocumentation){.twikiLink}
-   [Bugs](https://catamaran.labs.cs.uu.nl/jira/browse/OCT)
-   [Download](OctaveCompilerDownload){.twikiLink}

\
\
:::
:::
:::

::: {#footer}
<div>

<div>

------------------------------------------------------------------------

[search](WebSearch){.twikiLink} \| [index](WebIndex){.twikiLink} \|
[recent changes](WebChanges){.twikiLink} \|
[statistics](WebStatistics){.twikiLink}    
[printable](http://www.program-transformation.org/view/Octave/TypeBasedOptimization?skin=print)
\|
[refresh](http://www.program-transformation.org/fresh/Octave/TypeBasedOptimization)
\|
[edit](http://www.program-transformation.org/edit/Octave/TypeBasedOptimization?t=1536826801)
\|
[history](http://www.program-transformation.org/rdiff/Octave/TypeBasedOptimization)
\| [more
actions](http://www.program-transformation.org/oops/Octave/TypeBasedOptimization?template=oopsmore&param1=1.2&param2=1.2)

</div>

</div>
:::
:::
