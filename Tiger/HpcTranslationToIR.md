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
    Page](http://www.program-transformation.org/edit/Tiger/HpcTranslationToIR?t=1536826699)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/HpcTranslationToIR)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/HpcTranslationToIR)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/HpcTranslationToIR?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/HpcTranslationToIR?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tiger/HpcTranslationToIR?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/HpcTranslationToIR)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/HpcTranslationToIR?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tiger/HpcTranslationToIR?template=oopsmore&param1=1.1&param2=1.1)
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
Hpc Translation To IR {#hpc-translation-to-ir .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

**Translation to Intermediate Representation**

This is the second set of [HpcExercises](HpcExercises){.twikiLink}.
These will teach you to write a more complex transformation (translation
to IR) in Stratego.

1.  Download the new version (0.3) of [WebHome](WebHome){.twikiLink} and
    install it. (There is a distribution with precompiled binaries for
    Suns.)

<!-- -->

1.  Finish the desugaring component (sig/Tiger-Desugar.r) and test it.
    (See
    [ApplyingTisComponents[^?^](http://www.program-transformation.org/edit/Tiger/ApplyingTisComponents?topicparent=Tiger.HpcTranslationToIR)]{.twikiNewLink
    style="background : #FFFFCE;"} for instructions on how to use the
    components of the [TigerCompiler](TigerCompiler){.twikiLink}.)

<!-- -->

1.  Use the Tiger-Abstract-Syntax-Format checker to check that the
    output of your desugarer conforms to the format by making
    prog.tas.check.

<!-- -->

1.  Use the typechecker to typecheck some Tiger programs (by calling
    gmake prog.tc.tas).

<!-- -->

1.  Extend the translation of expressions in modules
    Translate-Expressions.r and Translate-Statements.r to cover all
    constructs of the language. This entails writing a rule
    [TrExp[^?^](http://www.program-transformation.org/edit/Tiger/TrExp?topicparent=Tiger.HpcTranslationToIR)]{.twikiNewLink
    style="background : #FFFFCE;"} for each expression construct in the
    language. Note that the translation of declarations is covered in
    Translate-Declarations.r.

------------------------------------------------------------------------

**Notes**

Note that the typechecker annotates the constructors for array
subscription (Subscript), record field selection
([FieldVar[^?^](http://www.program-transformation.org/edit/Tiger/FieldVar?topicparent=Tiger.HpcTranslationToIR)]{.twikiNewLink
style="background : #FFFFCE;"}), array creation (Array) and record
creation (Record) with the types of the data structures. This is
necessary for the translator to know the size of these data structures
(in particular offsets into records).

When you first define the translation don\'t be concerned with
optimizing chains of jumps. Just evaluate an expression to its boolean
value and then compare to 0 to make a jump as in

CJUMP(NE, e, CONST(0), t, f)

Also don\'t be concerned about putting arguments of function calls in
parameters. All formal parameters and local variables are stored in the
stack frame.

The MEM operator of the IR works both as fetch *and* store. (See section
7.2: Structured L-values.)

Sometimes it is useful to mix IR and Tiger abstract syntax, for example
when translating the For statement.

When you got the basic translation to work try to introduce short
circuit evaluation of Boolean expressiosn by using the Cx constructor.
If some (sub-)expression \'e\' should be interpreted as a Boolean
expression, wrap a \'Cx(e, t, f)\' around it to indicate that there
should be a jump to \'t\' when the expression evaluates to true and to
\'f\' otherwise. This pseudo construct can then be optimized if
possible. The default case should just do what you were doing al along:

[TrCx[^?^](http://www.program-transformation.org/edit/Tiger/TrCx?topicparent=Tiger.HpcTranslationToIR)]{.twikiNewLink
style="background : #FFFFCE;"} : Cx(e, t, f) -\> CJUMP(NE, e, CONST(0),
t, f)

The next exercise is to do escaping variables analysis to determine
which variables can be stored in registers.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
