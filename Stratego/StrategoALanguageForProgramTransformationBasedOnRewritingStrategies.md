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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoALanguageForProgramTransformationBasedOnRewritingStrategies?t=1536825423)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoALanguageForProgramTransformationBasedOnRewritingStrategies)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoALanguageForProgramTransformationBasedOnRewritingStrategies)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoALanguageForProgramTransformationBasedOnRewritingStrategies?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoALanguageForProgramTransformationBasedOnRewritingStrategies?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoALanguageForProgramTransformationBasedOnRewritingStrategies?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoALanguageForProgramTransformationBasedOnRewritingStrategies)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoALanguageForProgramTransformationBasedOnRewritingStrategies?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoALanguageForProgramTransformationBasedOnRewritingStrategies?template=oopsmore&param1=1.1&param2=1.1)
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
Stratego ALanguage For Program Transformation Based On Rewriting Strategies {#stratego-alanguage-for-program-transformation-based-on-rewriting-strategies .twikiTopicTitle}
===========================================================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

E. Visser. **Stratego: A language for program transformation based on
rewriting strategies. System description of Stratego 0.5.** In A.
Middeldorp, editor, Rewriting Techniques and Applications (RTA\'01),
volume 2051 of Lecture Notes in Computer Science, pages 357\--361.
Springer-Verlag, May 2001.

#### []{#Introduction} Introduction

Program transformation is used in many areas of software engineering.
Examples include compilation, optimization, synthesis, refactoring,
migration, normalization and improvement \\cite{OSPT}. Rewrite rules are
a natural formalism for expressing single program transformations.
However, using a standard strategy for normalizing a program with a set
of rewrite rules is not adequate for implementing program transformation
systems. It may be necessary to apply a rule only in some phase of a
transformation, to apply rules in some order, or to apply a rule only to
part of a program. These restrictions may be necessary to avoid
non-termination or to choose a specific path in a non-confluent rewrite
system.

Stratego is a language for the specification of program transformation
systems based on the paradigm of rewriting strategies. It supports the
separation of strategies from transformation rules, thus allowing
careful control over the application of these rules. As a result of this
separation, transformation rules are reusable in multiple different
transformations and generic strategies capturing patterns of control can
be described independently of the transformation rules they apply. Such
strategies can even be formulated independently of the object language
by means of the generic term traversal capabilities of Stratego.

In this short paper I give a description of version 0.5 of the Stratego
system, discussing the features of the language, the library, the
compiler and some of the applications that have been built. Stratego is
available as free software under the GNU [LGPL](LGPL){.twikiLink} from
<http://www.stratego-language.org>.

#### []{#Online} Online

-   <http://www.cs.uu.nl/people/visser/ftp/Vis01.pdf>

#### []{#Bib_entry} Bib entry

    @InProceedings{Vis01.rta,
      author =    {Eelco Visser},
      title =    {Stratego: {A} Language for Program Transformation
                      based on Rewriting Strategies. {S}ystem Description
                      of {Stratego} 0.5},
      booktitle =    {Rewriting Techniques and Applications (RTA'01)},
      pages =    {357--361},
      year =    2001,
      editor =    {A. Middeldorp},
      volume =    2051,
      series =    {Lecture Notes in Computer Science},
      month =    {May},
      publisher =    {Springer-Verlag}
    }

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
