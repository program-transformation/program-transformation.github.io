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
    Page](http://www.program-transformation.org/edit/Tiger/TranslateExpressionsToIntermediateRepresentation?t=1536826661)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/TranslateExpressionsToIntermediateRepresentation)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/TranslateExpressionsToIntermediateRepresentation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/TranslateExpressionsToIntermediateRepresentation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/TranslateExpressionsToIntermediateRepresentation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Tiger/TranslateExpressionsToIntermediateRepresentation?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Tiger/TranslateExpressionsToIntermediateRepresentation?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Tiger/TranslateExpressionsToIntermediateRepresentation?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Tiger/TranslateExpressionsToIntermediateRepresentation?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Tiger/TranslateExpressionsToIntermediateRepresentation?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tiger/TranslateExpressionsToIntermediateRepresentation?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/TranslateExpressionsToIntermediateRepresentation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/TranslateExpressionsToIntermediateRepresentation?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Tiger/TranslateExpressionsToIntermediateRepresentation?template=oopsmore&param1=1.6&param2=1.6)
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
Translate Expressions To Intermediate Representation {#translate-expressions-to-intermediate-representation .twikiTopicTitle}
====================================================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

Implement translation of
[TigerAbstractSyntax](http://www.program-transformation.org/Tiger/TigerAbstractSyntax){.twikiLink}
expressions to
[IntermediateRepresentation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}
code in module [TAS2IR](TAS2IR){.twikiLink} in the
[TigerTrans](TigerTrans){.twikiLink} package.

The [TigerTrans](TigerTrans){.twikiLink} package contains the definition
of
[IntermediateRepresentation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}
and (mostly empty) templates for the components to be implemented. The
[TigerXmpl](TigerXmpl){.twikiLink} package provides example Tiger
programs and a makefile for testing the new components. The
[ASM](ASM){.twikiLink} package provides the signature of assembly code
that is used by instruction selection in
[TigerTrans](TigerTrans){.twikiLink}.

### []{#Translation_to_Expression_or_Sta} Translation to Expression or Statement

Tiger knows only expressions. During translation a distinction should be
made into Tiger expressions that return a value (proper expressions) and
expressions that do not (statements). The same syntactic construct can
represent expressions and statements. This hold in particular for
if-then-else (`If`) and sequential composition (`Seq`). The
expression/statement type of an expression can be determined by its
context. For example, the body of a function is an expression if the
function returns a value, otherwise it is a statement. This knowledge
can be expressed in the traversal strategy employed by the translator.

Make two kinds of rules, `TrExp` translates expressions and `TrStm`
translates statements. Let the strategy determine which should be
called.

### []{#Records} Records

For the translation of record creation and record access use the type
information that is available in the
[TigerAbstractSyntax](http://www.program-transformation.org/Tiger/TigerAbstractSyntax){.twikiLink}
tree after typechecking

### []{#Function_Calls} Function Calls

Translate a `Call` to a `CALL`. Don\'t worry about passing arguments in
registers or on the stack. This will be dealt with during
[InstructionSelection](InstructionSelection){.twikiLink}.

### []{#Passing_Information_Around} Passing Information Around

Information about memory locations of local variables, function
arguments, and [static links](StaticLink){.twikiLink} can be passed
around using [DynamicRules](../Stratego/DynamicRule){.twikiLink}. For
example, to translate a variable, generate a rule when translating its
variable declaration (`VarDec`) that translates a `Var(x)` to a `TEMP`
or to a memory access depending on where the variable is placed at
declaration time.

Functions such as `getchar`, which are defined in the run-time system of
Tiger, do not expect a static link. Thus, the call translation rules
generated for the built-in functions should not pass a static link.

### []{#Static_Links} Static Links

To compute [static links](StaticLink){.twikiLink} keep a list [stack
frames](StackFrame){.twikiLink}. A stack frame can be represented by its
name and the offset from the frame pointer to the location where its
[static link](StaticLink){.twikiLink} is stored. When the static link is
passed as first argument of a function the offset will be zero. Keep the
list in a dynamic rule, such that it can be updated while traversing
into the tree. The current frame is the head of the list. The distance
between the current frame and the frame in which a function or variable
was declared determines the number of steps that needs to be taken to
obtain the pointer to its enclosing [stack
frame](StackFrame){.twikiLink}.

### []{#Frame_Pointer_Offset} Frame Pointer Offset

To allocate stack bound arguments and local variables on the stack it is
necessary to maintain an offset to the [frame
pointer](FramePointer){.twikiLink}. Increment the offset after each
variable access. After completing the translation of the function, this
offset needs to be stored in the fragment for the function. See the
definition of the [intermediate
representation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}
for a description of the parameters passed to a `PROC` fragment.

### []{#Nested_Functions} Nested Functions

While translating, leave the nesting structure of functions by
translating a `Let` with function declarations to a `LET` with as first
argument a list of `PROC` fragments (see [intermediate
representation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}.)
As the first action of
[IRCanonicalize](http://www.program-transformation.org/Tiger/IRCanonicalize){.twikiLink}
remove this nesting structure by lifting `PROC` fragments to top-level.

### []{#Function_Bodies} Function Bodies

After translation the statements of a function body will be shuffled
around during canonicalization. In order to start at the right
statement, the translation should remember where the body starts and
where it ends. This should be communicated to [instruction
selection](InstructionSelection){.twikiLink} by putting a start label at
the beginning of the body and jump to an end label at the end of the
body. These labels should be declared as parameters of the `PROC`
fragment of the function.

### []{#String_Constants} String Constants

String constants should translated to a piece of code that declares
static program data. For example, with a
[MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}
back-end the string `"hello world!"` should be translated to

        .align 2
        .rdata
    a_0:
        .word 12
        .asciiz "hello world!"     

This specific translation can be defferred until [instruction
selection](InstructionSelection){.twikiLink}, however. During
translation string constants should be translated to a combination of a
`STRING` fragment that declares the label at which the string data can
be found and the string itself, and an expression that yields the
address of the label using the `NAME` constructor. This can be done
using the `LET` construct, i.e., a string `"hello world!"` translates to

      LET([STRING("a_0", "hello world!")], NAME("a_0"))

In order to avoid translating multiple occurrences of the same string to
multiple data declarations, store the label associated with the string
constant in a dynamic rule when first encountering the string and
reproducing the label when next encountering the string.

------------------------------------------------------------------------

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
