::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[SDF Home](http://www.syntax-definition.org)**

-   [About](SdfLanguage){.twikiLink}
-   [Documentation](SdfDocumentation){.twikiLink}
-   [Download](SdfSoftware){.twikiLink}
-   [Grammars](SdfGrammars){.twikiLink}
-   [Related Software](SdfRelatedSoftware){.twikiLink}

**Community**

-   [Contributors](SdfDevelopment){.twikiLink}
-   [Publications](SdfPublications){.twikiLink}
-   [Applications](SdfApplications){.twikiLink}
-   [Mailing Lists](MailingList){.twikiLink}
-   [License](BSDLicense){.twikiLink}

**Development**

-   [Tools](DevelopmentTools){.twikiLink}
-   [API](http://homepages.cwi.nl/~daybuild/daily-docs)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers?t=1536826609)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers)
-   [Attach
    File](http://www.program-transformation.org/attach/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers?template=oopsmore&param1=1.7&param2=1.7)
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
Disambiguation Filters For Scannerless Generalized LRParsers {#disambiguation-filters-for-scannerless-generalized-lrparsers .twikiTopicTitle}
============================================================

::: {.twikiWebTitle}
Sdf
:::

by [MarkVanDenBrand](../Transform/MarkVanDenBrand){.twikiLink},
[JeroenScheerder[^?^](http://www.program-transformation.org/edit/Sdf/JeroenScheerder?topicparent=Sdf.DisambiguationFiltersForScannerlessGeneralizedLRParsers)]{.twikiNewLink
style="background : #FFFFCE;"},
[JurgenVinju](../Transform/JurgenVinju){.twikiLink} and
[EelcoVisser](../Transform/EelcoVisser){.twikiLink}. Disambiguation
filters for scannerless generalized LR parsers. In N. Horspool, editor,
Compiler Construction (Transform.CC\'02), volume 2304 of Lecture Notes
in Computer Science, pages 143\--158, Grenoble, France, April 2002.
Springer-Verlag.

**Abstract**

In this paper we present the fusion of generalized LR parsing and
scannerless parsing. This combination supports syntax definitions in
which all aspects (lexical and context-free) of the syntax of a language
are defined explicitly in one formalism. Furthermore, there are no
restrictions on the class of grammars, thus allowing a natural syntax
tree structure. Ambiguities that arise through the use of unrestricted
grammars are handled by explicit disambiguation constructs, instead of
implicit defaults that are taken by traditional scanner and parser
generators. Hence, a syntax definition becomes a full declarative
description of a language. Disambiguation constructs can be interpreted
as filters on parse forests. Scannerless generalized LR parsing is a
viable technique that has been applied in various industrial and
academic projects.

**Technical report**

-   <http://www.cs.uu.nl/~visser/ftp/BSVV02.pdf>

**Review**

The following is an excerpt from a anonymous referee report:

> This paper, \"Disambiguation Filters for Scannerless Generalized LR
> Parsers,\" is about a systematic way of dealing with the problem of
> parsing with ambiguous grammars.
>
> I thought this paper was wonderful. Sure it has some flaws, but I
> think it and all the [SGLR](SGLR){.twikiLink} papers should be
> required reading by all faculty who teach compilers and all graduate
> students who will someday teach compilers. Why? Because
> [SGLR](SGLR){.twikiLink} represents so many advantages over the
> lex+yacc or hand-coded lexer+parser models that the only compelling
> reason that I can think of to not teach [SGLR](SGLR){.twikiLink} is,
> as Homer Simpson would say, \"It\'s a good idea, but it\'s a new idea,
> and, therefore, I fear it and must reject it.\" (OK, it does have one
> disadvantage that is serious, speed, but that\'s not enough of a
> concern to eliminate it from all compiler jobs.)
>
> So, what\'s [SGLR](SGLR){.twikiLink}? It\'s a system of handling all
> lexical and parsing concerns within a unified Generalized LR parser.
> This unified system has advantages galore, which are well-described in
> the paper. Because it uses GLR parsing technology it allows ambiguous
> grammars. This paper describes 4 mechanisms that allow for
> **declarative** disambiguation of the resulting parses. All four are
> well described and carefully analyzed.

------------------------------------------------------------------------

[CategoryPaper](../Transform/CategoryPaper){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Sdf.DisambiguationFiltersForScannerlessGeneralizedLRParsers moved from
Transform.DisambiguationFiltersForScannerlessGeneralizedLRParsers on 24
Jan 2004 - 17:44 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Sdf/DisambiguationFiltersForScannerlessGeneralizedLRParsers?newweb=Transform&newtopic=DisambiguationFiltersForScannerlessGeneralizedLRParsers&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
