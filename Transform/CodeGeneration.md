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
    Page](http://www.program-transformation.org/edit/Transform/CodeGeneration?t=1536825740)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/CodeGeneration)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/CodeGeneration)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/CodeGeneration?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/CodeGeneration?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Transform/CodeGeneration?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/CodeGeneration?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/CodeGeneration?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/CodeGeneration?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/CodeGeneration?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/CodeGeneration?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/CodeGeneration)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/CodeGeneration?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Transform/CodeGeneration?template=oopsmore&param1=1.6&param2=1.6)
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
Code Generation {#code-generation .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Code generation (also called [instruction
selection](InstructionSelection){.twikiLink}) is a [program
transformation](ProgramTransformation){.twikiLink} performed in the
back-ends of compilers. At this state of compilation [intermediate
representation[^?^](http://www.program-transformation.org/edit/Transform/IntermediateRepresentation?topicparent=Transform.CodeGeneration)]{.twikiNewLink
style="background : #FFFFCE;"} expressions are transformed into
sequences of machine code instructions.

### []{#Code_Generator_Generators} Code Generator Generators

-   [BURG](BURG){.twikiLink}: generate a
    [CodeGenerator](CodeGenerator){.twikiLink} from a tree grammar that
    describes declaratively how
    [IntermediateRepresentation[^?^](http://www.program-transformation.org/edit/Transform/IntermediateRepresentation?topicparent=Transform.CodeGeneration)]{.twikiNewLink
    style="background : #FFFFCE;"} expression patterns can be mapped to
    machine instructions.

<!-- -->

-   [The New Jersey Machine-Code
    Toolkit](http://www.eecs.harvard.edu/~nr/toolkit/)

<!-- -->

-   [vcode: a portable, very fast dynamic code generation
    system](http://www.pdos.lcs.mit.edu/~engler/pldi96-abstract.html)

<!-- -->

-   [Google: Computers \> Programming \> Compilers \> Code Generator
    Kits](http://directory.google.com/Top/Computers/Programming/Compilers/Code_Generator_Kits/)

### []{#Publications_about_Code_Generati} Publications about Code Generation

-   Aho A V, Ganapathi M, Tjiang S W K \"Code generation using tree
    matching and dynamic programming\", [TOPLAS](TOPLAS){.twikiLink} v11
    \#4, pp491-516, Oct 1989

<!-- -->

-   Christopher T W, Hatcher P J \"High quality code generation via
    bottom up tree pattern matching\" Proceedings of the 13th annual
    [ACM](ACM){.twikiLink} symposium on principles of programming
    languages, pp119-130, 1986

<!-- -->

-   Fraser C W, Wendt A L \"Automatic generation of fast optimizing code
    generators\" [SIGPLAN](SIGPLAN){.twikiLink} Not. v23 \#7, pp79-84,
    Jul. 1988

<!-- -->

-   Fraser C W \"A language for writing code generators\",
    [SIGPLAN](SIGPLAN){.twikiLink} Not. v24 \#7, pp238-245, Jul. 1987

<!-- -->

-   Schwartz R A, Yates J S \"Dynamic programming and industrial
    strength instruction selection: code generation by tiring but not
    exhaustive, search\" [SIGPLAN](SIGPLAN){.twikiLink} Not. v23 \#10,
    pp131-140, Oct. 1988

<!-- -->

-   [Martin Bravenboer](MartinBravenboer){.twikiLink} and [Eelco
    Visser](EelcoVisser){.twikiLink}. [Rewriting Strategies for
    Instruction
    Selection](../Stratego/RewritingStrategiesForInstructionSelection){.twikiLink}.
    In S. Tison, *Rewriting Techniques and Applications
    ([RTA](RTA){.twikiLink}\'02)*. Volume ? of Lecture Notes in Computer
    Science. Springer Verlag. Copenhagen, Denmark, July 2002.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 08 Jan 2002, 09 Jun
2002

------------------------------------------------------------------------

[CategoryTransformation](CategoryTransformation){.twikiLink} \|
[CategoryOptimization](CategoryOptimization){.twikiLink} \|
[ProgramOptimization](ProgramOptimization){.twikiLink} \| Contributions
by [EelcoVisser](../Main/EelcoVisser){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
