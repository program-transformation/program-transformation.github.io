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
Function Type Specification {#function-type-specification .topic-header}
===========================

::: {.topic-text}
To help the Typechecker we have a language for specifying type of
builtin variables and functions. This is needed because we cannot derive
types for these variables and functions.

    definitions
      constants 
        do_fortran_indexing :=  int
        e       := float
        eps     := float
        pi      := float
        ...
      variables
        warn_fortran_indexing := int
        warn_num_to_str := int
        ...
      functions
        ...
        date    :: -> string 
        time    :: -> float
        ctime   :: float -> string
        isieee  :: -> int
        fnmatch :: string, matrix(char) -> matrix(int)
        fnmatch :: string, string -> int
        ...
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
[printable](http://www.program-transformation.org/view/Octave/FunctionTypeSpecification?skin=print)
\|
[refresh](http://www.program-transformation.org/fresh/Octave/FunctionTypeSpecification)
\|
[edit](http://www.program-transformation.org/edit/Octave/FunctionTypeSpecification?t=1536826799)
\|
[history](http://www.program-transformation.org/rdiff/Octave/FunctionTypeSpecification)
\| [more
actions](http://www.program-transformation.org/oops/Octave/FunctionTypeSpecification?template=oopsmore&param1=1.2&param2=1.2)

</div>

</div>
:::
:::
