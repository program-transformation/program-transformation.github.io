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
Octave Optimizer {#octave-optimizer .topic-header}
================

::: {.topic-text}
### []{#Contents} Contents

The [Octave Optimizer](OctaveOptimizer){.twikiLink} implements several
optimization on Octave code. The optimizations are implemented as
source-to-source transformation, similar to the optimization described
in the following paper,

-   K. Olmos and E. Visser. [Strategies for Source-to-Source Constant
    Propagation](http://www.elsevier.nl/locate/entcs/volume70.html).
    In B. Gramlich and S. Lucas, editors, *Workshop on Reduction
    Strategies (WRS\'02)*, volume 70 of *Electronic Notes in Theoretical
    Computer Science*, page 20, Copenhagen, Denmark, July 2002. Elsevier
    Science Publishers.
    ([entcs](http://www.elsevier.nl/locate/entcs/volume70.html),[pdf](http://www.cs.uu.nl/people/visser/ftp/OV02.pdf),[bib](http://www.cs.uu.nl/%7Evisser/visser/OV02.bib)).

The latest sources of the Octave Optimizer can be found at

-   <https://svn.cs.uu.nl:12443/repos/octave/octavec/trunk/octave-opt/>

### []{#Optimizations} Optimizations

**Constant Folding**

**Constant Propagation**

**Dead Code Elimination**

### []{#Loop_optimizations} Loop optimizations

Besides the previously mentioned optimizations, the Stratego Octave
Compiler has some experimental support for loop optimizations. [Remko
van Beusekom](../Main/RemkoVanBeusekom){.twikiLink} is implementing
these optimization as part of his Master thesis project. The loop
optimizations are a variant to the optimizations described in the
following book,

-   Ken Kennedy and John R. Allen. **Optimizing compilers for modern
    architectures: a dependence-based approach**. 2002. Morgan Kaufmann
    Publishers Inc.
    ([bib](http://portal.acm.org/popBibTex.cfm?id=502981&ids=502981&types=nondiv_book&reqtype=nondiv_book&coll=GUIDE&dl=ACM&CFID=31545933&CFTOKEN=63036509)).

**Loop vectorization**
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
[printable](http://www.program-transformation.org/view/Octave/OctaveOptimizer?skin=print)
\|
[refresh](http://www.program-transformation.org/fresh/Octave/OctaveOptimizer)
\|
[edit](http://www.program-transformation.org/edit/Octave/OctaveOptimizer?t=1536826797)
\|
[history](http://www.program-transformation.org/rdiff/Octave/OctaveOptimizer)
\| [more
actions](http://www.program-transformation.org/oops/Octave/OctaveOptimizer?template=oopsmore&param1=1.5&param2=1.5)

</div>

</div>
:::
:::
