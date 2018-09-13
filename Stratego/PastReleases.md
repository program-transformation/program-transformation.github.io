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
    Page](http://www.program-transformation.org/edit/Stratego/PastReleases?t=1536825604)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/PastReleases)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/PastReleases)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/PastReleases?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/PastReleases?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    43](http://www.program-transformation.org/view/Stratego/PastReleases?rev=1.43)
    [(diff 42)](http://www.program-transformation.org/rdiff/Stratego/PastReleases?rev1=1.43&rev2=1.42)
-   [Rev
    42](http://www.program-transformation.org/view/Stratego/PastReleases?rev=1.42)
    [(diff 41)](http://www.program-transformation.org/rdiff/Stratego/PastReleases?rev1=1.42&rev2=1.41)
-   [Rev
    41](http://www.program-transformation.org/view/Stratego/PastReleases?rev=1.41)
    [(diff 40)](http://www.program-transformation.org/rdiff/Stratego/PastReleases?rev1=1.41&rev2=1.40)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/PastReleases)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/PastReleases?template=oopsmore&param1=1.43&param2=1.43)
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
    \...](http://www.program-transformation.org/oops/Stratego/PastReleases?template=oopsmore&param1=1.43&param2=1.43)
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
Past Releases {#past-releases .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

This page contains plans for past releases. See
[ReleasePlan](ReleasePlan){.twikiLink} for planning of future releases.

### []{#StrategoRelease093_StrategoXT_0}[]{#_StrategoRelease093_StrategoXT_0} [StrategoXT 0.9.3](StrategoRelease093){.twikiLink}

released September 1, 2003

-   New names for `si` and `sc`: decide and apply
    -   [sc renamed to strc](ScRenamedToStrc){.twikiLink}
    -   `si` renamed to `stri`

<!-- -->

-   [Stratego Compiler](StrategoCompiler){.twikiLink}
    -   [Use Stratego Front
        signature[^?^](http://www.program-transformation.org/edit/Stratego/UseStrategoFrontSignature?topicparent=Stratego.PastReleases)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [Stratego Optimizer](StrategoOptimizer){.twikiLink}
        -   Refactor [Stratego
            simplifier](StrategoSimplifier){.twikiLink}
        -   [Build match fusion](BuildMatchFusion){.twikiLink}
        -   [Innermost fusion](InnermostFusion){.twikiLink}
        -   [Pattern match
            compilation](PatternMatchCompilation){.twikiLink}
        -   [Worker wrapper
            splitting](WorkerWrapperSplitting){.twikiLink}
        -   [Strategy inlining](StrategyInlining){.twikiLink}
        -   [Dead definition
            elimination](DeadDefinitionElimination){.twikiLink}
        -   [Constant and copy
            propagation](ConstantAndCopyPropagation){.twikiLink}
        -   [Bound unbound variable
            analysis](BoundUnboundVariableAnalysis){.twikiLink}
        -   [Dead variable
            elimination](DeadVariableElimination){.twikiLink}
        -   [Avoid run time checks on
            variables](AvoidRunTimeChecksOnVariables){.twikiLink}
        -   [Lift definitions to top
            level](LiftDefinitionsToTopLevel){.twikiLink}

<!-- -->

-   [Language extensions](LanguageExtensions){.twikiLink}
    -   [Native primitives](NativePrimitives){.twikiLink} with strategy
        arguments

### []{#StrategoRelease092_StrategoXT_0}[]{#_StrategoRelease092_StrategoXT_0} [StrategoXT 0.9.2](StrategoRelease092){.twikiLink}

released July 4, 2003

-   Upgrade to most recent versions of dependencies:
    -   [ATerm library](ATermLibrary){.twikiLink} 2.0
    -   sdf2 bundle: sglr 3.9, pgen 1.6

<!-- -->

-   Automate creation of RPMs and tarbundles in buildfarm for various
    platforms:
    -   aterm 2.0
    -   sdf2 bundle with sglr 3.9, pgen 1.6
    -   [StrategoXT](StrategoXT){.twikiLink}
    -   support DESTDIR (required for making RPMs)

<!-- -->

-   Make dailydists created by buildfarm available

<!-- -->

-   Allow a separate `make` and `make install` in **distributions** by
    using build-time srts
    -   [StrategoXT](StrategoXT){.twikiLink}
    -   sdf2 bundle

<!-- -->

-   Allow [Configuration without
    prefix[^?^](http://www.program-transformation.org/edit/Stratego/ConfigurationWithoutPrefix?topicparent=Stratego.PastReleases)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   Improved first installation of [StrategoXT](StrategoXT){.twikiLink}
    from Subversion:
    -   bootstrap-time autoxt installation

### []{#StrategoRelease091_StrategoXT_0}[]{#_StrategoRelease091_StrategoXT_0} [StrategoXT 0.9.1](StrategoRelease091){.twikiLink}

Released June 4, 2003

-   Migrate CVS repository to Subversion repository

<!-- -->

-   Get the [daily
    builds[^?^](http://www.program-transformation.org/edit/Stratego/DailyBuilds?topicparent=Stratego.PastReleases)]{.twikiNewLink
    style="background : #FFFFCE;"} completely running

<!-- -->

-   [Refactoring tool
    packages[^?^](http://www.program-transformation.org/edit/Stratego/RefactoringToolPackages?topicparent=Stratego.PastReleases)]{.twikiNewLink
    style="background : #FFFFCE;"}

<!-- -->

-   [XTC](XTC){.twikiLink}
    -   Improve error reporting :
        -   if an imported [XTC](XTC){.twikiLink} repository doesn\'t
            exist
        -   if a user doesn\'t has the rights to register a tool in an
            [XTC](XTC){.twikiLink} repository

<!-- -->

-   SSL
    -   Remove some modules from the SSL because the just don\'t work
        for now: server-test, client-test, accept-test, connect-test,
        communication, connect. Maybe we should work on sockets in the
        stratego-net package.
    -   Move all unit tests of the SSL to a seperate directory: do not
        install them and do not create rtrees .
    -   Efficient native implementation of concat-strings (required for
        [ExtendibleDocumentationGenerator](ExtendibleDocumentationGenerator){.twikiLink}).
    -   Remove `abox` and `abox-ext` module from SSL: tools operating on
        the [BoxLanguage](../Tools/BoxLanguage){.twikiLink} should use
        the signatures of [GPP](GPP){.twikiLink}

<!-- -->

-   [StrategoFront](StrategoFront){.twikiLink}
    -   `TupleCong` is overloaded for the empty tuple congruence and
        tuple congruences with strategy arguments.
        [GPP](GPP){.twikiLink} cannot handle this because constructor
        names cannot be overloaded.

<!-- -->

-   make boxenv an [AutoXT](AutoXT){.twikiLink} powered package and
    include boxenv.sty in distribution to prevent install time
    dependency on
    [LaTeX[^?^](http://www.program-transformation.org/edit/Stratego/LaTeX?topicparent=Stratego.PastReleases)]{.twikiNewLink
    style="background : #FFFFCE;"}.

<!-- -->

-   make stratego-util an [AutoXT](AutoXT){.twikiLink} powered package
    and include it in the list of packages

<!-- -->

-   [Mac OS X support](MacOSXSupport){.twikiLink}

### []{#StrategoRelease09_StrategoXT_0_9}[]{#_StrategoRelease09_StrategoXT_0_} [StrategoXT 0.9](StrategoRelease09){.twikiLink}

Released January 26, 2003

-   [Fusion of Stratego and XT](FusionOfStrategoAndXT){.twikiLink}
-   [Stratego Run Time System](StrategoRunTimeSystem){.twikiLink}
-   [AutoXT](AutoXT){.twikiLink}
    -   [Upgrade to new Autotools](UpgradeToNewAutotools){.twikiLink}
    -   [Automake support for
        Stratego[^?^](http://www.program-transformation.org/edit/Stratego/AutomakeSupportForStratego?topicparent=Stratego.PastReleases)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [Str
        extension[^?^](http://www.program-transformation.org/edit/Stratego/StrExtension?topicparent=Stratego.PastReleases)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [Bootstrapped packages containing generated
        sources[^?^](http://www.program-transformation.org/edit/Stratego/BootstrappedPackagesContainingGeneratedSources?topicparent=Stratego.PastReleases)]{.twikiNewLink
        style="background : #FFFFCE;"}
-   [XTC](XTC){.twikiLink} \-- [Transformation Tool
    Composition](TransformationToolComposition){.twikiLink}
-   Language/compiler
    -   [Retire Transform.YetAnotherCompilerCompiler
        Grammar[^?^](http://www.program-transformation.org/edit/Stratego/RetireTransformYetAnotherCompilerCompilerGrammar?topicparent=Stratego.PastReleases)]{.twikiNewLink
        style="background : #FFFFCE;"}
    -   [Character syntax](CharacterSyntax){.twikiLink}
    -   [Dynamic Rule Semantics](DynamicRuleSemantics){.twikiLink} \--
        Overlapping Left-Hand Sides bug
-   New packages
    -   [C Tools](CTools){.twikiLink}
    -   [Dot
        Tools[^?^](http://www.program-transformation.org/edit/Stratego/DotTools?topicparent=Stratego.PastReleases)]{.twikiNewLink
        style="background : #FFFFCE;"}
-   [GPP](GPP){.twikiLink} refactoring using [XTC](XTC){.twikiLink}
-   Binary distributions

### []{#StrategoRelease081_Stratego_0_8}[]{#_StrategoRelease081_Stratego_0_8} [Stratego 0.8.1](StrategoRelease081){.twikiLink}

Released September 20, 2002

-   maintenance release

### []{#StrategoRelease08_Stratego_0_8}[]{#_StrategoRelease08_Stratego_0_8_} [Stratego 0.8](StrategoRelease08){.twikiLink}

Released June 27, 2002

-   [ConcreteSyntax](ConcreteSyntax){.twikiLink} in
    [StrategoFront](StrategoFront){.twikiLink}
-   [TermAnnotation](TermAnnotation){.twikiLink} (improved)
-   [ListMatching](ListMatching){.twikiLink}
-   [StrategoPrettyPrinter](StrategoPrettyPrinter){.twikiLink}
-   [InnermostFusion](InnermostFusion){.twikiLink}

### []{#StrategoRelease07_Stratego_0_7}[]{#_StrategoRelease07_Stratego_0_7_} [Stratego 0.7](StrategoRelease07){.twikiLink}

Released March 13, 2002

-   [FixedLengthTuple](FixedLengthTuple){.twikiLink}
-   [ListConstructors](ListConstructor){.twikiLink}
-   [ListTraversal](ListTraversal){.twikiLink}
-   [PairConstructor](PairConstructor){.twikiLink}
-   [GlobalBacktracking[^?^](http://www.program-transformation.org/edit/Stratego/GlobalBacktracking?topicparent=Stratego.PastReleases)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [ConstantTermCaching](ConstantTermCaching){.twikiLink}
-   [GuardedLeftChoice](GuardedLeftChoice){.twikiLink}
-   [StrategoSyntax](StrategoSyntax){.twikiLink} (update)
-   [TermAnnotation](TermAnnotation){.twikiLink}
-   [PackStrategoShouldFailOnParserFailure[^?^](http://www.program-transformation.org/edit/Stratego/PackStrategoShouldFailOnParserFailure?topicparent=Stratego.PastReleases)]{.twikiNewLink
    style="background : #FFFFCE;"}

### []{#StrategoRelease064_Stratego_0_6}[]{#_StrategoRelease064_Stratego_0_6} [Stratego 0.6.4](StrategoRelease064){.twikiLink}

Released January 3, 2002

-   Fixed [StrategyRule](StrategyRule){.twikiLink} desugaring
-   [EvaluationOrder](EvaluationOrder){.twikiLink} for choice changed

### []{#StrategoRelease063_Stratego_0_6}[]{#_StrategoRelease063_Stratego_0_6} [Stratego 0.6.3](StrategoRelease063){.twikiLink}

Released November 26, 2001

-   [ExplodeTerm[^?^](http://www.program-transformation.org/edit/Stratego/ExplodeTerm?topicparent=Stratego.PastReleases)]{.twikiNewLink
    style="background : #FFFFCE;"} /
    [MkTerm[^?^](http://www.program-transformation.org/edit/Stratego/MkTerm?topicparent=Stratego.PastReleases)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [TermWrap](TermWrap){.twikiLink}
-   [TermProject](TermProject){.twikiLink}

### []{#StrategoRelease062_Stratego_0_6}[]{#_StrategoRelease062_Stratego_0_6} [Stratego 0.6.2](StrategoRelease062){.twikiLink}

Released October 6, 2001

-   [StrategoSyntax](StrategoSyntax){.twikiLink}

### []{#StrategoRelease06_Stratego_0_6}[]{#_StrategoRelease06_Stratego_0_6_} [Stratego 0.6](StrategoRelease06){.twikiLink}

Released August 2001

-   Declare constructors in compiler
-   Clean up specification of compiler components
-   New [ImplementationScheme](ImplementationScheme){.twikiLink}

### []{#StrategoRelease05_Stratego_0_5}[]{#_StrategoRelease05_Stratego_0_5_} [Stratego 0.5](StrategoRelease05){.twikiLink}

Released 26 March 2001

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.PastReleases moved from Stratego.OIdReleases on 10 Feb 2003 -
22:15 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Stratego/PastReleases?newweb=Stratego&newtopic=OIdReleases&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
