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
    Page](http://www.program-transformation.org/edit/Stratego/ReleasePlan?t=1536825663)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ReleasePlan)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ReleasePlan)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ReleasePlan?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ReleasePlan?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    164](http://www.program-transformation.org/view/Stratego/ReleasePlan?rev=1.164)
    [(diff 163)](http://www.program-transformation.org/rdiff/Stratego/ReleasePlan?rev1=1.164&rev2=1.163)
-   [Rev
    163](http://www.program-transformation.org/view/Stratego/ReleasePlan?rev=1.163)
    [(diff 162)](http://www.program-transformation.org/rdiff/Stratego/ReleasePlan?rev1=1.163&rev2=1.162)
-   [Rev
    162](http://www.program-transformation.org/view/Stratego/ReleasePlan?rev=1.162)
    [(diff 161)](http://www.program-transformation.org/rdiff/Stratego/ReleasePlan?rev1=1.162&rev2=1.161)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ReleasePlan)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ReleasePlan?template=oopsmore&param1=1.164&param2=1.164)
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
    \...](http://www.program-transformation.org/oops/Stratego/ReleasePlan?template=oopsmore&param1=1.164&param2=1.164)
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
Release Plan {#release-plan .twikiTopicTitle}
============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

This page provides the tentative scheduling for future releases of
[StrategoXT](StrategoXT){.twikiLink}. See
[PastReleases](PastReleases){.twikiLink} for an overview of the
development of [StrategoXT](StrategoXT){.twikiLink}. Note that except
for the first planned release, the plans mentioned on this page have the
character of a wishlist and that all dates are indicative only. If you
are interested in (contributing to) any of the items mentioned here or
have ideas of your own, feel free to join the discussion at the
stratego-dev [mailing list](MailingList){.twikiLink}.

[]{#Issue_Tracking} Issue Tracking
==================================

The [JIRA roadmap of the StrategoXT
project](https://catamaran.labs.cs.uu.nl/jira/secure/BrowseProject.jspa?id=10000&report=roadmap)
provides a detailed and up-to-date overview of upcoming features.

[]{#Items_that_need_to_be_added_to_J} Items that need to be added to JIRA
-------------------------------------------------------------------------

### []{#Language} Language

-   Concrete syntax for arithmetic and relational operations

<!-- -->

-   [Language extensions](LanguageExtensions){.twikiLink}
    -   [Dynamic
        patterns[^?^](http://www.program-transformation.org/edit/Stratego/DynamicPatterns?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [Dynamic
        strategies[^?^](http://www.program-transformation.org/edit/Stratego/DynamicStrategies?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
        style="background : #FFFFCE;"} Can currently be emulated for a
        single strategy with a dynamic rule `x -> x where s`.

<!-- -->

-   Instrumentation of Stratego programs in aspect-oriented style

### []{#Compiler} Compiler

-   [Stratego Core Language](StrategoCoreLanguage){.twikiLink}
    -   Integrate annotations in abstract syntax
    -   [Dynamic rule semantics](DynamicRuleSemantics){.twikiLink}:
        rewriting terms with annotations

<!-- -->

-   Typecheck match and build terms against signature (warning only)

<!-- -->

-   [Common subexpression
    elimination](CommonSubexpressionElimination){.twikiLink}

<!-- -->

-   [Separate compilation](SeparateCompilation){.twikiLink}

<!-- -->

-   [Effects analysis](EffectsAnalysis){.twikiLink}
    -   Make it possible to specify a certain rule should always
        succeed, and if it doesn\'t print the child rule that was
        responsable for the problem (maybe even print stacktrace)

<!-- -->

-   [Detect overlapping rules](DetectOverlappingRules){.twikiLink}

### []{#Interpreter} Interpreter

-   is the interpreter up to date? (testsuites)
-   make the interpreter reusable in different front-ends
    ([StrategoShell](StrategoShell){.twikiLink},
    [StrategoScript[^?^](http://www.program-transformation.org/edit/Stratego/StrategoScript?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
    style="background : #FFFFCE;"}) or even inside \'ordinary\' Stratego
    programs

### []{#Deployment} Deployment

-   Start maintaining Debian packages
    -   Become Debian apt source
    -   Daily build binary packages

<!-- -->

-   Solaris support verified in buildfarm
    -   [Solaris/UltraSPARC](SolarisUltraSparcSupport){.twikiLink}
    -   [Solaris/x86](SolarisIntelSupport){.twikiLink}

<!-- -->

-   [Mac OS X Support](MacOSXSupport){.twikiLink} verified in buildfarn
    -   Automate creation of binary distributions StrategoXT

<!-- -->

-   Separate deployment of individual packages
    -   Distribute separate packages in a collection of RPMS or Nix
        expressions?
    -   sdf2-bundle as well

<!-- -->

-   Verify the portability of the dependencies:
    -   [Choice Point Library
        Portability[^?^](http://www.program-transformation.org/edit/Stratego/ChoicePointLibraryPortability?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [ATerm
        Portability[^?^](http://www.program-transformation.org/edit/Stratego/ATermPortability?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [Sdf2 Bundle
        Portability[^?^](http://www.program-transformation.org/edit/Stratego/Sdf2BundlePortability?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
        style="background : #FFFFCE;"}

### []{#Tools} Tools

-   Embedding generator: generate [SDF](SDF){.twikiLink} grammar with
    all (?) concrete object syntax productions

<!-- -->

-   [GPP](GPP){.twikiLink}: better support for pretty-printing terms
    with annotations

<!-- -->

-   [ImplodeAsFix[^?^](http://www.program-transformation.org/edit/Tools/ImplodeAsFix?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
    style="background : #FFFFCE;"} : attach location in source file in
    annotations after implosion
    -   See [addPosInfo](../Tools/AddPosInfo){.twikiLink}

<!-- -->

-   [Tool
    documentation[^?^](http://www.program-transformation.org/edit/Stratego/ToolDocumentation?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
    style="background : #FFFFCE;"}
    -   Provide more easy and abstract facilities for tools to document
        themselves in `--help` and/or man pages
    -   Refactor the existing tool documentation (ofter in comments or
        bad layout) to this new mechanism.
    -   [DocBook[^?^](http://www.program-transformation.org/edit/Stratego/DocBook?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
        style="background : #FFFFCE;"} : write a docbook2wiki,
        docbook2help?

### []{#Misc}[]{#Misc_} Misc.

-   [QuickCheck[^?^](http://www.program-transformation.org/edit/Stratego/QuickCheck?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
    style="background : #FFFFCE;"} for Stratego: specify properties in
    program and test these for randomly generated arguments

<!-- -->

-   Benchmarking framework

<!-- -->

-   [XTC](XTC){.twikiLink}
    -   Improve overriding of tools
    -   Task-oriented component composition
    -   check out relation to package config

<!-- -->

-   [Improve IO facilities in SSL](ImproveIOFacilitiesInSSL){.twikiLink}

<!-- -->

-   Project wizard that sets up all default files for typical
    [StrategoXT](StrategoXT){.twikiLink} packages and applications.

[]{#StrategoRelease1_StrategoXT_1_0}[]{#_StrategoRelease1_StrategoXT_1_0} [StrategoXT 1.0](StrategoRelease1){.twikiLink}
------------------------------------------------------------------------------------------------------------------------

-   [ExamplesPackage[^?^](http://www.program-transformation.org/edit/Stratego/ExamplesPackage?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   [TypeSystem](TypeSystem){.twikiLink}

<!-- -->

-   Complete specification of the [Stratego
    semantics](StrategoSemantics){.twikiLink}

<!-- -->

-   Generalize traversal primitives \*
    [RightToLeftTraversal](RightToLeftTraversal){.twikiLink}

<!-- -->

-   [ReversibleRules](ReversibleRules){.twikiLink} A : t \<-\> t\' L(A)
    R(A) B reverse A

<!-- -->

-   [Conditional
    Compilation[^?^](http://www.program-transformation.org/edit/Stratego/ConditionalCompilation?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- Useful for enabling/disabling
    special features at compile time (such as support for language
    extensions), and for making modules useable both stand-alone and
    imported into other modules. Use C preprocessor says Eelco D.

<!-- -->

-   Scoped dynamic relations (multi-way rules)

<!-- -->

-   [Global
    variables[^?^](http://www.program-transformation.org/edit/Stratego/GlobalVariables?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
    style="background : #FFFFCE;"} \-- Maybe with a syntax that
    separates them clearly from local variables. Can of course be
    emulated using tables, at the expense of table lookups and the
    inconvenience of creating/destroying tables.

<!-- -->

-   [Scoped
    tables[^?^](http://www.program-transformation.org/edit/Stratego/ScopedTables?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
    style="background : #FFFFCE;"} (and global variables (in which case
    they probably won\'t be global anymore)).

<!-- -->

-   [Improve error
    messages[^?^](http://www.program-transformation.org/edit/Stratego/ImproveErrorMessages?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
    style="background : #FFFFCE;"} (add linenr, continue after problem
    if possible and give multiple/all errormsgs which decreases time to
    fix all problems).

<!-- -->

-   Improve debugging:
    -   allow for easy print statement that automatically adds
        filename + linenr

<!-- -->

-   Improve automatic [preservation of
    annotations[^?^](http://www.program-transformation.org/edit/Stratego/PreservationOfAnnotations?topicparent=Stratego.ReleasePlan)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   Auto concat Conc node after an antiquotation that returns a list

<!-- -->

-   Think about \< \> usage: \"s = id\" vs \"s = (\...)\"

[]{#StrategoXT_2_0} StrategoXT 2.0
----------------------------------

-   Complete redesign of the syntax. Stratego has matured enough that we
    have a good understanding of which features are needed. However, any
    attempts to use those features to solve non-trivial problems has a
    tendency to degenerate into a mess of strange symbols. Even simple
    things such as if-then-else are utterly unreadable (although the
    theory behind the syntax is elegant\...).

<!-- -->

-   Not only allow strategies to be passed as special arguments but also
    allow them to be returned from a rule/strategy and be assigned to a
    new variable.
    -   See [RhoStratego](RhoStratego){.twikiLink}
    -   [RepresentStrategyAsTerm](RepresentStrategyAsTerm){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.ReleasePlan moved from Stratego.FutureReleases on 09 Feb 2003
- 22:22 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Stratego/ReleasePlan?newweb=Stratego&newtopic=FutureReleases&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
