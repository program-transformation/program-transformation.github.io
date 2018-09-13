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
    Page](http://www.program-transformation.org/edit/Transform/ScannerlessGeneralizedLRParsing?t=1536826403)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ScannerlessGeneralizedLRParsing)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ScannerlessGeneralizedLRParsing)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ScannerlessGeneralizedLRParsing?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ScannerlessGeneralizedLRParsing?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/ScannerlessGeneralizedLRParsing?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/ScannerlessGeneralizedLRParsing?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/ScannerlessGeneralizedLRParsing?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/ScannerlessGeneralizedLRParsing?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/ScannerlessGeneralizedLRParsing?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ScannerlessGeneralizedLRParsing)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ScannerlessGeneralizedLRParsing?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/ScannerlessGeneralizedLRParsing?template=oopsmore&param1=1.3&param2=1.3)
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
Scannerless Generalized LRParsing {#scannerless-generalized-lrparsing .twikiTopicTitle}
=================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[EelcoVisser](EelcoVisser){.twikiLink}. **Scannerless Generalized-LR
parsing**. Technical Report P9707, Programming Research Group,
University of Amsterdam, July 1997.

-   Online: <http://www.cs.uu.nl/~visser/ftp/P9707.ps.gz>

**Abstract**

Current deterministic parsing techniques have a number of problems.
These include the limitations of parser generators for deterministic
languages and the complex interface between scanner and parser.
Scannerless parsing is a parsing technique in which lexical and
context-free syntax are integrated into one grammar and are all handled
by a single context-free analysis phase. This approach has a number of
advantages including discarding of the scanner and lexical
disambiguation by means of the context in which a lexical token occurs.
Scannerless parsing generates a number of interesting problems as well.
Integrated grammars do not fit the requirements of the conventional
deterministic parsing techniques. A plain context-free grammar formalism
leads to unwieldy grammars, if all lexical information is included.
Lexical disambiguation needs to be reformulated for use in context-free
parsing.

The scannerless generalized-LR parsing approach presented in this paper
solves these problems. Grammar normalization is used to support an
expressive grammar formalism without complicating the underlying
machinery. Follow restrictions are used to express longest match lexical
disambiguation. Reject productions are used to express the prefer
keywords rule for lexical disambiguation. The SLR(1) parser generation
algorithm is adapted to implement disambiguation by general priority and
associativity declarations and to interpret follow restrictions.
Generalized-LR parsing is used to provide dynamic lookahead and to
support parsing of arbitrary context-free grammars including ambiguous
ones. An adaptation of the GLR algorithm supports the interpretation of
grammars with reject productions.

**Further Reading**

-   [SDF2](../Sdf/WebHome){.twikiLink}
-   [Syntax Definition for Language
    Prototyping](SyntaxDefinitionForLanguagePrototyping){.twikiLink}
-   [Disambiguation filters for Scannerless Generalized LR
    Parsers[^?^](http://www.program-transformation.org/edit/Transform/DisambiguationFiltersForScannerlessGeneralizedLRParsers?topicparent=Transform.ScannerlessGeneralizedLRParsing)]{.twikiNewLink
    style="background : #FFFFCE;"}

------------------------------------------------------------------------

[CategoryPaper](CategoryPaper){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
