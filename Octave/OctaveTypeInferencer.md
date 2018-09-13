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
Octave Type Inferencer {#octave-type-inferencer .topic-header}
======================

::: {.topic-text}
The [Octave Type Inferencer](OctaveTypeInferencer){.twikiLink} is a
typechecker for the Octave language. Although the implementation has
changed significantly, currently the ideas are only expressed in the
following paper,

-   K. Olmos and E. Visser. [Turning Dynamic Typing into Static Typing
    by Program
    Specialization](http://csdl.computer.org/comp/proceedings/scam/2003/2005/00/20050141abs.htm).
    In D. Binkley and P. Tonella, editors, *Third IEEE International
    Workshop on Source Code Analysis and Manipulation (SCAM\'03)*, pages
    141\--150, Amsterdam, The Netherlands, September 2003. IEEE Computer
    Society Press.
    ([ieee](http://csdl.computer.org/comp/proceedings/scam/2003/2005/00/20050141abs.htm),
    [info](http://www.stratego-language.org/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization),
    [tr](http://www.cs.uu.nl/research/techreps/UU-CS-2003-049.html),
    [pdf](http://archive.cs.uu.nl/pub/RUU/CS/techreps/CS-2003/2003-049.pdf),
    [bib](http://www.cs.uu.nl/~visser/visser/OV03.bib)).

### []{#Contents} Contents

The latest sources of the Octave Typechecker can be found at

-   <https://svn.cs.uu.nl:12443/repos/octave/octavec/trunk/octave-tc/>

The Octave Typechecker uses a list of manually specified types of
built-in, mapping or dynamically loaded function (see also [Function
Type Specification](FunctionTypeSpecification){.twikiLink}).

### []{#Octave_Types} Octave Types

-   Base types
    -   Integer
    -   Float
    -   Boolean
    -   Function handle
    -   String
-   Composite types
    -   Array of \<base-type\>
    -   Cell array
    -   Struct
-   Universal type

### []{#TODO} TODO

-   Separate processes
    -   [Type-inferencing[^?^](http://www.program-transformation.org/edit/Octave/OctaveTypeInferencing?topicparent=Octave.OctaveTypeInferencer)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [Type based optimization](TypeBasedOptimization){.twikiLink}
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
[printable](http://www.program-transformation.org/view/Octave/OctaveTypeInferencer?skin=print)
\|
[refresh](http://www.program-transformation.org/fresh/Octave/OctaveTypeInferencer)
\|
[edit](http://www.program-transformation.org/edit/Octave/OctaveTypeInferencer?t=1536826798)
\|
[history](http://www.program-transformation.org/rdiff/Octave/OctaveTypeInferencer)
\| [more
actions](http://www.program-transformation.org/oops/Octave/OctaveTypeInferencer?template=oopsmore&param1=1.6&param2=1.6)

</div>

</div>
:::
:::
