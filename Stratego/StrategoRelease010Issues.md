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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease010Issues?t=1536825679)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease010Issues)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease010Issues)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease010Issues?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease010Issues?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoRelease010Issues?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease010Issues?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoRelease010Issues?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease010Issues)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease010Issues?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease010Issues?template=oopsmore&param1=1.2&param2=1.2)
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
Stratego Release 010 Issues {#stratego-release-010-issues .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Issues fixed in [StrategoXT 0.10](StrategoRelease010){.twikiLink}

[]{#Bug} Bug
------------

-   \[[STR-8](http://yellowgrass.org/STR-8)\] - Scopes and Undefined are
    reserved terms
-   \[[STR-10](http://yellowgrass.org/STR-10)\] - Incorrect variable
    unbound error when using the ( -\> ) construct
-   \[[STR-11](http://yellowgrass.org/STR-11)\] - Unbound variable in
    override rules
-   \[[STR-12](http://yellowgrass.org/STR-12)\] - @ in dynamic rule
    match
-   \[[STR-16](http://yellowgrass.org/STR-16)\] - Var not bound: no
    error or warning
-   \[[STR-26](http://yellowgrass.org/STR-26)\] - implode-asfix doesn\'t
    support \'iter-n\' nor \'iter-sep-n\'
-   \[[STR-27](http://yellowgrass.org/STR-27)\] - parse-pp-table
    doesn\'t support \'iter-n\' nor \'iter-sep-n\'
-   \[[STR-31](http://yellowgrass.org/STR-31)\] - NEWS/news breaks
    checkout/build on OS X
-   \[[STR-33](http://yellowgrass.org/STR-33)\] - sdf-bracket always
    assumes that the outer term is the grammar identifier
-   \[[STR-37](http://yellowgrass.org/STR-37)\] - Use new
    [SDF](SDF){.twikiLink} syntax definition in ppgen
-   \[[STR-43](http://yellowgrass.org/STR-43)\] - pack-stratego prefers
    the last -I argument, not the first one
-   \[[STR-49](http://yellowgrass.org/STR-49)\] - listvars as term
    arguments are not usable
-   \[[STR-60](http://yellowgrass.org/STR-60)\] - Bad constructor for
    definition in pack-sdf
-   \[[STR-69](http://yellowgrass.org/STR-69)\] - parse-unit cannot
    handle tuples in a test
-   \[[STR-80](http://yellowgrass.org/STR-80)\] - C keywords are not
    allowed as identifiers, but syntax def allows this.

[]{#New_Feature} New Feature
----------------------------

-   \[[STR-1](http://yellowgrass.org/STR-1)\] - if-then-else operator
-   \[[STR-19](http://yellowgrass.org/STR-19)\] - Explicit scope
    identification for dynamic rules to replace \'override rules\'
    construct: rules(f)(Inline : Call(f, es) -\> \...)
-   \[[STR-24](http://yellowgrass.org/STR-24)\] - Passing Hashtables
    around in Stratego, without table table
-   \[[STR-68](http://yellowgrass.org/STR-68)\] - switch-case construct
-   \[[STR-72](http://yellowgrass.org/STR-72)\] - Library support for
    ATerm placeholders

[]{#Task} Task
--------------

-   \[[STR-4](http://yellowgrass.org/STR-4)\] - Verify Microsoft Windows
    support in buildfarm
-   \[[STR-21](http://yellowgrass.org/STR-21)\] - Define meta transition
    markers in separate module stratego-front/sig (now in meta-explode).
-   \[[STR-22](http://yellowgrass.org/STR-22)\] - Clean up RPM spec file
    for ATerm and submit it to CWI for inclusion in their distribution
-   \[[STR-28](http://yellowgrass.org/STR-28)\] - Update and minimize
    README files of subpackages (and toplevel!)
-   \[[STR-29](http://yellowgrass.org/STR-29)\] - Change
    \--with-stratego-xt flag to \--with-strategoxt
-   \[[STR-45](http://yellowgrass.org/STR-45)\] - Include negative
    regression tests in compiler
-   \[[STR-71](http://yellowgrass.org/STR-71)\] - Remove
    [SDF](SDF){.twikiLink} 2.1. Update **every** tool to the most recent
    [SDF](SDF){.twikiLink} syntax.
-   \[[STR-78](http://yellowgrass.org/STR-78)\] - Remove
    [SDF](SDF){.twikiLink} signatures from asfix-tools. Improve
    [AsFix[^?^](http://www.program-transformation.org/edit/Stratego/AsFix?topicparent=Stratego.StrategoRelease010Issues)]{.twikiNewLink
    style="background : #FFFFCE;"} signature.
-   \[[STR-81](http://yellowgrass.org/STR-81)\] - Remove Stratego sigs,
    pp, and syntax definition. Use stratego-front.

[]{#Improvement} Improvement
----------------------------

-   \[[STR-18](http://yellowgrass.org/STR-18)\] - Application of
    \"extend dynamic rules\" should try all dynamic rules and not just
    the top of the stack
-   \[[STR-32](http://yellowgrass.org/STR-32)\] - Rewrite table-table
    strategies in terms of the new table primitives.
-   \[[STR-34](http://yellowgrass.org/STR-34)\] - Separate and improved
    pretty-print table for SDF2-pgen2.x
-   \[[STR-39](http://yellowgrass.org/STR-39)\] - ppgen outputs an
    unclear message when constructors are missing
-   \[[STR-41](http://yellowgrass.org/STR-41)\] - unpack-sdf: move to
    sdf-front and use new sdf syntax and pretty-printer
-   \[[STR-44](http://yellowgrass.org/STR-44)\] - Redesign dynamic rules
-   \[[STR-56](http://yellowgrass.org/STR-56)\] - Allow // EOF
-   \[[STR-57](http://yellowgrass.org/STR-57)\] - Use pgen 2.0
    [SDF](SDF){.twikiLink} syntax in sdf-cons
-   \[[STR-61](http://yellowgrass.org/STR-61)\] - remove
    AC\_FUNC\_MALLOC from srts/configure.in
-   \[[STR-73](http://yellowgrass.org/STR-73)\] - Support placeholders
    in pp-aterm
-   \[[STR-77](http://yellowgrass.org/STR-77)\] - Improve translation of
    list constructs in RTG to sig

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
