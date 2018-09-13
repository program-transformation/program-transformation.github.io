::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[WebHome](WebHome){.twikiLink}**\
[Transformation](../Transform/WebHome){.twikiLink}\
[GPCE](../Gpce/WebHome){.twikiLink}\
\
[Stratego/XT](../Stratego/WebHome){.twikiLink}\
[Tiger](../Tiger/WebHome){.twikiLink}\
[Tools](../Tools/WebHome){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Main/ArthurVanDam?t=1536825551)
-   [Rename
    Page](http://www.program-transformation.org/rename/Main/ArthurVanDam)
-   [Attach
    File](http://www.program-transformation.org/attach/Main/ArthurVanDam)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Main/ArthurVanDam?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Main/ArthurVanDam?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    51](http://www.program-transformation.org/view/Main/ArthurVanDam?rev=1.51)
    [(diff 50)](http://www.program-transformation.org/rdiff/Main/ArthurVanDam?rev1=1.51&rev2=1.50)
-   [Rev
    50](http://www.program-transformation.org/view/Main/ArthurVanDam?rev=1.50)
    [(diff 49)](http://www.program-transformation.org/rdiff/Main/ArthurVanDam?rev1=1.50&rev2=1.49)
-   [Rev
    49](http://www.program-transformation.org/view/Main/ArthurVanDam?rev=1.49)
    [(diff 48)](http://www.program-transformation.org/rdiff/Main/ArthurVanDam?rev1=1.49&rev2=1.48)
-   [Total
    History](http://www.program-transformation.org/rdiff/Main/ArthurVanDam)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Main/ArthurVanDam?template=oopsmore&param1=1.51&param2=1.51)
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
    \...](http://www.program-transformation.org/oops/Main/ArthurVanDam?template=oopsmore&param1=1.51&param2=1.51)
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
Arthur Van Dam {#arthur-van-dam .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Program-Transformation.Org
:::

-   **Name:** Arthur van Dam
-   **Email:** <adam@cs.uu.nl>
-   **Personal homepage:** <http://www.eye-home.net>
-   **Research homepage:** <http://arthur.van-dam.net/twiki/>
-   **Country:** Netherlands
-   **Main activity:** Adaptive Solution Techniques for PDE systems as
    PhD student at the [Mathematical Institute,
    Utrecht](http://www.math.uu.nl)
-   **Program transformation activities:**
    -   [DynamicRules](../Stratego/DynamicRule){.twikiLink}
    -   Various (too much) sidetracks concerning small Stratego
        thingies.

::: {.twikiToc}
-   [Thesis Computer Science](ArthurVanDam#Thesis_Computer_Science)
    -   [Abstract](ArthurVanDam#Abstract)
-   [Another LaTeX thesis documentclass:
    st-thesis](ArthurVanDam#Another_LaTeX_thesis_documentcla)
    -   [Features](ArthurVanDam#Features)
    -   [Usage](ArthurVanDam#Usage)
    -   [Additional commands](ArthurVanDam#Additional_commands)
    -   [Download](ArthurVanDam#Download)
    -   [Questions or Feature
        requests](ArthurVanDam#Questions_or_Feature_requests)
-   [stratego in LaTeX](ArthurVanDam#stratego_in_LaTeX)
    -   [Features](ArthurVanDam#Features)
    -   [Usage](ArthurVanDam#Usage)
    -   [Download](ArthurVanDam#Download)
:::

------------------------------------------------------------------------

### []{#Thesis_Computer_Science} Thesis Computer Science

Arthur van Dam. **Extending Dynamic Rules, An Application Oriented Study
Into Stratego's New Dynamic Rules**. MSc Thesis INF/SCR-04-25. Center
for Software Technology, Institute of Information and Computing
Sciences, Utrecht University, February 2004.
([pdf](http://www.cs.uu.nl/~visser/ftp/Dam04.pdf))

#### []{#Abstract} Abstract

The Stratego language for program transformation is based on a
strategy-controlled application of basic rewrite rules. These rewrite
rules have only local knowledge of the input term they are rewriting.
Information gained elsewhere in the transformation of the input tree is
unknown. Getting this context information available elsewhere in the
transformation will make the rewrite system more specific for its
current input, hence more powerful.

Dynamic rules are rewrite rules that can be generated at runtime. They
may contain specific information aimed at the current input that has
just become known. In Stratego 0.10 the dynamic rule system has been
completely revised and now offers rule (re-/un-)defining, scoping,
refined scoping by scope-labeling, forking followed by intersection or
union in controlflow situations, and rule set extending when multiple
rules should not redefine each other.

The dynamic rule concepts are introduced and illustrated in the context
of three case studies: Shrinking inlining in a small lambda calculus,
constant propagation in the imperative Tiger language, and deforestation
in a first-order functional language.

The implementation and representation of dynamic rules is sketched, and
their qualitative performance is investigated by several benchmarks.

------------------------------------------------------------------------

### []{#Another_LaTeX_thesis_documentcla} Another LaTeX thesis documentclass: st-thesis

Some of the graduate students suggested to use a more-or-less uniform
style for their theses. And hey, as a LaTeX fan, I immediately made an
initial setup of a package \`stratego\` and a documentclass
\`stratego-thesis\`.

#### []{#Features} Features

Some (optional) features of documentclass \`stratego-thesis\`:

-   B5 and A4 paper format
-   Sans-serif document font
-   Fancy headings
-   Several tiny layout tweaks

#### []{#Usage} Usage

    \documentclass[]{st-thesis}

Below are the available options (most are default). Defaults can be
switched off by using:

    \documentclass[sffont=false,12pt,color=false]{st-thesis}

-   **parskip** (default)\
    Extra vertical space at start of paragraph. Zero Parindent
    (horizontal indent) and non-zero Parskip (vertical space).
-   \*marginnotes\*\
    Account for marginnotes, make sure headers still look ok. Not
    thoroughly tested.
-   **sffont** (default)\
    Use a sans-serif font as document default.
-   **twoside** (default)\
    Generate double sided document.
-   **b5paper** (default)\
    Use B5 paper format.
-   **a4paper**\
    Use A4 paper format.
-   **widepage** (default) Make pagewidth somewhat bigger, comparable to
    package \'a4wide\'.
-   **fancyhdr** (default)\
    Use package \'fancyhdr\', highly recommended.
-   **hyperref** (default)\
    Use package hyperref, for fancy clickable links, pdf-toc, and all
    such good stuff.
-   **openright** (default)\
    Make sure each chapter starts at a right page.
-   **color** (default)\
    Sets some more eye-friendly colors for (hyper-)links and citations.
    Switch off for printing.
-   **10pt** (default)\
    Fontsize 10 as document default.
-   **11pt**\
    Fontsize 11 as document default.
-   **12pt**\
    Fontsize 12 as document default.
-   **reportopt**\
    Allows to pass on additional options to underlying package `report`.
    Usage: `\documentclass[...,reportop={fleqn,openbib},..]{st-thesis}`

#### []{#Additional_commands} Additional commands

-   `\frontmatter` Light-weight variant of `\frontmatter` in the `book`
    documentclass. Just changes page numbering to roman (i, ii, \...).
-   `\mainmatter` Light-weight variant of `\mainmatter` in the `book`
    documentclass. Just changes page numbering to arabic (1, 2, \...).

<!-- -->

-   `\preface` Makes a numberless chapter, titled \'Preface\', with
    proper hyperlinking and TOC-entry.
-   `\introduction` Idem, now for \'Introduction\'
-   `\chapnonr{TOC-text}{chapter-text}` Equivalent of `\chapter*`, but
    now with an unnumbered entry in table of contents, and proper
    hyperlinking.

#### []{#Download} Download

-   <http://losser.st-lab.cs.uu.nl/~adam/tex/>\
    You need `st-thesis.cls`. Make sure it\'s in your writing directory,
    or in a path contained in `$TEXINPUTS`. Also download `geometry.sty`
    and place it in your writing directory. This is version 2.2 of
    geometry, for newer versions of package geometry, st-thesis produces
    other layout.

#### []{#Questions_or_Feature_requests} Questions or Feature requests

Mail to <adam@cs.uu.nl>

### []{#stratego_in_LaTeX} stratego in LaTeX

For stratego-related writing, here are some listings- and
stratego-semantics-oriented commands, available in package \`stratego\`.

#### []{#Features} Features

Some features of package \`stratego\`:

-   highlighted Stratego code, and Tiger, ATerm, SDF2, and more.
-   Code fragments as floats

#### []{#Usage} Usage

    \usepackage{stratego}

-   No options needed.
-   Provided commands:
    -   todo\...

#### []{#Download} Download

-   <http://losser.st-lab.cs.uu.nl/~adam/tex/>\
    You need `stratego.sty` and `stratego-langdefs.tar.gz`. Unpacking
    the latter yields an `ldf/` directory with language definitions (for
    simple code-highlighting). Make sure `stratego.sty` and the
    directory `ldf/` are in your working directory, or in a path
    contained in `$TEXINPUTS`.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
