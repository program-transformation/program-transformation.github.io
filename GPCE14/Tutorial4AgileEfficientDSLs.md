::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![gpce-logo.jpg](../pub/GPCE14/WebLeftBar/gpce-logo.jpg){width="100"
height="120"}

**[GPCE Home](http://program-transformation.org/Gpce)**\
**[GPCE\'14 Home](WebHome){.twikiLink}**\
\
**[Registration](GpceRegistration){.twikiLink}**\
\
[Program](ConferenceProgram){.twikiLink}\
[Keynote](KeynoteSpeakers){.twikiLink}\
[Tech Talk](TechTalk){.twikiLink}\
\
[Poster and Flyer](Poster){.twikiLink}\
[Organization](ConferenceOrganization){.twikiLink}\
[Dates](ImportantDates){.twikiLink}\
[Call for Papers](CallForPapers){.twikiLink}\
\
[Grants](Grants){.twikiLink}\
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/GPCE14/Tutorial4AgileEfficientDSLs?t=1536828862)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE14/Tutorial4AgileEfficientDSLs)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE14/Tutorial4AgileEfficientDSLs)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE14/Tutorial4AgileEfficientDSLs?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE14/Tutorial4AgileEfficientDSLs?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/GPCE14/Tutorial4AgileEfficientDSLs?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/GPCE14/Tutorial4AgileEfficientDSLs?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/GPCE14/Tutorial4AgileEfficientDSLs?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/GPCE14/Tutorial4AgileEfficientDSLs?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/GPCE14/Tutorial4AgileEfficientDSLs?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE14/Tutorial4AgileEfficientDSLs)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE14/Tutorial4AgileEfficientDSLs?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/GPCE14/Tutorial4AgileEfficientDSLs?template=oopsmore&param1=1.3&param2=1.3)
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
Tutorial 4 {#tutorial-4 .twikiTopicTitle}
==========

::: {.twikiWebTitle}
Generative Programming: Concepts and Experiences
:::

### []{#Agile_and_Efcient_Domain_Specic}[]{#Agile_and_Efcient_Domain_Specic_} Agile and Efﬁcient Domain-Speciﬁc Languages using Multi-stage Programming in Java Mint

##### []{#http_www_cs_rice_edu_mgricken_Ma}[]{#_http_www_cs_rice_edu_mgricken_M} [Mathias Ricken](http://www.cs.rice.edu/~mgricken/), [Edwin Westbrook](http://www.cs.rice.edu/~emw4/)

###### []{#Abstract} Abstract

Domain-specific languages (DSLs) are a powerful productivity tool
because they allow domain experts, who are not necessarily programming
experts, to quickly develop programs. DSL implementations have unique
constraints for programming languages because they must be efficient, in
order to ensure high productivity, but they must also be agile, in order
to meet the rapidly changing demands of their domains. In this tutorial
we show how multi-stage programming (MSP) can be used to build staged
interpreters, which combine the agility of interpreters with the
efficiency of compilers. The tutorial is conducted in Java Mint, an
multi-stage Java based on recent work incorporating MSP into imperative
object-oriented languages. In the first half of the tutorial, we
introduce MSP by demonstrating how to write a staged interpreter for a
number of basic language constructs, such as recursive functions,
conditionals, and let expressions. In the second half, we extend our
staged interpreter to take advantage of several well-known compiler
optimizations, including type inference, constant folding, and static
parallel loop scheduling. We highlight the opportunities afforded by
using MSP with object-oriented design to quickly create efficient DSL
implementations.

###### []{#Author_bios} Author bios

[Mathias Ricken](http://www.cs.rice.edu/~mgricken/) is a doctoral
candidate in the Programming Languages Team at Rice University and one
of the principal developers of the DrJava integrated development
environment. His research interests include concurrent programming,
extending the Java language, and computer science education. He is the
developer of the Concutest concurrent unit testing framework and has
created various experimental extensions of Java to address, for
instance, programming with meta-data. Currently, Mathias is contributing
to Java Mint, a multi-stage extension of Java that allows safe and
expressive statically typed program generation and specialization in an
imperative language setting.

[Edwin Westbrook](http://www.cs.rice.edu/~emw4/) is a post-doctoral
researcher at Rice University. His primary interests are in developing
techniques for implementing and verifying properties of domain-speciﬁc
languages (DSLs). He has worked on a number of projects in this area,
including: Cinic, a type theory for building machine-checked proofs of
properties of DSLs using a new approach to higher-order abstract syntax;
Java Mint, a multi-stage version of Java used for efﬁcient
implementations of DSLs; and Acumen, a DSL for designing cyber-physical
systems.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
