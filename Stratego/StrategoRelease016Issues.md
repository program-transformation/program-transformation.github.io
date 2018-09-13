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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease016Issues?t=1536825681)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease016Issues)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease016Issues)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease016Issues?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease016Issues?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoRelease016Issues?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease016Issues)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease016Issues?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease016Issues?template=oopsmore&param1=1.1&param2=1.1)
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
Stratego/XT 0.16 Issues {#strategoxt-0.16-issues .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Release Notes - Stratego/XT - Version 0.16 (Stratego Core Compiler)

[]{#Bug} Bug
------------

-   \[[STR-14](https://bugs.cs.uu.nl/browse/STR-14)\] - Scoping problem
    at higher optimization levels
-   \[[STR-15](https://bugs.cs.uu.nl/browse/STR-15)\] - strc doesn\'t
    work if invoked with -O \[0/1\]
-   \[[STR-85](https://bugs.cs.uu.nl/browse/STR-85)\] - Sloppy
    variable-scope in let-strategies
-   \[[STR-145](https://bugs.cs.uu.nl/browse/STR-145)\] - Shared
    libraries are not shared at Cygwin: static linking is used.
-   \[[STR-199](https://bugs.cs.uu.nl/browse/STR-199)\] - Dynrules:
    matching of static patterns is not always modulo annos
-   \[[STR-220](https://bugs.cs.uu.nl/browse/STR-220)\] - syntax
    priority issue: \'s1 \< s2 + s3 + s4\' is ambiguous
-   \[[STR-224](https://bugs.cs.uu.nl/browse/STR-224)\] - Term
    projection in annotations is broken
-   \[[STR-235](https://bugs.cs.uu.nl/browse/STR-235)\] - Syntactical
    ambiguity with higher order arguments
-   \[[STR-251](https://bugs.cs.uu.nl/browse/STR-251)\] - Dependent
    dynamic rules not compatible with separate compilation
-   \[[STR-258](https://bugs.cs.uu.nl/browse/STR-258)\] - Dynamic rule
    intersection and union should restore dynamic rule after failure
-   \[[STR-260](https://bugs.cs.uu.nl/browse/STR-260)\] - Dynamic rule
    lifting generates lookup code for undefine rule (L :- t)
-   \[[STR-264](https://bugs.cs.uu.nl/browse/STR-264)\] - collect-all:
    recurse to current term instead of children of current term
-   \[[STR-269](https://bugs.cs.uu.nl/browse/STR-269)\] - Strange bug
    with dynamic rules
-   \[[STR-275](https://bugs.cs.uu.nl/browse/STR-275)\] - lift dynamic
    rules: lifting goes wrong with dependent rules with scope label
-   \[[STR-276](https://bugs.cs.uu.nl/browse/STR-276)\] - Stratego
    doesn\'t honour -at-\* flags
-   \[[STR-290](https://bugs.cs.uu.nl/browse/STR-290)\] - concat-strings
    seg fault
-   \[[STR-293](https://bugs.cs.uu.nl/browse/STR-293)\] - strc tests:
    Makefile.am must use XT\_DARWIN
-   \[[STR-294](https://bugs.cs.uu.nl/browse/STR-294)\] - Standalone
    strc: fix link order for Cygwin
-   \[[STR-301](https://bugs.cs.uu.nl/browse/STR-301)\] - Check
    implementation of quoted constructors
-   \[[STR-308](https://bugs.cs.uu.nl/browse/STR-308)\] - pp-c (or
    possibly parse-c) splits && operator into \"& &()\"
-   \[[STR-309](https://bugs.cs.uu.nl/browse/STR-309)\] - Overlapping
    dynamic rules in definition of expand-overlays transformation
-   \[[STR-318](https://bugs.cs.uu.nl/browse/STR-318)\] - format-check
    fails when reporting incorrect types at top-level (start-symbols)
-   \[[STR-322](https://bugs.cs.uu.nl/browse/STR-322)\] - Concatenation
    of two iter-star-sep lists is not imploded.
-   \[[STR-326](https://bugs.cs.uu.nl/browse/STR-326)\] - File foo not
    removed during configure
-   \[[STR-327](https://bugs.cs.uu.nl/browse/STR-327)\] -
    XT\_CHECK\_STRATEGOXT\_UTILS should use pkgconfig.
-   \[[STR-329](https://bugs.cs.uu.nl/browse/STR-329)\] - use-def
    complains about unbound variables
-   \[[STR-331](https://bugs.cs.uu.nl/browse/STR-331)\] -
    stratego-warning: missing build operator
-   \[[STR-335](https://bugs.cs.uu.nl/browse/STR-335)\] - Typing bug
    with 0.15 strc
-   \[[STR-336](https://bugs.cs.uu.nl/browse/STR-336)\] - Improve
    printing of \'constructor not declared\' error message
-   \[[STR-338](https://bugs.cs.uu.nl/browse/STR-338)\] - strc prints
    \"SSL\_printnl: argument not a list\" to stderr for unclear reasons.
-   \[[STR-339](https://bugs.cs.uu.nl/browse/STR-339)\] - ast2abox
    \--help is wrong
-   \[[STR-341](https://bugs.cs.uu.nl/browse/STR-341)\] - sglri does not
    give nice error message if there are multiple ambiguities
-   \[[STR-343](https://bugs.cs.uu.nl/browse/STR-343)\] - Linking
    problem for identity Stratego program at Mac OS X
-   \[[STR-344](https://bugs.cs.uu.nl/browse/STR-344)\] - Stratego
    libraries should declare interlibrary dependencies
-   \[[STR-372](https://bugs.cs.uu.nl/browse/STR-372)\] - \--keep 10 no
    longer works in all cases
-   \[[STR-381](https://bugs.cs.uu.nl/browse/STR-381)\] - gcc-4.0.1
    invalid storage class for function
-   \[[STR-382](https://bugs.cs.uu.nl/browse/STR-382)\] - rm-annotations
    does not remove annotations
-   \[[STR-402](https://bugs.cs.uu.nl/browse/STR-402)\] - sdf-bundel and
    strategoxt collision on man/man1/sdf2table.1
-   \[[STR-406](https://bugs.cs.uu.nl/browse/STR-406)\] - strc -CI is
    broken
-   \[[STR-411](https://bugs.cs.uu.nl/browse/STR-411)\] - strc-core
    \--library generates mangled external definitions for imported
    external definitions
-   \[[STR-415](https://bugs.cs.uu.nl/browse/STR-415)\] - pp-stratego
    does not print quotes around string literals
-   \[[STR-416](https://bugs.cs.uu.nl/browse/STR-416)\] - No
    pretty-print for [IfThen](IfThen){.twikiLink}
-   \[[STR-417](https://bugs.cs.uu.nl/browse/STR-417)\] - files left
    after distcheck
-   \[[STR-421](https://bugs.cs.uu.nl/browse/STR-421)\] - stratego2abox:
    adapt pretty-printing of switch
-   \[[STR-435](https://bugs.cs.uu.nl/browse/STR-435)\] - parse-unit:
    ambiguous comment
-   \[[STR-439](https://bugs.cs.uu.nl/browse/STR-439)\] - parse-unit:
    \"\" is not allowed in aterm patterns.
-   \[[STR-441](https://bugs.cs.uu.nl/browse/STR-441)\] - pp-stratego
    duplicates double quotes for strings.
-   \[[STR-442](https://bugs.cs.uu.nl/browse/STR-442)\] - pp-stratego
    duplicaties quotes of character literals.
-   \[[STR-443](https://bugs.cs.uu.nl/browse/STR-443)\] - parse-stratego
    no longer supports input from stdin
-   \[[STR-447](https://bugs.cs.uu.nl/browse/STR-447)\] - Placeholder
    strategies missing

[]{#New_Feature} New Feature
----------------------------

-   \[[STR-111](https://bugs.cs.uu.nl/browse/STR-111)\] - pptable-diff:
    consider number of arguments in pp rule
-   \[[STR-164](https://bugs.cs.uu.nl/browse/STR-164)\] - Let: support
    rule syntax
-   \[[STR-303](https://bugs.cs.uu.nl/browse/STR-303)\] - pkg-config:
    introduce variables for location of [XTC](XTC){.twikiLink}
    repository
-   \[[STR-316](https://bugs.cs.uu.nl/browse/STR-316)\] - Old style
    dynamic rules no longer supported
-   \[[STR-320](https://bugs.cs.uu.nl/browse/STR-320)\] - Option for
    preferring .str files over .rtree files
-   \[[STR-325](https://bugs.cs.uu.nl/browse/STR-325)\] - Overlay bodies
    should be pure term expressions
-   \[[STR-345](https://bugs.cs.uu.nl/browse/STR-345)\] - stratego
    runtime libraries must be self-contained
-   \[[STR-346](https://bugs.cs.uu.nl/browse/STR-346)\] - Calling
    strategies by their name
-   \[[STR-351](https://bugs.cs.uu.nl/browse/STR-351)\] - checksum
-   \[[STR-353](https://bugs.cs.uu.nl/browse/STR-353)\] - Detect
    overlapping dynamic rules
-   \[[STR-360](https://bugs.cs.uu.nl/browse/STR-360)\] - autoxt:
    introduce variables for [XTC](XTC){.twikiLink} repository (e.g.
    STRATEGOXT\_XTC, JAVA\_FRONT\_XTC)
-   \[[STR-361](https://bugs.cs.uu.nl/browse/STR-361)\] - autoxt:
    introduce support for pkg\_STRCFLAGS variables
-   \[[STR-371](https://bugs.cs.uu.nl/browse/STR-371)\] - \--statistics
    option
-   \[[STR-375](https://bugs.cs.uu.nl/browse/STR-375)\] - Support
    dynamic linking on Cygwin
-   \[[STR-383](https://bugs.cs.uu.nl/browse/STR-383)\] - standalone
    strc: don\'t use a search path for libraries
-   \[[STR-404](https://bugs.cs.uu.nl/browse/STR-404)\] - Strc: support
    -Xcc (similar to -Xlinker)
-   \[[STR-422](https://bugs.cs.uu.nl/browse/STR-422)\] - pp-stratego
    should support amb nodes

[]{#Task} Task
--------------

-   \[[STR-4](https://bugs.cs.uu.nl/browse/STR-4)\] - Verify Microsoft
    Windows support in buildfarm
-   \[[STR-5](https://bugs.cs.uu.nl/browse/STR-5)\] - Automate creation
    of binary distributions for Microsoft Windows + Cygwin.
-   \[[STR-58](https://bugs.cs.uu.nl/browse/STR-58)\] - Stratego Core
    Language
-   \[[STR-243](https://bugs.cs.uu.nl/browse/STR-243)\] - Restructure
    the native C code of the SSL
-   \[[STR-292](https://bugs.cs.uu.nl/browse/STR-292)\] - Check native
    code of strateg-lib for comparison to ATempty
-   \[[STR-306](https://bugs.cs.uu.nl/browse/STR-306)\] - Adapt
    pretty-printer to Stratego-Sugar syntax
-   \[[STR-307](https://bugs.cs.uu.nl/browse/STR-307)\] - Move
    stratego-desugar from stratego-front to strc-core
-   \[[STR-313](https://bugs.cs.uu.nl/browse/STR-313)\] - Build order of
    stratego-front and stratego-lib
-   \[[STR-315](https://bugs.cs.uu.nl/browse/STR-315)\] - Merge
    improvements to strc with strc-core
-   \[[STR-317](https://bugs.cs.uu.nl/browse/STR-317)\] - Adapt
    optimizer to Stratego Core language
-   \[[STR-319](https://bugs.cs.uu.nl/browse/STR-319)\] - Update
    meta-explode to Stratego-Sugar abstract syntax
-   \[[STR-321](https://bugs.cs.uu.nl/browse/STR-321)\] - List variables
    in concrete syntax and abstract syntax should have \* suffix
-   \[[STR-324](https://bugs.cs.uu.nl/browse/STR-324)\] - Disable build
    of sig2rtg
-   \[[STR-376](https://bugs.cs.uu.nl/browse/STR-376)\] - Replace prims
    for annotation manipulation by annotation match and build operations
-   \[[STR-377](https://bugs.cs.uu.nl/browse/STR-377)\] - Merge
    stratego-runtime and stratego-runtime-choice
-   \[[STR-378](https://bugs.cs.uu.nl/browse/STR-378)\] - strc \--help:
    svn revision is 0 is tarball and buildfarm.
-   \[[STR-379](https://bugs.cs.uu.nl/browse/STR-379)\] - Fix
    compilation issues on Fedor Core 3 in data2xml-doc
-   \[[STR-380](https://bugs.cs.uu.nl/browse/STR-380)\] - Remove code
    from srts that is defined only for bootstrap reasons.
-   \[[STR-387](https://bugs.cs.uu.nl/browse/STR-387)\] - Check native
    code of stratego-lib for compatibility with new translation scheme
-   \[[STR-393](https://bugs.cs.uu.nl/browse/STR-393)\] - Revive
    strategy inlining
-   \[[STR-394](https://bugs.cs.uu.nl/browse/STR-394)\] - Revive pattern
    match compilation
-   \[[STR-395](https://bugs.cs.uu.nl/browse/STR-395)\] - Revive
    innermost fusion
-   \[[STR-396](https://bugs.cs.uu.nl/browse/STR-396)\] - Inlude manual
    pages from Stratego/XT manual in Stratego/XT distribution
-   \[[STR-399](https://bugs.cs.uu.nl/browse/STR-399)\] - Move
    stratego-ensugar to strc
-   \[[STR-423](https://bugs.cs.uu.nl/browse/STR-423)\] - Check if the
    Stratego syntax definition is non-ambiguous without heuristic
    filters.
-   \[[STR-430](https://bugs.cs.uu.nl/browse/STR-430)\] - Fix misc. C
    warnings reported by GCC
-   \[[STR-431](https://bugs.cs.uu.nl/browse/STR-431)\] - Release
    sdf2-bundle that builds on gcc4.
-   \[[STR-432](https://bugs.cs.uu.nl/browse/STR-432)\] - Create binary
    distributions for aterm 2.4.2
-   \[[STR-448](https://bugs.cs.uu.nl/browse/STR-448)\] - Re-enable
    installation of .rtree files

[]{#Improvement} Improvement
----------------------------

-   \[[STR-66](https://bugs.cs.uu.nl/browse/STR-66)\] - Review and
    improve dummification of LHS terms in dynrule lifter
-   \[[STR-76](https://bugs.cs.uu.nl/browse/STR-76)\] - Undefine dynamic
    rules on backtracking
-   \[[STR-101](https://bugs.cs.uu.nl/browse/STR-101)\] - graph-tools:
    use xml-front for
    [GraphXML[^?^](http://www.program-transformation.org/edit/Stratego/GraphXML?topicparent=Stratego.StrategoRelease016Issues)]{.twikiNewLink
    style="background : #FFFFCE;"} input and output
-   \[[STR-210](https://bugs.cs.uu.nl/browse/STR-210)\] - Conc support:
    conc the Conc arguments in build.
-   \[[STR-217](https://bugs.cs.uu.nl/browse/STR-217)\] - Emacs mode:
    support fill-paragraph (alt-q) of xdoc comments
-   \[[STR-219](https://bugs.cs.uu.nl/browse/STR-219)\] - Emacs mode:
    abstract syntax buffer for concrete objects syntax
-   \[[STR-242](https://bugs.cs.uu.nl/browse/STR-242)\] - Define native
    ssl functions as external definitions
-   \[[STR-278](https://bugs.cs.uu.nl/browse/STR-278)\] - ppgen:
    incorrect report of missing constructor
-   \[[STR-279](https://bugs.cs.uu.nl/browse/STR-279)\] - conc-strings:
    support tuples of \>2 strings
-   \[[STR-310](https://bugs.cs.uu.nl/browse/STR-310)\] - remove obscure
    features
-   \[[STR-312](https://bugs.cs.uu.nl/browse/STR-312)\] - Implement
    failure by returning NULL (instead of setjmp/longjmp)
-   \[[STR-328](https://bugs.cs.uu.nl/browse/STR-328)\] - strc
    \--version should provide SVN revision number
-   \[[STR-332](https://bugs.cs.uu.nl/browse/STR-332)\] - strc: \--keep
    only keeps intermediate file if format checker fails
-   \[[STR-347](https://bugs.cs.uu.nl/browse/STR-347)\] - Configuration:
    support combined explicit and implicit configuration
-   \[[STR-348](https://bugs.cs.uu.nl/browse/STR-348)\] - Factorize
    generation of code in
    [SplitDynamicRule[^?^](http://www.program-transformation.org/edit/Stratego/SplitDynamicRule?topicparent=Stratego.StrategoRelease016Issues)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   \[[STR-350](https://bugs.cs.uu.nl/browse/STR-350)\] - Don\'t install
    the internal autoxt macros
-   \[[STR-352](https://bugs.cs.uu.nl/browse/STR-352)\] - Rewrite
    tool-doc to desugaring instead of overlays
-   \[[STR-368](https://bugs.cs.uu.nl/browse/STR-368)\] - Do not
    generate undefine- and new- code for non-dependent dynamic rules
-   \[[STR-369](https://bugs.cs.uu.nl/browse/STR-369)\] - Use checksum
    instead of stamp to generate dynamic rule closure labels
-   \[[STR-370](https://bugs.cs.uu.nl/browse/STR-370)\] - Introduce
    STRCFLAGS. SCFLAGS is obsolete but supported.
-   \[[STR-374](https://bugs.cs.uu.nl/browse/STR-374)\] - Logging should
    not always print the current term
-   \[[STR-384](https://bugs.cs.uu.nl/browse/STR-384)\] - stratego-lib
    testsuite should use libraries in prefix.
-   \[[STR-385](https://bugs.cs.uu.nl/browse/STR-385)\] - Extend
    bound-unbound variables analysis to dynamic rules
-   \[[STR-386](https://bugs.cs.uu.nl/browse/STR-386)\] - suggestion for
    a string-replace strategy
-   \[[STR-390](https://bugs.cs.uu.nl/browse/STR-390)\] - Support make
    check on Cygwin
-   \[[STR-391](https://bugs.cs.uu.nl/browse/STR-391)\] - Support make
    check on Darwin
-   \[[STR-392](https://bugs.cs.uu.nl/browse/STR-392)\] -
    Check-constructor: pretty-print Stratego AST in error message.
-   \[[STR-401](https://bugs.cs.uu.nl/browse/STR-401)\] - Remove
    pkgconfig file of sdf2-bundle from strategoxt
-   \[[STR-405](https://bugs.cs.uu.nl/browse/STR-405)\] - Strc: Consider
    to invoke gcc with -Werror
-   \[[STR-413](https://bugs.cs.uu.nl/browse/STR-413)\] - sglri:
    \--no-heuristic-filters should be the default behaviour.
-   \[[STR-414](https://bugs.cs.uu.nl/browse/STR-414)\] - Pattern match
    compiler: matrix with single row can be implemented directly
-   \[[STR-440](https://bugs.cs.uu.nl/browse/STR-440)\] - parse-unit:
    don\'t accept ambiguities in the testsuite itself

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
