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
    Page](http://www.program-transformation.org/edit/Tiger/HpcTigerAbstractSyntax?t=1536826699)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/HpcTigerAbstractSyntax)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/HpcTigerAbstractSyntax)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/HpcTigerAbstractSyntax?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/HpcTigerAbstractSyntax?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Tiger/HpcTigerAbstractSyntax?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/HpcTigerAbstractSyntax)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/HpcTigerAbstractSyntax?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Tiger/HpcTigerAbstractSyntax?template=oopsmore&param1=1.1&param2=1.1)
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
Hpc Tiger Abstract Syntax {#hpc-tiger-abstract-syntax .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

**Tiger Abstract Syntax**

This is the first set of [HpcExercises](HpcExercises){.twikiLink} that
will teach you the structure of the abstract syntax of the
[TigerLanguage](TigerLanguage){.twikiLink}, the use of the
[StrategoCompiler[^?^](http://www.program-transformation.org/edit/Tiger/StrategoCompiler?topicparent=Tiger.HpcTigerAbstractSyntax)]{.twikiNewLink
style="background : #FFFFCE;"} and writing a simple transformation on
Tiger programs. The result of the final exercise is the first component
to add to the [TigerCompiler](TigerCompiler){.twikiLink}:
[TigerDesugar](http://www.program-transformation.org/Tiger/TigerDesugar){.twikiLink}.

Here is an example Tiger program that will be referred to in the
following exercises:

let var a:= 0 function g(a: int) : int = a + 1 in if a \<\> 0 then g(2)
else g(3) end

1.  Download and install the [WebHome](WebHome){.twikiLink}
    distribution. (See also
    [StrategoAtCSUUNL](StrategoAtCSUUNL){.twikiLink})

<!-- -->

1.  Write the abstract syntax representation according to the Tiger
    signature in the sig/ directory of the
    [TigerLanguage](TigerLanguage){.twikiLink} program above.

<!-- -->

1.  Implement the identity transformation, compile it and apply it to
    the term of exercise 2.

<!-- -->

1.  Parse the example program to produce abstract syntax automatically
    using the parse-tiger program, which calls the SGLR parser and the
    [ImplodeAsFix[^?^](http://www.program-transformation.org/edit/Tiger/ImplodeAsFix?topicparent=Tiger.HpcTigerAbstractSyntax)]{.twikiNewLink
    style="background : #FFFFCE;"} program. See xmpl/make-rules and look
    at the targets for %.pre-tas. (See
    [ApplyingTisComponents[^?^](http://www.program-transformation.org/edit/Tiger/ApplyingTisComponents?topicparent=Tiger.HpcTigerAbstractSyntax)]{.twikiNewLink
    style="background : #FFFFCE;"} for an explanation.)

<!-- -->

1.  Use the pretty-printer to format the abstract syntax as text. See
    the target for %.txt in xmpl/make-rules.

<!-- -->

1.  Specify a transformation that normalizes all expressions such that
    additions and multiplications become right associative, i.e., of the
    form (x + (y + z)).

<!-- -->

1.  Write a transformation that defines for loops in terms of while
    loops.

<!-- -->

1.  Write a desugaring component
    ([TigerDesugar](http://www.program-transformation.org/Tiger/TigerDesugar){.twikiLink})
    that

-   -   defines Boolean conjunction and disjunction in terms of
        conditionals;

<!-- -->

-   -   flattens let expressions such that only one variable
        declarations or set of function declarations per let binding is
        used;

<!-- -->

-   -   expresses binary operators such as Plus, Times, Minus, etc. in
        terms of the [BinOp](BinOp){.twikiLink} en
        [RelOp[^?^](http://www.program-transformation.org/edit/Tiger/RelOp?topicparent=Tiger.HpcTigerAbstractSyntax)]{.twikiNewLink
        style="background : #FFFFCE;"} operators;

<!-- -->

-   -   removes redundant Seq(\[\_\]) contexts

1.  Apply
    [TigerDesugar](http://www.program-transformation.org/Tiger/TigerDesugar){.twikiLink}
    to the term of exercise 2. Verify that the result is correct by
    checking it with
    [TigerAbstractSyntaxFormat](TigerAbstractSyntaxFormat){.twikiLink}
    (see the targets %.tas and %.tas.check in xmpl/make-rules).

The next set of exercises concerns
[HpcTranslationToIR](HpcTranslationToIR){.twikiLink}.

**Notes**

The basic technique to use in the specification exercises is that of
writing rules of the form

Lab : lhs -\> rhs

where \'lhs\' is a term pattern that describes the term to transform and
\'rhs\' is a term pattern that describes the term to which it should be
transformed. The label \'Lab\' is the name of the rule and can be used
in strategies to invoke the rule.

The rules you write should be applied to a program by traversing it to
each node. Useful strategies are \'topdown(s)\' that applies a strategy
\'s\' to each node of a tree and \'try(s)\' that tries to apply a
strategy but succeeds also if the strategy did not succeed.

To make a strategy into the main strategy of a transformation component
you have to read a term from file, apply the strategy and write it back
to some other file. These actions can be programmed using the primitives
\'ReadFromFile\' and \'WriteToTextFile\' (see the
[StrategoLibrary[^?^](http://www.program-transformation.org/edit/Tiger/StrategoLibrary?topicparent=Tiger.HpcTigerAbstractSyntax)]{.twikiNewLink
style="background : #FFFFCE;"}), but that requires writing strategies to
handle command-line options and such. Therefore, the
[StrategoLibrary[^?^](http://www.program-transformation.org/edit/Tiger/StrategoLibrary?topicparent=Tiger.HpcTigerAbstractSyntax)]{.twikiNewLink
style="background : #FFFFCE;"} defines a couple of standard io wrappers.
The simplest one \'stdio(s)\' reads a term from stdin, applies the
strategy and writes the result to stdout. The more sophisticated
\'iowrap(s)\' can also do that, but in addition handles a couple of
command-line options. The most relevant are \'-i infile\' to name the
input file and \'-o outfile\' to name the output file name.

When you import a module from a different directory use the \'-I dir\'
option to sc to extend the include path. For example if you import the
Tiger signature in the Right-Associative module (in directory
tiger/assoc/) use

sc -i Right-Associative -I ../sig

The path to the
[StrategoLibrary[^?^](http://www.program-transformation.org/edit/Tiger/StrategoLibrary?topicparent=Tiger.HpcTigerAbstractSyntax)]{.twikiNewLink
style="background : #FFFFCE;"} is added by default. (See also
\*/Makefile.am)\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
