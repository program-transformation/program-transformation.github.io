::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[WGLD](http://www.program-transformation.org/view/WGLD/WebHome)**

------------------------------------------------------------------------

-   [Home](WebHome){.twikiLink}
-   [IFIP Proposal](Proposal){.twikiLink}
-   [Members](GroupMembers){.twikiLink}
-   [Meetings](Meetings){.twikiLink}

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
    Page](http://www.program-transformation.org/edit/WGLD/MeetingProceedings2014?t=1536829034)
-   [Rename
    Page](http://www.program-transformation.org/rename/WGLD/MeetingProceedings2014)
-   [Attach
    File](http://www.program-transformation.org/attach/WGLD/MeetingProceedings2014)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/WGLD/MeetingProceedings2014?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/WGLD/MeetingProceedings2014?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/WGLD/MeetingProceedings2014?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/WGLD/MeetingProceedings2014?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/WGLD/MeetingProceedings2014?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/WGLD/MeetingProceedings2014?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/WGLD/MeetingProceedings2014?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/WGLD/MeetingProceedings2014)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/WGLD/MeetingProceedings2014?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/WGLD/MeetingProceedings2014?template=oopsmore&param1=1.3&param2=1.3)
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
Meeting Proceedings 2014 {#meeting-proceedings-2014 .twikiTopicTitle}
========================

::: {.twikiWebTitle}
Working Group on Language Design
:::

These are the talks given at the [IFIP WG 1.16 meeting at Skamania
Lodge](Meeting2014){.twikiLink}, WA, USA from June 2 to June 6, 2014.

[]{#Sean_McDirmid_Programming_with_M} Sean McDirmid: Programming with Managed Time in Glitch
--------------------------------------------------------------------------------------------

Most programming languages expose the hardware\'s ability to update
global state at any time, leaving programmers to carefully coordinate
state updates; an especially tricky task for reactive, concurrent,
incremental, or iterative behaviors. As observed by Jonathan Edwards,
just as languages runtimes now liberate us from meticulously allocating
and freeing memory, they could also properly order state updates for us.
In this spirit, we propose a new programming model, Glitch, where all
updates between external events appear to execute simultaneously through
a combination of incremental replay and update rollback. Programs in
Glitch are then immediately responsive to event-induced changes, are
iterative without extra logic, and are deterministic in their
concurrency. By rationalizing state update, program executions in Glitch
can also be replayed in an IDE, and can be revised incrementally under
arbitrary code changes.

[]{#Mads_Torgersen_Opening_up_C}[]{#Mads_Torgersen_Opening_up_C_} Mads Torgersen: Opening up C\#
------------------------------------------------------------------------------------------------

The C\# team is changing its ways: the C\# compiler is rewritten (in
C\#) with a public API that is immutable, efficient, detailed and
full-fidelity. The whole compiler code base is open source. Language
design notes are public -- everyone gets to see how the sausage is made.
In the talk I'll give the lay of the land and see where the discussion
goes. One interesting aspect is whether this codebase is interesting for
teaching: the industry has come a long way since the dragon book.

[]{#Jonathan_Edwards_Two_way_Dataflo} Jonathan Edwards: Two-way Dataflow
------------------------------------------------------------------------

Subtext is an experiment in radical simplification of application
programming. The goal is to combine the power of frameworks like Rails
and iOS with the simplicity of a spreadsheet. Mutable state is a
notorious source of complexity in application programming and indeed has
long been a central concern in programming language design. I propose a
new approach called two-way dataflow which breaks the program into
cyclic output and input phases. Output is handled with a form of pure
lazy functional programming. Input is governed by a new semantics called
one-way action which is a highly restricted form of event-driven
imperative programming. Two-way dataflow has been designed not only to
simplify the semantics of imperative programming but also to allow a
representation in the IDE that, like a spreadsheet, provides a fully
WYSIWYG programming experience.

[]{#Adam_Chlipala_Separating_Functio} Adam Chlipala: Separating Functionality and Optimizations: A New Programming Paradigm Enabled by Formal Methods?
------------------------------------------------------------------------------------------------------------------------------------------------------

Programming language design has progressed largely through the invention
of new mechanisms for abstraction and modularity. We often expect our
languages to *enforce* modularity, rejecting programs that would break
abstraction boundaries. One important sort of modularity has largely
eluded us: separating the *functionality* of a program from the
*optimizations* that lead us to a performant enough implementation. To
understand a program, a reader must wade through optimizations that
obscure the underlying intent and structure. How might we get a
programming language to enforce correct schemes of separating
functionality and optimizations? Traditional modularity mechanisms
don\'t seem up to the challenge, considering the breadth of optimization
techniques that programmers feel compelled to apply in different
contexts.

I suggest that we use one of the strongest known modularity mechanisms:
formal (machine-checked) proof of adherence to specifications. A
well-designed specification language lets us say exactly what we mean to
say, in as few lines of code as possible. A well-designed proof system
gives us plenty of flexibility in demonstrating why a program module
meets its specification. These are the ingredients we need to support
language-enforced modularity between features and optimizations.

In particular, we are working on a system codenamed Fiat, a library
within the Coq proof assistant. The unifying metaphor is
correct-by-construction program refinement, an idea with a venerable
history in the world of program synthesis. The \"functionality\" part of
a program can be a program with some nondeterministic operations. Our
goal is to replace the nondeterminism with efficient code, in a
logically sound way called refinement. Any notation for writing down
refinement strategies constitutes the \"optimizations\" part of a
program; mistakes in it cannot lead to \"breaking the semantics\" of a
program, since Coq is checking each of our refinements, which must be
proved correct. I will demo some of our experiments so far, refining
SQL-style specifications into decently efficient functional programs.

[]{#Tom_van_Cutsem_The_rise_and_fall} Tom van Cutsem: The rise and fall (and rise?) of distributed programming languages
------------------------------------------------------------------------------------------------------------------------

Context/abstract: the 1970\'s and \'80s marked an era of innovation in
the domain of distributed programming languages. Innovative languages
such as Argus (Liskov et al), Emerald (Jul, Black et al), Occam (May,
Hoare et al), Erlang (Armstrong et al), Modula-3 (Cardelli et al), etc.
were all designed during those days. In the \'90s, with the emergence of
Java, we saw a shift toward so-called \"middleware\", such as Java RMI,
CORBA, etc. where most distributed systems concerns were no longer dealt
with in the programming language. Today, these object-oriented
middleware systems are in turn largely superseded by \"service-oriented
architectures\", web services or resource-oriented REST architectures.
Whatever happened to good old distributed programming languages? Have
they failed? If so, why? If not, why are they receiving so little
attention? What can we learn from the past to improve the future of
distributed programming abstractions?

[]{#James_Noble_Capabilities_Trust_a} James Noble: Capabilities, Trust, and Risk
--------------------------------------------------------------------------------

The Escrow Exchange Contract has been used as a case study of building
up complex and trustworthy systems from basic object capabilities, {in
the context of concurrent and distributed programming. I\'ll present a
Rational Reconstruction of the Escrow Exchange Contract case study,
expressed in Grace, concentrating on the most essential issues of
trustworthiness, and ignoring issues to do with distribution or more
complex protocols.

[Slides](http://program-transformation.org/pub/WGLD/CAPE14-WG2.16-v8.pdf)

[]{#Roberto_Ierusalimschy_OO_in_Lua}[]{#Roberto_Ierusalimschy_OO_in_Lua_} Roberto Ierusalimschy: OO in Lua (or DIY OO Systems)
------------------------------------------------------------------------------------------------------------------------------

Lua presents a very basic and simple class-based object-oriented model.
In this talk, I discuss how we can build rich prototype-based
object-oriented models on top of the original simple model.

[Slides](http://program-transformation.org/pub/WGLD/MeetingProceedings2014/ifip-2014.pdf)

\
[]{#TopicEnd}
:::

::: {.twikiAttachments}
  [I](http://www.program-transformation.org/WGLD/MeetingProceedings2014?sortcol=0&table=1&up=0#sorted_table "Sort by this column")   [Attachment](../TWiki/FileAttachment){.twikiLink} [![sort](../pub/TWiki/TablePlugin/diamond.gif)](http://www.program-transformation.org/WGLD/MeetingProceedings2014?sortcol=1&table=1&up=0#sorted_table "Sort by this column")   [Action](http://www.program-transformation.org/WGLD/MeetingProceedings2014?sortcol=2&table=1&up=0#sorted_table "Sort by this column")                                                [Size](http://www.program-transformation.org/WGLD/MeetingProceedings2014?sortcol=3&table=1&up=0#sorted_table "Sort by this column") [Date](http://www.program-transformation.org/WGLD/MeetingProceedings2014?sortcol=4&table=1&up=0#sorted_table "Sort by this column")   [Who](http://www.program-transformation.org/WGLD/MeetingProceedings2014?sortcol=5&table=1&up=0#sorted_table "Sort by this column")   [Comment](http://www.program-transformation.org/WGLD/MeetingProceedings2014?sortcol=6&table=1&up=0#sorted_table "Sort by this column")
  ---------------------------------------------------------------------------------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------ ----------------------------------------------------------------------------------------------------------------------------------------
  ![](../pub/icn/pdf.gif){width="16" height="16"}                                                                                    [CAPE14-WG2.16-v8.pdf](http://www.program-transformation.org/pub/WGLD/MeetingProceedings2014/CAPE14-WG2.16-v8.pdf)                                                                                                               [manage](http://www.program-transformation.org/attach/WGLD/MeetingProceedings2014?filename=CAPE14-WG2.16-v8.pdf&revInfo=1 "change, update, previous revisions, move, delete...")                                                                                                                                5777.6 K 14 Jun 2014 - 13:33                                                                                                                   [EelcoVisser](../Main/EelcoVisser){.twikiLink}                                                                                       James Noble
  ![](../pub/icn/pdf.gif){width="16" height="16"}                                                                                    [ifip-2014.pdf](http://www.program-transformation.org/pub/WGLD/MeetingProceedings2014/ifip-2014.pdf)                                                                                                                             [manage](http://www.program-transformation.org/attach/WGLD/MeetingProceedings2014?filename=ifip-2014.pdf&revInfo=1 "change, update, previous revisions, move, delete...")                                                                                                                                        121.8 K 11 Mar 2015 - 20:48                                                                                                                   [EelcoVisser](../Main/EelcoVisser){.twikiLink}                                                                                        
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
