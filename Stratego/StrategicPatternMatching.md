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
    Page](http://www.program-transformation.org/edit/Stratego/StrategicPatternMatching?t=1536825424)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategicPatternMatching)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategicPatternMatching)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategicPatternMatching?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategicPatternMatching?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/StrategicPatternMatching?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/StrategicPatternMatching?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/StrategicPatternMatching?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/StrategicPatternMatching?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategicPatternMatching?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategicPatternMatching?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategicPatternMatching)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategicPatternMatching?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategicPatternMatching?template=oopsmore&param1=1.4&param2=1.4)
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
Strategic Pattern Matching {#strategic-pattern-matching .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Strategic Pattern Matching is a paper about extending standard
first-order term pattern matching using strategies to define complex
patterns. Specifically it describes the [Stratego
idioms](StrategoIdiom){.twikiLink} [recursive
pattern](RecursivePattern){.twikiLink}, [contextual
rule](ContextualRule){.twikiLink} and [overlay
definition](OverlayDefinition){.twikiLink}.

**Bibliographic Information**

Eelco Visser. Strategic Pattern Matching. In *Rewriting Techniques and
Applications (RTA\'99)*, volume 1631 of Lecture Notes in Computer
Science, pages 30-44, Trento, Italy. July 1999.

**Abstract**

Stratego is a language for the specification of transformation rules and
strategies for applying them. The basic actions of transformations are
matching and building instantiations of first-order term patterns. The
language supports concise formulation of generic and data type-specific
[term traversals](TermTraversal){.twikiLink}. One of the unusual
features of Stratego is the separation of scope from matching, allowing
sharing of variables through traversals. The combination of first-order
patterns with strategies forms an expressive formalism for pattern
matching. In this paper we discuss three examples of *strategic pattern
matching*: (1) [Contextual rules](ContextualRule){.twikiLink} allow
matching and replacement of a pattern at an arbitrary depth of a subterm
of the root pattern. (2) [Recursive
patterns](RecursivePattern){.twikiLink} can be used to characterize
concisely the structure of languages that form a restriction of a larger
language. (3) [Overlays](OverlayDefinition){.twikiLink} serve to hide
the representation of a language in another (more generic) language.
These techniques are illustrated by means of specifications in Stratego.

**Download**

-   <http://www.cs.uu.nl/people/visser/ftp/Vis99.ps.gz>

------------------------------------------------------------------------

[CategoryPaper](../Transform/CategoryPaper){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
