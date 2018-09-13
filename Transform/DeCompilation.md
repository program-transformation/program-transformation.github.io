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
    Page](http://www.program-transformation.org/edit/Transform/DeCompilation?t=1536825728)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DeCompilation)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DeCompilation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DeCompilation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DeCompilation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    83](http://www.program-transformation.org/view/Transform/DeCompilation?rev=1.83)
    [(diff 82)](http://www.program-transformation.org/rdiff/Transform/DeCompilation?rev1=1.83&rev2=1.82)
-   [Rev
    82](http://www.program-transformation.org/view/Transform/DeCompilation?rev=1.82)
    [(diff 81)](http://www.program-transformation.org/rdiff/Transform/DeCompilation?rev1=1.82&rev2=1.81)
-   [Rev
    81](http://www.program-transformation.org/view/Transform/DeCompilation?rev=1.81)
    [(diff 80)](http://www.program-transformation.org/rdiff/Transform/DeCompilation?rev1=1.81&rev2=1.80)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DeCompilation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DeCompilation?template=oopsmore&param1=1.83&param2=1.83)
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
    \...](http://www.program-transformation.org/oops/Transform/DeCompilation?template=oopsmore&param1=1.83&param2=1.83)
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
The Decompilation Wiki {#the-decompilation-wiki .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Decompilation is a
[ProgramTransformation](ProgramTransformation){.twikiLink} by which a
high-level source code for an executable program is discovered.
Decompilation is the inverse of
[ProgramCompilation](ProgramCompilation){.twikiLink}.

Decompilation techniques were initially used in the 1960s to aid in the
migration of programs from one platform to another. Since then,
decompilation techniques have been used to aid in the recovery of lost
source code, debugging of programs, locating of viruses, comprehending
programs, recovery of high-level views of programs, and more; see
[WhyDecompilation](WhyDecompilation){.twikiLink}.

### []{#Introduction} Introduction

-   The [LegalityOfDecompilation](LegalityOfDecompilation){.twikiLink}
    and [legal issues](LegalIssues){.twikiLink} of [reverse
    engineering](ReverseEngineering){.twikiLink}
-   [Is it possible?](DecompilationPossible){.twikiLink}
-   [Why Decompilation](WhyDecompilation){.twikiLink}?
-   [History Of Decompilation 1](HistoryOfDecompilation1){.twikiLink}
    (1960-1979)
-   [History Of Decompilation 2](HistoryOfDecompilation2){.twikiLink}
    (1980-1999)
-   [History Of Decompilation 3](HistoryOfDecompilation3){.twikiLink}
    (2000-present)
-   The [Decompilation Process](DecompilationProcess){.twikiLink}
-   [Decompilation And Reverse
    Engineering](DecompilationAndReverseEngineering){.twikiLink}

### []{#Decompilers} Decompilers

Decompilers are categorised by the types of programs that they will
decompile. A decompiler might not emit code in the same language that
the original program was written in.

-   [Machine code](MachineCodeDecompilers){.twikiLink}
-   [Assembly language](AssemblyDecompilers){.twikiLink}
-   [Delphi](DelphiDecompilers){.twikiLink}
-   [Visual Basic](VisualBasicDecompilers){.twikiLink}
-   [Java bytecodes](JavaDecompilers){.twikiLink}
-   [.NET bytecodes](DotNetDecompilers){.twikiLink}
-   [Python bytecodes](PythonDecompilers){.twikiLink}
-   [Foxbase/FoxPro](FoxbaseDecompilers){.twikiLink}
-   [Specific compiler generated
    programs](DecompilationCompilerSpecific){.twikiLink}

### []{#Services_offered_and_wanted} Services offered and wanted

-   [Companies Offering Decompilation
    Services](CompaniesOfferingDecompilationServices){.twikiLink}
-   [Decompilation Help Wanted](DecompilationHelpWanted){.twikiLink}
-   I want an [Automatic Decompiler](AutomaticDecompiler){.twikiLink}

### []{#Related_Areas} Related Areas

-   [Disassembly](DisAssembly){.twikiLink}
-   [Binary Translation](BinaryTranslation){.twikiLink}
-   [Program Obfuscation](ProgramObfuscation){.twikiLink}
-   [Tamper Resistant Software](TamperResistantSoftware){.twikiLink}

### []{#Theory} Theory

-   Machine code patterns that are [Impossible To
    Decompile](ImpossibleToDecompile){.twikiLink} automatically
-   Why [user interaction](DecompilerInteraction){.twikiLink} might be
    needed

### []{#Recently_changed_pages} Recently changed pages

-   [Anatomizer Decompiler Test](AnatomizerDecompilerTest){.twikiLink}
-   [Decompiler Interaction](DecompilerInteraction){.twikiLink}
-   A [refutation](BobStoutRefutation){.twikiLink} of [Bob Stout\'s FAQ
    on decompilation](BobStoutOnDecompilation){.twikiLink}

### []{#Other} Other

-   [DecompilationResources](DecompilationResources){.twikiLink}
    (peripherally related)
-   For a site map, see
    [CategoryDecompilation](CategoryDecompilation){.twikiLink}
-   [Referencing](ReferencingDecompilationWikiPages){.twikiLink} these
    pages
-   [About](AboutDecompilation){.twikiLink} these pages

                                                                                            [Please feel free to keep these pages up to date!](DeCompilation@sortcol=0&table=1&up=0#sorted_table "Sort by this column")
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   Just select Edit from the Page menu near the top of every page. However, you do need to [register](../TWiki/TWikiRegistration){.twikiLink} and to become a member of the [Transform Group](../Main/TransformGroup){.twikiLink} now; see [AboutDecompilation](AboutDecompilation){.twikiLink} for more details.

[CategoryDecompilation](CategoryDecompilation){.twikiLink} \|
[CategoryReverseEngineering](CategoryReverseEngineering){.twikiLink} \|
[CategoryEntryPoint](CategoryEntryPoint){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
