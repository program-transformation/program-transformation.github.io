::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

[![](../pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Transform/RuleWorkshopProposal?t=1536826559)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/RuleWorkshopProposal)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/RuleWorkshopProposal)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/RuleWorkshopProposal?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/RuleWorkshopProposal?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    13](http://www.program-transformation.org/view/Transform/RuleWorkshopProposal?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/Transform/RuleWorkshopProposal?rev1=1.13&rev2=1.12)
-   [Rev
    12](http://www.program-transformation.org/view/Transform/RuleWorkshopProposal?rev=1.12)
    [(diff 11)](http://www.program-transformation.org/rdiff/Transform/RuleWorkshopProposal?rev1=1.12&rev2=1.11)
-   [Rev
    11](http://www.program-transformation.org/view/Transform/RuleWorkshopProposal?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/Transform/RuleWorkshopProposal?rev1=1.11&rev2=1.10)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/RuleWorkshopProposal)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/RuleWorkshopProposal?template=oopsmore&param1=1.13&param2=1.13)
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
    \...](http://www.program-transformation.org/oops/Transform/RuleWorkshopProposal?template=oopsmore&param1=1.13&param2=1.13)
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
Rule Workshop Proposal {#rule-workshop-proposal .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Name of the workshop**

[Workshop on Rule Based
Programming](WorkshopOnRuleBasedProgramming){.twikiLink}
([RULE](RULE){.twikiLink})

Associated with [PPDP](PPDP){.twikiLink}

**The goals of the workshop**

The rule-based programming paradigm is characterized by the repeated,
localized transformation of a shared data object such as a term, graph,
proof, or constraint store. The transformations are described by *rules*
which separate the description of the sub-object to be replaced (the
*pattern*) from the calculation of the replacement. Optionally, rules
can have further conditions that restrict their applicability. The
transformations are controlled by explicit or implicit *strategies*.

The basic concepts of rule-based programming appear throughout computer
science, from theoretical foundations to practical implementations.
[Term rewriting](TermRewriting){.twikiLink} is used in semantics in
order to describe the meaning of programming languages, as well as in
the implementation of [program
transformation](ProgramTransformation){.twikiLink} systems. It is used
implicitly or explicitly to perform computations, e.g., in Mathematica,
OBJ, or [ELAN](ELAN){.twikiLink}, or to perform deductions, e.g., by
using inference rules to describe or implement a logic, theorem prover
or constraint solver. Extreme examples of rule-based programming include
the mail system in Unix which uses rules in order to rewrite mail
addresses to canonical forms, or the transition rules used in model
checkers.

Rule-based programming is currently experiencing a renewed period of
growth with the emergence of new concepts and systems that allow a
better understanding and better usability. On the theoretical side,
after the in-depth study of rewriting concepts during the eighties, the
nineties saw the emergence of the general concepts of rewriting logic
and of the rewriting calculus. On the practical side, new languages such
as ASM, [ASF+SDF](ASFandSDF){.twikiLink}, Claire,
[ELAN](ELAN){.twikiLink}, Maude, and
[Stratego](../Stratego/StrategoLanguage){.twikiLink}, new systems such
as [LRR](LRR){.twikiLink} and commercial products such as [Ilog
Rules](IlogRules){.twikiLink} and [Eclipse](EclipseLanguage){.twikiLink}
have shown that rules are a useful programming tool.

The practical application of rule-based programming prompts research
into the algorithmic complexity and optimization of rule-based programs
as well as into the expressivity, semantics and implementation of
rules-based languages. Here, a particular focus is the use and
specification of strategies as a high-level control flow concept for the
application of the rules.

The purpose of this workshop is to bring together researchers from the
various communities working on rule-based programming to foster
fertilisation between theory and practice, as well as to favour the
growth of this programming paradigm.

**Topics**

-   Languages for rule-based programming
    -   Expressivity
    -   Semantics
    -   Implementation techniques
-   Applications of rule-based programming
    -   Analysis of rule-based programs
    -   Programming methods
-   System descriptions

**Names and addresses of organizers**

-   Bernd Fischer\
    Automated Software Engineering Group, USRA/RIACS, NASA Ames Research
    Center, M/S 269-2\
    Moffett Field, CA 94035, USA\
    Phone: +1(650)604-2977\
    mail:fisch\@email.arc.nasa.gov\
    <http://ase.arc.nasa.gov/people/fischer>

<!-- -->

-   Eelco Visser\
    Institute of Information and Computing Sciences, Universiteit
    Utrecht\
    P.O. Box 80089, 3508 TB Utrecht, The Netherlands\
    Phone: +31-30-253 4592\
    Fax: +31-30-251 3791\
    mail:visser\@acm.org\
    <http://www.cs.uu.nl/~visser/>

**Names of potential participants, such as program committee members**

-   [Mark van den Brand](MarkVanDenBrand){.twikiLink}
-   [Bernd Fischer](BerndFischer){.twikiLink}
-   [Claude Kirchner](ClaudeKirchner){.twikiLink}
-   [Herbert Kuchen](HerbertKuchen){.twikiLink}
-   [Mark Minas](MarkMinas){.twikiLink}
-   [Eelco Visser](EelcoVisser){.twikiLink}
-   PC-members from
    [RCoRP[^?^](http://www.program-transformation.org/edit/Transform/RCoRP?topicparent=Transform.RuleWorkshopProposal)]{.twikiNewLink
    style="background : #FFFFCE;"} workshop (TBD)

**Plans for call for participation (e.g., call for papers)**

-   Preliminary call for papers: December 2001 / January 2002
-   Call for papers: February 2002
-   Call for participation / Final call for papers: June 1, 2002
-   Submission deadline: June 15, 2002
-   Notification of acceptance: August 15, 2002
-   Camera-ready version: September 15, 2002

**Important related dates**

[ICFP](ICFP){.twikiLink}:

-   Submission deadline: 21 March 2002
-   Notification of acceptance or rejection: 14 May 2002
-   Conference: October 4-6, 2002

[PPDP](PPDP){.twikiLink}:

-   Submission deadline: 21 March 2002
-   Notification of acceptance or rejection: 30 May 2002
-   Conference: October 6-8, 2002

**Invited Speaker**

-   [Paul Haley](PaulHaley){.twikiLink} (to be confirmed)

**Workshop-Schedule**

**Expected number of attendees**

-   20-25

**Plans for publicity**

mailinglists

-   amast
-   eapls
-   seworld
-   list of former [RULE](RULE){.twikiLink} participants / PC-members
-   list of former
    [RCoRP[^?^](http://www.program-transformation.org/edit/Transform/RCoRP?topicparent=Transform.RuleWorkshopProposal)]{.twikiNewLink
    style="background : #FFFFCE;"} participants / PC-members

newsgroups

-   comp.ai
-   comp.compilers
-   comp.lang.functional
-   comp.lang.prolog
-   comp.software-eng

**Plans for a proceedings**

-   Printed participants proceedings (Utrecht University Technical
    Report)
-   Post-conference publication in ENTCS

**Past Events**

RULE\'01

-   Date: September 4, 2001
-   Site: Florence, Italy (affiliated with [PLI](PLI){.twikiLink} 2001)
-   Organizers: [Mark van den Brand](MarkVanDenBrand){.twikiLink},
    [Rakesh Verma](RakeshVerma){.twikiLink}
-   Submissions/accepts: 11 / 11
-   Attendance: 20
-   Registration fees: \$65
-   Budget: \$150 for the proceedings
-   URL: <http://www.cwi.nl/~markvdb/RULE2001/>

RULE\'00

-   Date: Sep. 19, 2000
-   Site: Montreal
-   Organizers: Nachum Dershowitz and [Claude
    Kirchner](ClaudeKirchner){.twikiLink}
-   Submissions/accepts: 13/11
-   Attendance: 21
-   Registration fees: see <http://www.cs.yorku.ca/pli00/>
-   Budget: just the proceedings
-   [URL](URL){.twikiLink}: <http://www.loria.fr/~ckirchne/=rule2000/>

**URL address of the workshop description**

-   <http://www.program-transformation.org/rule02>

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
