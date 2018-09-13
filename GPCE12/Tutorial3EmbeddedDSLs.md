::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![gpce-logo.jpg](../pub/GPCE12/WebLeftBar/gpce-logo.jpg){width="100"
height="120"}

**[GPCE Home](http://program-transformation.org/Gpce)**\
**[GPCE\'12 Home](WebHome){.twikiLink}**\
**[GPCE\'13 Home](http://program-transformation.org/GPCE13/WebHome)**\

[Program](ConferenceProgram){.twikiLink}\
[Registration](GpceRegistration){.twikiLink}\
[Venue and Accommodation](VenueAccomodation){.twikiLink}\
[Organization](ConferenceOrganization){.twikiLink}\
[Dates](ImportantDates){.twikiLink}

**Calls for**\
[Papers](CallForPapers){.twikiLink}\
[Tech Talks](CallForTechTalks){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/GPCE12/Tutorial3EmbeddedDSLs?t=1536828834)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE12/Tutorial3EmbeddedDSLs)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE12/Tutorial3EmbeddedDSLs)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE12/Tutorial3EmbeddedDSLs?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE12/Tutorial3EmbeddedDSLs?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/GPCE12/Tutorial3EmbeddedDSLs?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/GPCE12/Tutorial3EmbeddedDSLs?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/GPCE12/Tutorial3EmbeddedDSLs?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/GPCE12/Tutorial3EmbeddedDSLs?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/GPCE12/Tutorial3EmbeddedDSLs?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE12/Tutorial3EmbeddedDSLs)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE12/Tutorial3EmbeddedDSLs?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/GPCE12/Tutorial3EmbeddedDSLs?template=oopsmore&param1=1.3&param2=1.3)
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
Tutorial 3 {#tutorial-3 .twikiTopicTitle}
==========

::: {.twikiWebTitle}
Generative Programming and Component Engineering
:::

### []{#Embedded_Domain_specic_Language}[]{#Embedded_Domain_specic_Language_} Embedded Domain-speciﬁc Language Implementation using Dependent Types

##### []{#http_www_cs_st_andrews_ac_uk_eb}[]{#_http_www_cs_st_andrews_ac_uk_eb} [Edwin Brady](http://www.cs.st-andrews.ac.uk/~eb/)

###### []{#Abstract} Abstract

Domain-speciﬁc languages (DSLs) are programming languages designed for
solving problems in a particular domain. By providing suitable
abstractions, they allow experts to focus on solving high-level problems
without being concerned with low-level programming details. Embedded
domain-speciﬁc languages (EDSLs) are an emerging implementation
technique, in which features of a host language, for example parsing or
code generation, are exploited by the DSL implementation. In this way,
EDSLs can be implemented much more rapidly than their standalone
equivalents and can take advantage of compiler optimisations and other
implementation effort in the host.

Dependent types allow types to be predicated on values. Using dependent
types, a programmer can ascribe a precise type to a program, for example
that concatenating lists of length n and m yields a list of length n +
m, or that sorting a list of length n yields a list of length n which is
a permutation of its input satisfying a given ordering. In this way,
types can be viewed as a form of speciﬁcation, veriﬁed by the type
checker.

Using a dependently typed language as the host for an EDSL brings
additional beneﬁts. Not only can we reuse the host language's parser and
code generator, we can exploit its type system to express properties of
the EDSL and guarantee their correctness. In this tutorial I will
introduce I DRIS, a dependently typed functional programming language. I
will give practical examples of dependently type programs, culminating
in the construction of an EDSL for network protocol implementation.

###### []{#Author_biography} Author biography

[Edwin Brady](http://www.cs.st-andrews.ac.uk/~eb/) is a SICSA Advanced
Research Fellow in Computer Science at the University of St Andrews,
where he has worked since receiving his PhD from the University of
Durham in 2005. His research interests include functional programming
with dependent types, type theory, program generation and programming
language design and implementation. His previous work has included
compilation and optimisation techniques for dependently typed functional
programming languages. This has important applications in the
veriﬁcation of safety-critical systems; he has also been closely
involved with the Hume project (<http://www.hume-lang.org/>), applying
dependent type systems to the correct implementation of safety-critical
embedded systems with limited memory. He is the main developer of I DRIS
(<http://www.idris-lang.org/>), a functional language with dependent
types intended for systems programming, and contributes to the
development of Epigram (<http://www.e-pig.org/>). His recent work has
focused on the practical applications of dependently typed programming,
using I DRIS to implement domain-speciﬁc languages for veriﬁed network
protocols, data formats, and resource aware systems in general.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
