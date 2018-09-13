::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![gpce-logo.jpg](../pub/GPCE10/WebLeftBar/gpce-logo.jpg){width="100"
height="120"}

**[GPCE Home](http://program-transformation.org/Gpce)**\
**[GPCE\'10 Home](WebHome){.twikiLink}**\
[Keynotes](KeynoteSpeakers){.twikiLink}\
[Schedule](ConferenceProgram){.twikiLink}\
[Accepted Papers](AcceptedPapers){.twikiLink}\
[Poster](Poster){.twikiLink}\
[Organization](ConferenceOrganization){.twikiLink}\
[Dates](ImportantDates){.twikiLink}\
[Venue](ConferenceVenue){.twikiLink}\
[Registration](ConferenceRegistration){.twikiLink}\

**Calls for**\
[Papers](CallForPapers){.twikiLink}\
[Tutorials](CallForTutorials){.twikiLink}

**Workshop**\
[FOSD](http://www.infosun.fim.uni-passau.de/cl/staff/apel/FOSD2010/index.html)

**[Electronic\
Submission](http://www.easychair.org/conferences/?conf=gpce10)**\
(Submission system is closed)\
Abstracts due: [Wednesday, May 26, 23:59:59, Apia
time](http://www.timeanddate.com/worldclock/fixedtime.html?month=5&day=26&year=2010&hour=23&min=59&sec=59&p1=282).\
Full papers due: [Sunday, May 30, 23:59:59, Apia
time](http://www.timeanddate.com/worldclock/fixedtime.html?month=5&day=30&year=2010&hour=23&min=59&sec=59&p1=282).
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/GPCE10/Tutorial4AgileEfficientDSLs?t=1536828788)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE10/Tutorial4AgileEfficientDSLs)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE10/Tutorial4AgileEfficientDSLs)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE10/Tutorial4AgileEfficientDSLs?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE10/Tutorial4AgileEfficientDSLs?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/GPCE10/Tutorial4AgileEfficientDSLs?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/GPCE10/Tutorial4AgileEfficientDSLs?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/GPCE10/Tutorial4AgileEfficientDSLs?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/GPCE10/Tutorial4AgileEfficientDSLs?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/GPCE10/Tutorial4AgileEfficientDSLs?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/GPCE10/Tutorial4AgileEfficientDSLs?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE10/Tutorial4AgileEfficientDSLs)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE10/Tutorial4AgileEfficientDSLs?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/GPCE10/Tutorial4AgileEfficientDSLs?template=oopsmore&param1=1.7&param2=1.7)
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
Generative Programming and Component Engineering
:::

### []{#Agile_and_Efcient_Domain_Specic}[]{#Agile_and_Efcient_Domain_Specic_} Agile and Efﬁcient Domain-Speciﬁc Languages using Multi-stage Programming in Java Mint

##### []{#http_www_cs_rice_edu_mgricken_Ma}[]{#_http_www_cs_rice_edu_mgricken_M} [Mathias Ricken](http://www.cs.rice.edu/~mgricken/), [Edwin Westbrook](http://www.cs.rice.edu/~emw4/), [Walid Taha](http://www.cs.rice.edu/~taha/)

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
systems.

[Walid Taha](http://www.cs.rice.edu/~taha/) is an professor at Halmstad
University. His current interest is in modeling and simulation of
cyberphysical systems. He was the principal investigator on a number of
research awards and contracts from the National Science Foundation
(NSF), Semi-conductor Research Consortium (SRC), and Texas Advanced
Technology Program (ATP). He received an NSF CAREER award to develop
Java Mint. He is the principle designer [Java
Mint](http://javamint.org), [Acumen](http://acumen.cyphy.org),
[MetaOCaml](http://metaocaml.org), and the Verilog Preprocessor. He
founded the ACM Conference on Generative Programming and Component
Engineering (GPCE), the IFIP Working Group on Program Generation (WG
2.11), and the Middle Earth Programming Languages Seminar (MEPLS). In
2009, he chaired the IFIP Working Conference on Domain Specific
Languages (DSLs).

Download slides in
[pdf](http://program-transformation.org/pub/GPCE10/ConferenceProgram/Mint-GPCE-tutorial-presentation-20101010-small.pdf)
or
[ppt](http://program-transformation.org/pub/GPCE10/ConferenceProgram/Mint-GPCE-tutorial-presentation-20101010.ppt).\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
