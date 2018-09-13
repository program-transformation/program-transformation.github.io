::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
  ----------------------------------------------------------------------------------
  [![](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)](WebHome)
  ----------------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

-   [Documentation](StrategoDocumentation){.twikiLink}
-   [Language](StrategoLanguage){.twikiLink}
-   [Research Papers](StrategoPublications){.twikiLink}
-   [Applications](StrategoApplication){.twikiLink}

**[Download](StrategoDownload){.twikiLink}**

-   [Continuous build](ContinuousBuild){.twikiLink}
-   [Extensions](AdditionalPackageDownload){.twikiLink}

**[Support](StrategoSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Users Days](StrategoUsersDay){.twikiLink}
-   [Bug Reports](http://yellowgrass.org/project/StrategoXT)

**[Developers](StrategoDev){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/StrategoXT/strategoxt/trunk)
-   [Buildfarm
    results](http://hydra.nixos.org/jobset/strategoxt/strategoxt-release/all)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Stratego/FourthStrategoUsersDay?t=1536825537)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/FourthStrategoUsersDay)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/FourthStrategoUsersDay)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/FourthStrategoUsersDay?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/FourthStrategoUsersDay?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    23](http://www.program-transformation.org/view/Stratego/FourthStrategoUsersDay?rev=1.23)
    [(diff 22)](http://www.program-transformation.org/rdiff/Stratego/FourthStrategoUsersDay?rev1=1.23&rev2=1.22)
-   [Rev
    22](http://www.program-transformation.org/view/Stratego/FourthStrategoUsersDay?rev=1.22)
    [(diff 21)](http://www.program-transformation.org/rdiff/Stratego/FourthStrategoUsersDay?rev1=1.22&rev2=1.21)
-   [Rev
    21](http://www.program-transformation.org/view/Stratego/FourthStrategoUsersDay?rev=1.21)
    [(diff 20)](http://www.program-transformation.org/rdiff/Stratego/FourthStrategoUsersDay?rev1=1.21&rev2=1.20)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/FourthStrategoUsersDay)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/FourthStrategoUsersDay?template=oopsmore&param1=1.23&param2=1.23)
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
    \...](http://www.program-transformation.org/oops/Stratego/FourthStrategoUsersDay?template=oopsmore&param1=1.23&param2=1.23)
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
Fourth [Stratego Users Day](StrategoUsersDay){.twikiLink} (SUD\'03)

June 5, 2003

Utrecht University

Utrecht, The Netherlands

::: {.twikiToc}
-   [Achievements](FourthStrategoUsersDay#Achievements)
-   [Call for
    Participation](FourthStrategoUsersDay#Call_for_Participation)
-   [Venue](FourthStrategoUsersDay#Venue)
-   [Program](FourthStrategoUsersDay#Program)
-   [Registered
    Participants](FourthStrategoUsersDay#Registered_Participants)
-   [Important Dates](FourthStrategoUsersDay#Important_Dates)
:::

### []{#Achievements} Achievements

The last year was again a productive year for the Stratego/XT project.

The union of the Stratego and XT distributions was necessary to overcome
the development deadlock caused by the introduction of concrete syntax.
The autoxt package provides support for automake, dramatically reducing
the size of makefiles. The introduction of the [XTC](XTC){.twikiLink}
transformation tool composition model makes it a piece of cake to glue
together tools. Concrete syntax is now completely integrated in the
Stratego compiler; the LEX/Transform.YetAnotherCompilerCompiler based
parser has been replaced by an [SDF](SDF){.twikiLink} parser. Rob
Vermaas is developing a documentation generator for Stratego (and for
other languages), which should make the use of the library and any
Stratego sources much easier. Martin Bravenboer is currently cleaning up
the XT packages. The 0.9 distribution builds smoothly at many platforms
and the first binary distributions have been produced.

Lots of new applications were developed and existing applications were
revamped to use the latest technology. The Tiger compiler was refactored
to use autoxt and [XTC](XTC){.twikiLink}. A partial evaluator was
developed for the program transformation course at Utrecht University.
Martin Bravenboer wrote a front-end package for Java and developed a set
of XML tools including schema-based validation. Karina Olmos and Gordon
Cichone are working on a compiler for Octave. A collaboration with Bernd
Fischer from NASA Ames was initiated to work on optimization of code
generated by their [AutoBayes](AutoBayes){.twikiLink} synthesis system.

A record number of theses based on Stratego related work were finished.
At Utrecht University Lennart Swart wrote a Master\'s thesis on partial
evaluation of scheme programs in Stratego. At the University of
Amsterdam Merijn de Jonge defended his PhD thesis on software reuse with
Stratego/XT as a case study. At Bergen University Otto Bagge and
Karl-Trygve Kalleberg defended their master\'s theses on the design and
implementation of [CodeBoost](CodeBoost){.twikiLink}, a domain-specific
source-to-source optimizer for numeric programs in C++.

A number of papers were presented at conferences and workshops. At
WRS\'02 Karina Olmos presented [Strategies for source to source constant
propagation](StrategiesForSourceToSourceConstantPropagation){.twikiLink}.
At RTA\'02 Eelco Visser presented [Rewriting strategies for instruction
selection](RewritingStrategiesForInstructionSelection){.twikiLink}. At
GPCE\'02 Eelco Visser presented [Meta programming with concrete object
syntax](MetaProgrammingWithConcreteObjectSyntax){.twikiLink}. Ralf
Laemmel presented [Strategic programming meets adaptive
programming](../Transform/StrategicProgrammingMeetsAdaptiveProgramming){.twikiLink}
at AOSD\'03.

### []{#Call_for_Participation} Call for Participation

So it is high time to take stock at another Stratego Users Day. On
Thursday June 5, 2003 we meet at Utrecht University so that everyone
interested in Stratego can get up to date with current developments, and
get an overview of ongoing activities. It is also a good opportunity for
Master\'s students to see what is going on in the program transformation
project.

Participation is free and includes lunch. Usually we go out for dinner
at night, which is at your own expense. Please register as soon as
possible so that we can make reservations for lunch and dinner by
sending an email to <visser+sud03@cs.uu.nl>. If you are coming from
outside and need accomodation, you can consult the [list of recommended
hotels](http://www.cs.uu.nl) of the department.

### []{#Venue} Venue

The meeting will be held at the Uithof campus of Utrecht University:\

Room BBL-420\
Buys Ballot Laboratorium\
Princetonplein 5\
3584 CC Utrecht\
Directions \--\> <http://www.cs.uu.nl/docs/reach/>

### []{#Program} Program

10:00 Tools (chair: Martin Bravenboer)

-   Transformation Tool Composition with [XTC](XTC){.twikiLink} \--
    Eelco Visser
    ([slides](ftp://ftp.stratego-language.org/pub/stratego/SUD03/sud03-xtc.pdf))
-   User-Defined Rules in [CodeBoost](CodeBoost){.twikiLink} \-- Otto
    Bagge
    ([slides](ftp://ftp.stratego-language.org/pub/stratego/SUD03/sud03-udr.pdf))

11:00 (chair: Merijn de Jonge)

-   ATerm/SDF report from CWI \-- Jurgen Vinju
    ([slides](ftp://ftp.stratego-language.org/pub/stratego/SUD03/sud03-aterm.pdf))
-   Generating Code and API Documentation with
    [ExtendibleDocumentationGenerator](ExtendibleDocumentationGenerator){.twikiLink}
    \-- Rob Vermaas (Eelco Visser)
    ([slides](ftp://ftp.stratego-language.org/pub/stratego/SUD03/sud03-xdoc.pdf))

12:00 Lunch

13:30 Configuration and Deployment (chair: Eelco Dolstra)

-   Testing Packages in the ST Buildfarm \-- Armijn Hemel
    ([slides](ftp://ftp.stratego-language.org/pub/stratego/SUD03/sud03-buildfarm.pdf))
-   Building [StrategoXT](StrategoXT){.twikiLink} packages with
    [AutoXT](AutoXT){.twikiLink} \-- Eelco Visser
    ([slides](ftp://ftp.stratego-language.org/pub/stratego/SUD03/sud03-autoxt.pdf))

14:00 XML (chair: Jurgen Vinju)

-   [XML
    Tools[^?^](http://www.program-transformation.org/edit/Stratego/XmlTools?topicparent=Stratego.FourthStrategoUsersDay)]{.twikiNewLink
    style="background : #FFFFCE;"} and [Stratego
    Networking](StrategoNetworking){.twikiLink} \-- Martin Bravenboer
    ([slides](ftp://ftp.stratego-language.org/pub/stratego/SUD03/sud03-xml-net.ps))
-   [StrategoWeb[^?^](http://www.program-transformation.org/edit/Stratego/StrategoWeb?topicparent=Stratego.FourthStrategoUsersDay)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- Niels Janssen
    ([slides](ftp://ftp.stratego-language.org/pub/stratego/SUD03/sud03-strategoxtorg.pdf))

15:00 Break

15:15 Optimization (chair: Otto Bagge)

-   Compiling Octave \-- Karina Olmos
    ([slides](ftp://ftp.stratego-language.org/pub/stratego/SUD03/sud03-octave.pdf))
-   Loop Optimization for [AutoBayes](AutoBayes){.twikiLink} \-- Jozef
    Kruger
    ([slides](ftp://ftp.stratego-language.org/pub/stratego/SUD03/sud03-loopfusion.sxi))
-   Core Simplification for the Helium Compiler \-- Alan van Dam
    ([slides](ftp://ftp.stratego-language.org/pub/stratego/SUD03/sud03-hsopt.pdf))

Generation (chair: Eelco Visser)

-   Template-based Application Generation \-- Jonne van Wijngaarden
    ([slides](ftp://ftp.stratego-language.org/pub/stratego/SUD03/sud03-templates.pdf))
-   [MetaTiger](../Tiger/MetaTiger){.twikiLink} \-- Robert Anisko
    ([slides](ftp://ftp.stratego-language.org/pub/stratego/SUD03/sud03-metatiger.pdf))

17:30 Discussion

19:00 Dinner

-   In Café restaurant TOQUE TOQUE\
    Oudegracht 138\
    3511 AA Utrecht\
    Tel: 030-2318787\
    Fax: 030-2317610\
    <http://www.toque.nl/>

### []{#Registered_Participants} Registered Participants

1.  Andres Loeh (UU) \[lunch, not dinner\]
2.  Akim Demaille (Epita) \[lunch, dinner\]
3.  Alan van Dam (UU) \[lunch, not dinner\]
4.  Alexey Rodriguez (UU) \[lunch, not dinner\]
5.  Armijn Hemel (UU) \[lunch, not dinner\]
6.  Arthur van Dam (UU) \[lunch, not dinner\]
7.  Clement Vasseur (Epita) \[lunch, dinner\]
8.  Dave Clarke (UU) \[lunch, not dinner\]
9.  Eelco Dolstra (UU) \[lunch, dinner\]
10. Eelco Visser (UU) \[lunch, dinner\]
11. Gordon Cichone (Dresden) \[lunch, dinner\]
12. Johan Jeuring (UU) \[after lunch, not dinner\]
13. Jonne van Wijngaarden (UU) \[lunch, dinner\]
14. Jory van Zessen (UU) \[lunch, not dinner\]
15. Jozef Kruger (UU) \[lunch, dinner\]
16. Jurgen Vinju (CWI) \[lunch, not dinner\]
17. Karina Olmos (UU) \[lunch, dinner\]
18. Martin Bravenboer (UU) \[lunch, dinner\]
19. Merijn de Jonge (TUE) \[lunch, not dinner\]
20. Niels Janssen (UU) \[lunch, not dinner\]
21. Otto Skrove Bagge (Bergen) \[lunch, dinner\]
22. Robert Anisko (Epita) \[lunch, dinner\]
23. Valentin David (Epita) \[lunch, dinner\]
24. Wilco Niessen (UU) \[until lunch, not dinner\]

### []{#Important_Dates} Important Dates

-   Deadline for registration: May 25, 2003
-   Users Day: June 5, 2003

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
