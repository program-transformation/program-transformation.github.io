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
    Page](http://www.program-transformation.org/edit/Transform/IslandGrammars?t=1536826499)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/IslandGrammars)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/IslandGrammars)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/IslandGrammars?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/IslandGrammars?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Transform/IslandGrammars?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/IslandGrammars?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/IslandGrammars?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/IslandGrammars?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/IslandGrammars?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/IslandGrammars?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/IslandGrammars)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/IslandGrammars?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Transform/IslandGrammars?template=oopsmore&param1=1.6&param2=1.6)
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
Island Grammars {#island-grammars .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Description**

An *island grammar* only precisely defines small portions of the syntax
of a language. The rest of the syntax is defined imprecisely, for
instance as a list of characters, or a list of tokens.

-   In
    [BuildingDocumentationGenerators](BuildingDocumentationGenerators){.twikiLink},
    we have described an Island Grammar as consisting of
    1.  detailed productions for the language constructs we are
        specifically interested in
    2.  liberal productions catching all remaining constructs; and
    3.  a minimal set of general definitions covering the overall
        structure of a program. \-- *ArieVanDeursen*

**Examples**

From *AQuickIntroductionToSDF*:

       module Message
         exports
          syntax
          Msg   -> <START>
          X*    -> Msg
          ~[]   -> X {avoid}

       module Mailaddress
         exports
          syntax
          Segment "@" Hostname     -> X
          [A-Za-z][A-Za-z0-9\-\_]* -> Segment
          {Segment "."}+           -> Hostname

Thus, this grammar gives a precise syntax definition only for mail
addresses (the *islands*), and describes the rest of a message as a list
of arbitrary characters (the *sea*).

**Purpose**

The purposes of [IslandGrammars](IslandGrammars){.twikiLink} are the
following:

-   *Faster parsing*: the grammar is smaller, and contains less (local)
    ambiguities (hopefully).
-   *More robust parsing*: an island grammar is less dependent of
    language changes or differences between dialects than a regular,
    precise one.
-   *Ignorant parsing*: full knowledge of the syntax of a given language
    is not required to parse it.

------------------------------------------------------------------------

**Discussion**

I have some quesions:

-   Does anyone have more examples of
    [IslandGrammars](IslandGrammars){.twikiLink}?
-   Is there evidence that parsing with
    [IslandGrammars](IslandGrammars){.twikiLink} can indeed be faster
    than with regular grammars?
-   How about
    [LakeGrammars[^?^](http://www.program-transformation.org/edit/Transform/LakeGrammars?topicparent=Transform.IslandGrammars)]{.twikiNewLink
    style="background : #FFFFCE;"} or
    [SkeletonGrammars[^?^](http://www.program-transformation.org/edit/Transform/SkeletonGrammars?topicparent=Transform.IslandGrammars)]{.twikiNewLink
    style="background : #FFFFCE;"}: grammars where the \"top\" of the
    syntax is defined precisely, while some lower non-terminals are
    defined imprecisely. For instance, a precise Yacc grammar where the
    semantic actions (C code) are defined imprecisely?

\--JoostVisser

------------------------------------------------------------------------

I\'ve occasionally done a skeleton grammar, usually for language
conversion. It\'s just an ordinary grammar, byt the lexer recognises an
extra token, usually called **stuff** which matches any token or other
junk that does not occur in the grammar. Very useful for things like
converting between control-statements that have end-markers and ones
that don\'t, for everting C declarations, etc. It gets most of the
boring bulk editing done, leaving you to do the changes that need actual
brainwork \-- [HendrikBoom](../Main/HendrikBoom){.twikiLink}

------------------------------------------------------------------------

[ErnstJanVerhoeven[^?^](http://www.program-transformation.org/edit/Transform/ErnstJanVerhoeven?topicparent=Transform.IslandGrammars)]{.twikiNewLink
style="background : #FFFFCE;"}\'s MSc thesis contains several examples
of [IslandGrammars](IslandGrammars){.twikiLink} in
[SDFII](SDFII){.twikiLink}, which are mostly related to
[COBOL](COBOL){.twikiLink} analysis for [DocGen](DocGen){.twikiLink}.

The current distribution of [DocGen](DocGen){.twikiLink} also includes
an SQL island grammar in [JavaCC](JavaCC){.twikiLink}. It only extracts
the basic SQL commands (insert, delete, update, select, cursor
declarations, \...) but essentially ignores expressions. The
implementation in [JavaCC](JavaCC){.twikiLink} (done out of portability
reasons) is quite a challenge, as it is an LL1 parser generator. \--
[ArieVanDeursen](ArieVanDeursen){.twikiLink}

------------------------------------------------------------------------

[LeonMoonen](LeonMoonen){.twikiLink} as a paper on Island Grammars at
[WCRE](WCRE){.twikiLink} 2001, see
<http://www.cwi.nl/~leon/papers/wcre2001/>

------------------------------------------------------------------------

[CategoryReverseEngineering](CategoryReverseEngineering){.twikiLink} \|
Contributions by [ArieVanDeursen](ArieVanDeursen){.twikiLink},
[JoostVisser](JoostVisser){.twikiLink},
[HendrikBoom](../Main/HendrikBoom){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
