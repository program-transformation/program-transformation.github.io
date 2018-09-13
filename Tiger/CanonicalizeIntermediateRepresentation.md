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
    Page](http://www.program-transformation.org/edit/Tiger/CanonicalizeIntermediateRepresentation?t=1536826660)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/CanonicalizeIntermediateRepresentation)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/CanonicalizeIntermediateRepresentation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/CanonicalizeIntermediateRepresentation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/CanonicalizeIntermediateRepresentation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Tiger/CanonicalizeIntermediateRepresentation?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Tiger/CanonicalizeIntermediateRepresentation?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Tiger/CanonicalizeIntermediateRepresentation?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Tiger/CanonicalizeIntermediateRepresentation?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Tiger/CanonicalizeIntermediateRepresentation?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Tiger/CanonicalizeIntermediateRepresentation?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/CanonicalizeIntermediateRepresentation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/CanonicalizeIntermediateRepresentation?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Tiger/CanonicalizeIntermediateRepresentation?template=oopsmore&param1=1.6&param2=1.6)
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
Canonicalize Intermediate Representation {#canonicalize-intermediate-representation .twikiTopicTitle}
========================================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

### []{#Canonicalization} Canonicalization

Implement the
[IRCanonicalize](http://www.program-transformation.org/Tiger/IRCanonicalize){.twikiLink}
component that transforms
[IntermediateRepresentation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}
expressions into canonical form. The component can be found in directory
`ir/` of the [TigerTrans](TigerTrans){.twikiLink} package. The component
can be invoked using the `%.cir` target in the make-rules.

### []{#Lifting_Functions} Lifting Functions

During translation nested function declarations where left in place and
translated to the `LET` construct. Since addition of [static
links](StaticLink){.twikiLink} to functions makes functions independent
of their static position, their declarations can be lifted to top-level.

Lifting can be done nicely using `collect-split`. See module `collect`
in the [Stratego standard
library[^?^](http://www.program-transformation.org/edit/Stratego/StrategoStandardLibrary?topicparent=Tiger.CanonicalizeIntermediateRepresentation)]{.twikiNewLink
style="background : #FFFFCE;"}.

### []{#Linearize_Expressions} Linearize Expressions

Extend module
[IRCanonicalize](http://www.program-transformation.org/Tiger/IRCanonicalize){.twikiLink}
with transformation rules for linearizing an
[IntermediateRepresentation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}
expression and define a strategy to apply the linearization rules. The
result of linearization is a flat list of statements.

Beware for non-termination of `CALL` lifting. What is a good strategy?

By first simplifying expressions using simple constant folding rules,
better results can sometimes be obtained. Be aware that no side effects
should be removed or reordered by simplification.

### []{#Basic_Blocks} Basic Blocks

Divide the list of statements of a `PROC` into a list of [basic
blocks](BasicBlock){.twikiLink}.

-   [BasicBlockPositioning](../Transform/BasicBlockPositioning){.twikiLink}

### []{#Traces} Traces

Reorder the basic blocks into traces.

Make sure that each conditional jump (`CJUMP`) is followed by its false
label. If necessary rephrase the condition such that this is the case.

### []{#Call_Space} Call Space

After canonicalization compute the call space, i.e., the maximum number
of arguments of any function called (directly) within the body of a
function. This number is needed to compute the size of the [stack
frame](StackFrame){.twikiLink}. The number should be stored in the
`CALL` parameter of the `PROC` fragment of the function. (Use collect

### []{#Format_Checker} Format Checker

In order to check the result of canonicalization, define a
[FormatChecker](../Stratego/FormatChecker){.twikiLink} (using
[RecursivePattern](../Stratego/RecursivePattern){.twikiLink}) that
describes [intermediate
representation](http://www.program-transformation.org/Tiger/IntermediateRepresentation){.twikiLink}
expressions in canonical form in module
[CIRFormat](http://www.program-transformation.org/Tiger/CIRFormat){.twikiLink}.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
