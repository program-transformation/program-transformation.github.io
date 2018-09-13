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
    Page](http://www.program-transformation.org/edit/Transform/ProgramRefactoring?t=1536825742)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ProgramRefactoring)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ProgramRefactoring)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ProgramRefactoring?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ProgramRefactoring?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    20](http://www.program-transformation.org/view/Transform/ProgramRefactoring?rev=1.20)
    [(diff 19)](http://www.program-transformation.org/rdiff/Transform/ProgramRefactoring?rev1=1.20&rev2=1.19)
-   [Rev
    19](http://www.program-transformation.org/view/Transform/ProgramRefactoring?rev=1.19)
    [(diff 18)](http://www.program-transformation.org/rdiff/Transform/ProgramRefactoring?rev1=1.19&rev2=1.18)
-   [Rev
    18](http://www.program-transformation.org/view/Transform/ProgramRefactoring?rev=1.18)
    [(diff 17)](http://www.program-transformation.org/rdiff/Transform/ProgramRefactoring?rev1=1.18&rev2=1.17)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ProgramRefactoring)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ProgramRefactoring?template=oopsmore&param1=1.20&param2=1.20)
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
    \...](http://www.program-transformation.org/oops/Transform/ProgramRefactoring?template=oopsmore&param1=1.20&param2=1.20)
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
Program Refactoring {#program-refactoring .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Definition**

[Refactoring](Refactoring){.twikiLink} is typically applied at the level
of programs (i.e., source code). A program refactoring is a [program
transformation](ProgramTransformation){.twikiLink} that improves the
design of a program while preserving its behaviour.
[MartinFowler](MartinFowler){.twikiLink} defines a **refactoring** as:

-   *a change made to the internal structure of software to make it
    easier to understand and cheaper to modify without changing its
    observable behavior*

He then continues to define the verb **to refactor** as

-   *to restructure software by applying a series of refactorings
    without changing its observable behavior*.

Refactoring is an important component of the [Extreme
Programming](XP){.twikiLink} software engineering methodology. In this
context, refactorings are often associated with:

-   many small changes applied repeatedly
-   a catalog of widely discussed changes
-   explicit unit tests applied before and after each minimal change
-   interactive, perhaps tool-supported, but not automated.

------------------------------------------------------------------------

### []{#Tools} Tools

The following indicative list of refactoring tools is inevitable
incomplete but gives a clear idea about the diversity of tools for
refactoring available. For a more up to date list of refactoring tools,
we refer to the Google Web Directory on [Code
Refactoring](http://directory.google.com/Top/Computers/Programming/Languages/Java/Development_Tools/Code_Refactoring/?il=1)

**JavaLanguage**

-   [IDEA](http://www.intellij.com/idea/)
-   [Transmogrify](http://transmogrify.sourceforge.net)
-   [JRefactory](http://jrefactory.sourceforge.net)
-   [jFactor](http://www.instantiations.com/jfactor/)
-   [RECODER](http://recoder.sourceforge.net)
-   [InjectJ](http://injectj.fzi.de)
-   [Eclipse](http://www.eclipse.org/)
-   [RefactorIt](http://www.refactorit.com/)

**Smalltalk**

-   [Smalltalk Refactoring
    Browser](http://st-www.cs.uiuc.edu/~brant/Refactory/RefactoringBrowser.html)

**Special Refactoring Tools**

Tools for carrying out specific refactorings have been built over the
years. Commercial tools for restructuring spaghetti code in
[COBOL](COBOL){.twikiLink} and FORTRAN have been available since the
late 1970s. There are reputed to be tools that will restructure C
programs and headers to use minimal numbers of INCLUDEs. Specific tools
include:

-   [CloneDR](http://www.semdesigns.com/Products/Clone/index.html) -
    Finds (and possibly removes) redundant source code

------------------------------------------------------------------------

### []{#Resources} Resources

A more extensive and up to date list of [software refactoring
literature](http://staff.umh.ac.be/Mens.Tom/resources/refactoringPapers.html)
is available.

**Books**

-   [MartinFowler](MartinFowler){.twikiLink}. [Refactoring: Improving
    the Design of Existing
    Code](RefactoringImprovingTheDesignOfExistingCode){.twikiLink},
    Addison-Wesley, 1999. This book presents a catalog of refactorings
    on [Java programs](JavaLanguage){.twikiLink}. The [refactoring
    catalog](http://www.refactoring.com/catalog/) is also available
    online.

**Surveys**

-   [TomMens](TomMens){.twikiLink},
    [TomTourwe[^?^](http://www.program-transformation.org/edit/Transform/TomTourwe?topicparent=Transform.ProgramRefactoring)]{.twikiNewLink
    style="background : #FFFFCE;"}. [A survey on software
    refactoring](http://csdl.computer.org/comp/trans/ts/2004/02/e0126abs.htm),
    Transactions on Software Engineering, [IEEE](IEEE){.twikiLink}
    Computer Society Press, February 2004.

**PhD Theses**

-   Sander Tichelaar. Modeling Object-Oriented Software for Reverse
    Engineering and Refactoring. University of Bern, 2001.
-   Don Bradley Roberts. Practical Analysis for Refactoring. University
    of Illinois at Urbana-Champaign, 1999.
-   William F. Opdyke. Refactoring: A Program Restructuring Aid in
    Designing Object-Oriented Application Frameworks. University of
    Illinois at Urbana-Champaign, 1992.
-   William G. Griswold. Program Restructuring as an Aid to Software
    Maintenance. University of Washington, August 1991.

**Useful links**

-   <http://www.refactoring.com>: the refactoring site maintained by
    [MartinFowler](MartinFowler){.twikiLink}.
-   <http://c2.com/cgi/wiki?WikiPagesAboutRefactoring>: an extensive
    list of all the refactoring pages at the Wiki of
    [WardCunningham[^?^](http://www.program-transformation.org/edit/Transform/WardCunningham?topicparent=Transform.ProgramRefactoring)]{.twikiNewLink
    style="background : #FFFFCE;"}.
-   [Google Web Directory on
    Refactoring](http://directory.google.com/Top/Computers/Programming/Methodologies/Refactoring/)

------------------------------------------------------------------------

### []{#Research_Projects} Research Projects

-   [Language Parametric Program
    Restructuring](http://www.cs.vu.nl/lppr/), a research project by
    [RalfLaemmel](RalfLaemmel){.twikiLink}
-   [Refactoring Functional
    Programs](http://www.cs.kent.ac.uk/projects/refactor-fp/), a
    research project by
    [SimonThompson[^?^](http://www.program-transformation.org/edit/Transform/SimonThompson?topicparent=Transform.ProgramRefactoring)]{.twikiNewLink
    style="background : #FFFFCE;"} and
    [ClausReinke[^?^](http://www.program-transformation.org/edit/Transform/ClausReinke?topicparent=Transform.ProgramRefactoring)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [Formal Foundations of Software
    Refactoring](http://win-www.uia.ac.be/u/lore/refactoringProject/index.php),
    a research project by [TomMens](TomMens){.twikiLink},
    [SergeDemeyer[^?^](http://www.program-transformation.org/edit/Transform/SergeDemeyer?topicparent=Transform.ProgramRefactoring)]{.twikiNewLink
    style="background : #FFFFCE;"} and
    [DirkJanssens[^?^](http://www.program-transformation.org/edit/Transform/DirkJanssens?topicparent=Transform.ProgramRefactoring)]{.twikiNewLink
    style="background : #FFFFCE;"}.

------------------------------------------------------------------------

### []{#Events} Events

-   [The First International Workshop on Refactoring: Achievements,
    Challenges, Effects](http://swen.uwaterloo.ca/~reface03/)
    (REFACE03), November 2003
-   [Graph Transformation for
    Refactoring](http://www.fots.ua.ac.be/graphtransfo_refactoring/),
    April 2004

------------------------------------------------------------------------

### []{#People} People

-   [MartinFowler](MartinFowler){.twikiLink}
-   [ChrisSeguin[^?^](http://www.program-transformation.org/edit/Transform/ChrisSeguin?topicparent=Transform.ProgramRefactoring)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [DonRoberts](DonRoberts){.twikiLink}
-   [RalfLaemmel](RalfLaemmel){.twikiLink} is working on *generic
    refactoring*: language-independent refactorings
-   [SimonThompson[^?^](http://www.program-transformation.org/edit/Transform/SimonThompson?topicparent=Transform.ProgramRefactoring)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [ClausReinke[^?^](http://www.program-transformation.org/edit/Transform/ClausReinke?topicparent=Transform.ProgramRefactoring)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [TomMens](TomMens){.twikiLink}
-   [SergeDemeyer[^?^](http://www.program-transformation.org/edit/Transform/SergeDemeyer?topicparent=Transform.ProgramRefactoring)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [DirkJanssens[^?^](http://www.program-transformation.org/edit/Transform/DirkJanssens?topicparent=Transform.ProgramRefactoring)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [TomTourwe[^?^](http://www.program-transformation.org/edit/Transform/TomTourwe?topicparent=Transform.ProgramRefactoring)]{.twikiNewLink
    style="background : #FFFFCE;"}

------------------------------------------------------------------------

[CategoryTransformationParadigm](CategoryTransformationParadigm){.twikiLink}
\| [CategoryReengineeringPages](CategoryReengineeringPages){.twikiLink}
\| [CategorySoftwareEvolution](CategorySoftwareEvolution){.twikiLink} \|
Contributors: [EelcoVisser](../Main/EelcoVisser){.twikiLink},
[ArieVanDeursen](../Main/ArieVanDeursen){.twikiLink},
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink},
[TomMens](../Main/TomMens){.twikiLink} - 5 April 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
