::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[Spoofax](http://www.program-transformation.org/view/Spoofax/WebHome)**

\

**[Home](WebHome){.twikiLink}**

**[Tour and screenshots](Tour){.twikiLink}**

**[Documentation](Documentation){.twikiLink}**

**[Download](Download){.twikiLink}**

**[Research](Research){.twikiLink}**

**[Development](Development){.twikiLink}**

**[Support](Support){.twikiLink}**

\

\
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Spoofax/Testing?t=1536825365)
-   [Rename
    Page](http://www.program-transformation.org/rename/Spoofax/Testing)
-   [Attach
    File](http://www.program-transformation.org/attach/Spoofax/Testing)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Spoofax/Testing?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Spoofax/Testing?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Spoofax/Testing?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Spoofax/Testing?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Spoofax/Testing?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Spoofax/Testing?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Spoofax/Testing?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Spoofax/Testing)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Spoofax/Testing?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Spoofax/Testing?template=oopsmore&param1=1.3&param2=1.3)
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
Test-Driven Language Development with Spoofax {#test-driven-language-development-with-spoofax .twikiTopicTitle}
=============================================

::: {.twikiWebTitle}
Spoofax
:::

This short primer shows how to use tests as a basis for language
development with Spoofax. As an example project we create a small
\'calculator\' language that shows many of the basics of language
definitions.

The source for our example project is collected in
[before.zip[^?^](http://www.program-transformation.org/edit/Spoofax/PubSpoofaxTestingbeforezip?topicparent=Spoofax.Testing)]{.twikiNewLink
style="background : #FFFFCE;"}. The complete project, with all
functionality implemented to make the test cases succeed is collected in
[after.zip[^?^](http://www.program-transformation.org/edit/Spoofax/PubSpoofaxTestingafterzip?topicparent=Spoofax.Testing)]{.twikiNewLink
style="background : #FFFFCE;"}.

A full description of the testing language can be found in the paper
[Integrated Language Definition Testing. Enabling Test-Driven Language
Development](http://researchr.org/publication/KatsVermaasVisser2011).
Presentation slides also show Spoofax testing in action:
<http://slidesha.re/tYaHQT>

::: {.twikiToc}
-   [A Calculator Language](Testing#A_Calculator_Language)
-   [Syntax](Testing#Syntax)
-   [Evaluation of expressions](Testing#Evaluation_of_expressions)
-   [Variables](Testing#Variables)
-   [Editor features](Testing#Editor_features)
-   [Execution](Testing#Execution)
:::

[]{#A_Calculator_Language} A Calculator Language
------------------------------------------------

Our example language supports arithmetic expressions, variables, and
assignments. An example:

    a = 3
    a * 4

Based on this simple language we can write test cases. Doing test-driven
development, these can even drive the development of the language, but
in this document we focus on the tests.

Tests can be written using a `.spt` file. Create one in a Spoofax
project, and press control-space to get a basic test definition. It will
have tests of this form:

    test description [[
      a = 3
      a * 4
    ]] 0 errors

As the example shows, each test can quote a program using `[[`, `[[[` or
`[[[[` brackets. It can also specify a *description* for the test, and a
condition. This test specifies that `0` semantic `errors` are expected.

[]{#Syntax} Syntax
------------------

Example of tests of the syntax:

    test Add [[
      1 + 2
    ]] parse succeeds

    test Abstract syntax (1) [[
      1
    ]]
      parse to Int("1")

    test Abstract syntax (2) [[
      1 * 2
    ]]
      parse to Mul(Int("1"), _)

    test Parentheses [[
      (1 + 2)
    ]]

These tests specify parse success, compare the abstract syntax of the
test input against a pattern, or simply specify that the test should
succeed.

Tests can also use concrete syntax to test operator precedence and
associativity:

    test Multiply and add (1) [[
      1 + 2 * 3
    ]] parse to Add(_, Mul(_, _))

    test Multiply and add (2) [[
      1 + 2 * 3
    ]] parse to [[
      1 + (2 * 3)
    ]]

    test Add and multiply [[
      1 * 2 + 3
    ]] parse to [[
      (1 * 2) + 3
    ]]

    test Add and add [[
      1 + 2 + 3
    ]] parse to [[
      (1 + 2) + 3
    ]]

[]{#Evaluation_of_expressions} Evaluation of expressions
--------------------------------------------------------

The following tests will `run` a transformation named `calc` to test
evaluation of expressions:

    test Constant [[
      1
    ]] run calc to "1"

    test Add [[
      1 + 1
    ]] run calc to "2"

    test Subexpression [[
      1 + [[2 + 3]]
    ]] run calc to "5"

Note that the last test in this series uses the `[[` \... `]``]`
brackets to make a **selection** in the test. The `calc` transformation
is evaluated for this selection.

[]{#Variables} Variables
------------------------

The following tests exercise the definition of variables:

    test Variable [[
      x
    ]] parse

    test Variable [[
      longname
    ]] parse

    test Assignment [[
      x = 4
    ]] parse

    test Multiple statements [[
       x = 1
       y = 2
    ]] parse to Statements([Assign(_, _), Assign(_, _)])

        Stm*       -> Start {cons("Statements")}
        ID "=" Exp -> Stm {cons("Assign")}
        Exp        -> Stm
        ID         -> Exp {cons("Var")}

    test Evaluate multiple statements [[
      1
      2
    ]] run calc to "2"

      calc:
         Statements(s*) -> last
         where
            s'*  := <map(calc)> s*;
            last := <last> s'*

    test Eval constant [[
      PI
    ]] run calc to "3.14"

      calc:
        Var("PI") -> "3.14"

    test Eval multiple variables [[
      x = 2
      y = x * 2 + x
      y
    ]] run calc to "6"

[]{#Editor_features} Editor features
------------------------------------

The following test cases test the editor facilities of the language:

    test Variable unassigned [[
      y
    ]] 1 error /unassigned/

This test succeeds if the input has `1 error` and it matches the regular
expression `/unassigned/` (as variable `y` is unassigned).

    test Multiple assignments to same variable [[
      y = 1
      y = 2
      y
    ]] /multiple/

This test succeeds if there are one or more (error) messages that match
`/multiple/` (as there are *multiple* definitions of `y`).

    test Reference resolving (1) [[
      x = 4
      [[x]]
    ]] resolve

    test Reference resolving (2) [[
      [[x]] = 4
      [[x]]
    ]] resolve #2 to #1

    test Content completion [[
      avariable = 1
      [[a]]
    ]] complete to "avariable"

These test cases test reference resolving and content completion. They
use the `[[` \... `]``]` selection mechanic to select parts of the
program. The first test case specifies that reference resolving should
work for the selection. The second specifies that the second selection
should resolve to the first selection. The last test case specifies that
the selection should provide a content completion option `avariable`.

[]{#Execution} Execution
------------------------

The `Calculang` project generates Java code. The following test case
tests the output that is returned when the program is compiled and
executed:

    test 42 [[
      42
    ]] build generate-result to 42

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
:::
