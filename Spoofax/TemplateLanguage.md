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
    Page](http://www.program-transformation.org/edit/Spoofax/TemplateLanguage?t=1536826265)
-   [Rename
    Page](http://www.program-transformation.org/rename/Spoofax/TemplateLanguage)
-   [Attach
    File](http://www.program-transformation.org/attach/Spoofax/TemplateLanguage)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Spoofax/TemplateLanguage?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Spoofax/TemplateLanguage?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Spoofax/TemplateLanguage?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Spoofax/TemplateLanguage?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Spoofax/TemplateLanguage?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Spoofax/TemplateLanguage?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Spoofax/TemplateLanguage?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Spoofax/TemplateLanguage?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Spoofax/TemplateLanguage)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Spoofax/TemplateLanguage?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Spoofax/TemplateLanguage?template=oopsmore&param1=1.5&param2=1.5)
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
Template Language {#template-language .twikiTopicTitle}
=================

::: {.twikiWebTitle}
Spoofax
:::

::: {.twikiToc}
-   [About](TemplateLanguage#About)
-   [Syntax Overview](TemplateLanguage#Syntax_Overview)
-   [Parsing](TemplateLanguage#Parsing)
-   [Unparsing / pretty
    printing](TemplateLanguage#Unparsing_pretty_printing)
    -   [Overview](TemplateLanguage#Overview)
    -   [Parenthezation](TemplateLanguage#Parenthezation)
    -   [How to use](TemplateLanguage#How_to_use)
-   [Completion templates](TemplateLanguage#Completion_templates)
-   [Implementation Notes](TemplateLanguage#Implementation_Notes)
-   [Publications](TemplateLanguage#Publications)
:::

[]{#About} About
================

The \"template language\" is a language that aims to eliminate
redundancy in the specification of grammar, completion templates, and
pretty printer. It borrows syntax from [SDF](../Sdf/WebHome){.twikiLink}
and [StringTemplate](http://stringtemplate.org/).

[]{#Syntax_Overview} Syntax Overview
====================================

**Template language sections**
:::
:::
:::
:::

`templates   t* `

Section with templates *t\**

`template options   o* `

Section with options *o\**

**Productions**

`Sort = < e* >`

Template with elements *e\**

`Sort.Constructor = < e* >`

Template with elements *e\**

`Sort = [ e* ]`

Template with elements *e\** (alt. brackets)

`Sort.Constructor = [ e* ]`

Template with elements *e\** (alt. brackets)

**Placeholders**

`<Sort>`

Placeholder (1)

`<Sort?>`

Optional placeholder (0..1)

`<Sort*>`

Repetition (0..n)

`<Sort+>`

Repetition (1..n)

`<Sort*; separator="\n">`

Repetition with separator

`<Sort; text="hi">`

Placeholder with replacement text

`<Sort; hide>`

Placeholder hidden from completion template

**Escapes**

`<\\\'\"\ \t\r\n>`

Element containing escaped characters

`<\u0065>`

Unicode escape

`<\\>`

Escape next line break

`<>`

No output; layout will be allowed here in the grammar

`\<`, `\>`, `\[`, `\]`, `\\`

Escaped brackets / backslash (prefer alt. brackets)

**Priority specification**

`context-free priorities  {left: Exp.Times Exp.Over} >  {left: Exp.Plus Exp.Minus}`

Refer to templates using sort and constructor name

**Lexical syntax**

`lexical syntax  ID = [A-Za-z] [A-Za-z0-9]*`

Lexical syntax similar to [SDF](../Sdf/WebHome){.twikiLink}

**Template options**

`keyword -/- [A-Za-z0-9]`

Follow restriction for keywords

`tokenize : "()"`

Layout is allowed around (sequences of) these characters

`newlines : none `

Experimental: generate grammar that requires newline characters.\
Possible values: `none`, `separating`, `leading`, `trailing`

[]{#Parsing} Parsing
====================

For each syntax template there is a simple mapping to a
[SDF](../Sdf/WebHome){.twikiLink} production. The semantics of the
parser for the syntax template is given entirely by the generated SDF
productions.

-   Literal strings are tokenized on space characters (whitespace, tab).
    Each token results in one literal in the production. That is,
    `hello world` maps to `"hello" "world"`, thus allowing any layout
    between the two tokens.
-   Additionally, literal strings are tokenized on boundaries between
    characters from the set given by the `tokenize` option, and any
    other characters. That is, `if()` maps to `"if" "(" Exp ")"`, to
    allow layout between the if keyword and the parentheses.
-   Placeholders translate literally. If a `separator` option containing
    any non-layout characters is given, the placeholder maps to a list
    with separator.

[]{#Unparsing_pretty_printing} Unparsing / pretty printing
==========================================================

[]{#Overview} Overview
----------------------

The pretty printer that is generated from syntax templates consists of a
number of [Stratego](../Stratego/StrategoLanguage){.twikiLink}
strategies. Each matches a particular pattern in the AST. If the pattern
matches, the strategy (recursively) invokes the pretty printing
strategies for the child nodes, and combines the results into a
[BOX](../Tools/BoxLanguage){.twikiLink} AST. This BOX AST can then be
converted to a string using the `box2text-string` strategy from
[libstratego-gpp](http://releases.strategoxt.org/docs/api/libstratego-gpp/libstratego-gpp-docs-stable/docs/).

For example, for a simple plus-expression syntax template:

      Exp.Plus = <<Exp> + <Exp>> {left}

the pretty printing strategy that may be generated is:

      prettyprint-Exp:
        Plus(a, b) ->
          [ H([SOpt(HS(), "0")], [ <pp-one-Z(prettyprint-Exp)> a, S(" + "), <pp-one-Z(prettyprint-Exp)> b ]) ]

As you can see, the pretty printing strategies return a list of boxes
that the caller should wrap in a `V` or `Z` box (among other things,
that is what `pp-one-Z` does). The user is responsible for this when
invoking one of the `prettyprint-*` strategies from their code!

All pretty printing strategies that are specific to a symbol are hooked
up to one global `prettyprint-LanguageName` strategy, so that it is easy
to pretty print an arbitrary subtree of an AST without knowing the type
of the root node in advance:

      prettyprint-LanguageName = prettyprint-Exp

[]{#Parenthezation} Parenthezation
----------------------------------

In Spoofax, it is common to not parse parentheses to an AST node. After
all, the fact that parentheses are necessary at some point in an
expression can be inferred from the priorities of the operators (which
are specified in the grammar) and the structure of the AST. The tool
`sdf2parenthesize` does exactly this, and is integrated into
[SpoofaxLang[^?^](http://www.program-transformation.org/edit/Spoofax/SpoofaxLang?topicparent=Spoofax.TemplateLanguage)]{.twikiNewLink
style="background : #FFFFCE;"} via the `parenthesize-LanguageName`
strategy. Invoking the `parenthesize-LanguageName` strategy results in
the addition of `Parenthetical` constructors to the AST at every place
where the structure of the AST conflicts with the operator priorities
specified in the grammar. The generated pretty printer knows how to
handle the `Parenthetical` constructor, because a syntax template for
parentheses with the `bracket` attribute, such as:

      Exp = <(<Exp>)> {bracket}

generates the pretty printing strategy:

      prettyprint-Exp:
        Parenthetical(a) ->
          [ H([SOpt(HS(), "0")], [ S("("), <pp-one-Z(prettyprint-Exp)> a, S(")") ]) ]

[]{#How_to_use} How to use
--------------------------

The idiomatic way to invoke the generated pretty printer, including
parenthezation, and a conversion to string (with word wrap at the 100th
column, if applicable), is:

      prettyprint-LanguageName-string =
        parenthesize-LanguageName
        ; prettyprint-LanguageName
        ; !V([], <id>)
        ; box2text-string(|100)

\-- [TobiVollebregt](../Main/TobiVollebregt){.twikiLink} - 01 Feb 2012\
[]{#TopicEnd}

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
