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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease054?t=1536825682)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease054)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease054)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease054?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease054?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoRelease054?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease054)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease054?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease054?template=oopsmore&param1=1.1&param2=1.1)
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
Stratego Release 054 {#stratego-release-054 .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Changes since [StrategoRelease053](StrategoRelease053){.twikiLink}

Summary

-   Dynamic rules: see
    [ScopedDynamicRewriteRules](ScopedDynamicRewriteRules){.twikiLink}
    paper
-   Lots of improvements to the library (thanks
    [HedzerWestra](../Main/HedzerWestra){.twikiLink} and
    [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink})
-   Improvement of installation robustness (e.g., not depending on
    defined path to sc; thanks
    [JohnReppy[^?^](http://www.program-transformation.org/edit/Transform/JohnReppy?topicparent=Stratego.StrategoRelease054)]{.twikiNewLink
    style="background : #FFFFCE;"})

<!-- -->

    2001-06-20  Eelco Visser  <visser@acm.org>

       * Release 0.5.4

    2001-06-18  Eelco Visser  <visser@acm.org>

       * spec/front/frontend-test.r: updated tests, Undefined dynamic
       rules can also have conditions.

    2001-06-17  Eelco Visser  <Eelco Visser <visser@acm.org>>

       * spec/front/normalize-spec.r: Added overriding dynamic rules that
       change the definition for the currently active key without
       introducing an entry in the local scope. This is needed to update
       rules defined in outer scopes. (Application: dead code
       elimination)
       
    2001-06-17  Eelco Visser <visser@acm.org>

       * spec/front/normalize-spec.r: Repaired bug in desugaring
       of "Undefined" dynamic rules.

    2001-06-15  Eelco Visser  <visser@acm.org>

       * spec/syn/stratego.lx: Allow \begin{code} to start file.

    2001-06-14  Eelco Visser  <visser@acm.org>

       * spec/front/normalize-spec.r: Dynamic rules that have Undefined
       as right-hand side will cause the invocation of the dynamic rule
       (on the specific lhs pattern) to fail. This is needed in order to
       shadow rules from outer scopes that might not be applicable.

    2001-06-13  Eelco Visser  <visser@acm.org>

       * src/make_rules.in (CC): Declare as @CC@ instead of gcc.

       * spec/slib/spec/string-test.r, string.r: get-path extracts the
       path prefix from a command string.

       * spec/syn/pack-stratego.r: Deduce path for parse-mod from path
       for pack-stratego (from command-line option 0).

    2001-06-13 Hedzer Westra <hhwestra@cs.uu.nl>

       * Added test for strcmp and such, and fixed string-gt

    2001-06-13  Eelco Visser  <visser@acm.org>

       * spec/front/data/Makefile.am : Repaired EXTRA_DIST

       * spec/slib/spec/scoped-finite-map-test.r: Added tests for
       assert.

       * spec/slib/spec/scoped-finite-map.r: Assert now also works
       when without initialization of the table.

       * test/syntax/dynamic-rules-test.r: Added test of overriding
       behaviour of dynamic rules.

    2001-06-11  Eelco Visser  <visser@acm.org>

       * spec/front/check-constructors.r: Rules and strategies are merged.

       * bootinstall

       * spec/syn/stratego.lx: Tokens {| and |} for delimiting dynamic
       rule scopes.

       * spec/lib/stratlib.r: Added binding by DynamicRules

       * spec/front/extract.r, spec/front/inline.r, spec/front/inlining.r,
       spec/front/needed-defs-test.r: main -> name of module

       * spec/sig/sugar.r: Signatures for dynamic rules constructors.

       * spec/front/frontend-test.r: Unit tests for desugaring of dynamic
       rules

       * spec/front/spec-to-sdefs.r, spec/front/use-def.r: Rules and strategies were merged.

       * spec/front/frontend.r: layout

       * spec/front/data/dynrules.r: Test for desugaring of dynamic rules

    2001-06-10  Eelco Visser  <visser@acm.org>

       * spec/front/normalize-spec.r: Desugaring of dynamic rules. Rules
       and strategies were merged into one list.

       * test/syntax/dynamic-rules-test.r: Test for dynamic rule syntax

       * spec/slib/spec/env-traversal.r: Traversals involving one.

    2001-06-10  Eelco Visser  <visser@acm.org>

       * spec/slib/src/tables.c: Made table access more robust; there is
       no need to create a table explicitly, it is always created when a
       table-put or table-get is done.

       * spec/slib/spec/tables-test.r: Tests for robustness of table
       operations

    2001-06-09  Eelco Visser  <visser@acm.org>

       * spec/syn/stratego.grm: Liberalized syntax: rule and strategy
       definition can now be defined under both the rules and strategies
       keywords. In effect, rules and strategy definitions can be mixed
       in any order.

    2001-06-07  Eelco Visser  <visser@acm.org>

       * spec/slib/spec/string.r: Repaired basename to correctly
       handle slashes in names. (Merijn de Jonge)

       * spec/slib/spec/string-test.r: Extra test for basename

    2001-06-01    <visser@acm.org>

       * spec/slib/spec/template-test.r: Defined main

    2001-06-08    <hhwestra@cs.uu.nl>

            * spec/slib/spec/string.r: Changed string.r to use -1, which wasn't parsed by parse-mod
              when strcmp was defined.
     
    2001-05-31    <visser@acm.org>

       * Redocumented all library modules; add literate program wrapper
       and consistent naming of header.

    2001-05-24    <visser@acm.org>

       * configure.in: Incremented version number to 0.5.4beta

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
