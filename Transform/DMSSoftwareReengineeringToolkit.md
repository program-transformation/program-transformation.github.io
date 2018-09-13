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
    Page](http://www.program-transformation.org/edit/Transform/DMSSoftwareReengineeringToolkit?t=1536825822)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DMSSoftwareReengineeringToolkit)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DMSSoftwareReengineeringToolkit)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DMSSoftwareReengineeringToolkit?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DMSSoftwareReengineeringToolkit?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Transform/DMSSoftwareReengineeringToolkit?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/DMSSoftwareReengineeringToolkit?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Transform/DMSSoftwareReengineeringToolkit?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/DMSSoftwareReengineeringToolkit?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/DMSSoftwareReengineeringToolkit?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/DMSSoftwareReengineeringToolkit?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DMSSoftwareReengineeringToolkit)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DMSSoftwareReengineeringToolkit?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Transform/DMSSoftwareReengineeringToolkit?template=oopsmore&param1=1.7&param2=1.7)
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
DMSSoftware Reengineering Toolkit {#dmssoftware-reengineering-toolkit .twikiTopicTitle}
=================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Homepage:** <http://www.semdesigns.com/Products/DMS/DMSToolkit.html>

[DMSSoftwareReengineeringToolkit](DMSSoftwareReengineeringToolkit){.twikiLink}
is a
[DesignMaintenanceSystem[^?^](http://www.program-transformation.org/edit/Transform/DesignMaintenanceSystem?topicparent=Transform.DMSSoftwareReengineeringToolkit)]{.twikiNewLink
style="background : #FFFFCE;"} for software
[ReEngineering](ReEngineering){.twikiLink} from
[SemanticDesigns](SemanticDesigns){.twikiLink}.

DMS provides generalized compiler technology for automating custom
analysis, modification, and generation of large software system sources.
It includes:

-   [UNICODE](UNICODE){.twikiLink}-based lexer generator. DMS lexers
    capture binary values of lexemes, all comments, and source file
    positioning information. Support is provided for INCLUDE files and
    other preprocessor issues.
-   Context-free GLR parser generator. Automatic construction of
    Abstract (not concrete) syntax trees (AST). Handling of local and
    conventional ambiguities. Parse-time semantic checking is possible.
-   Pretty printer generator. DMS prettyprinters can pretty-print ASTs
    according to custom prettyprinting rules, or \"fidelity\" print,
    preserving as much of the original formatting as possible.
-   Multi-pass attribute evaluator generator. Attributes computed from
    one pass are available in following passes. Attribute evaluation
    occurs in parallel, based on data dependencies.
-   Symbol table support for both conventional and unusual scoping
    rules.
-   Surface-syntax pattern and rewrite rule specification.
    Patterns/rewrites written in the notation of the target language, or
    in both source and target notations if different languages.
    Conditional rewriting, with optional procedural attachment. Optional
    procedural attachment for Right-hand-side construction. Pattern and
    ruleset compositions.
-   Associative/Commutative rewrite engine.
-   Scalable foundations Paralell execution based symmetric
    multiprocessing in [PARLANSE](PARLANSE){.twikiLink}, Semantic
    Design\'s parallel language for symbolic execution. Handles tens of
    thousands of files comprising several million lines on Windows NT
    4.0 or Windows 2000 platforms

A number of legacy languages have been predefined for use with DMS.

-   ANSI C and C++, with a built in preprocessor.
-   [COBOL](COBOL){.twikiLink} (ANSI 85/IBM VS II) with built in
    preprocessor
-   Java 2.0
-   C\#
-   [HTML](HTML){.twikiLink} 4.0, XHTML, Internet Explorer dialect
-   PHP
-   ISO Pascal and (Borland)
    [ObjectPascal[^?^](http://www.program-transformation.org/edit/Transform/ObjectPascal?topicparent=Transform.DMSSoftwareReengineeringToolkit)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   Ada83/95
-   Fortran77/90/95
-   ECMAScript (aka
    [JavaScript[^?^](http://www.program-transformation.org/edit/Transform/JavaScript?topicparent=Transform.DMSSoftwareReengineeringToolkit)]{.twikiNewLink
    style="background : #FFFFCE;"})
-   [XML](XML){.twikiLink}
-   Verilog
-   VHDL
-   others\...

**See also**

-   [IraBaxter](IraBaxter){.twikiLink}
-   [Branch Coverage For Arbitrary Languages Made
    Easy](BranchCoverageForArbitraryLanguagesMadeEasy){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.DMSSoftwareReengineeringToolkit moved from
Transform.DMSToolkit on 18 Mar 2002 - 15:42 by
[TWikiGuest](../Main/TWikiGuest){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Transform/DMSSoftwareReengineeringToolkit?newweb=Transform&newtopic=DMSToolkit&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
