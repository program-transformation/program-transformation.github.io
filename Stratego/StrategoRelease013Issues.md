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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease013Issues?t=1536825680)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease013Issues)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease013Issues)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease013Issues?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease013Issues?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoRelease013Issues?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease013Issues)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease013Issues?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease013Issues?template=oopsmore&param1=1.1&param2=1.1)
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
Stratego Release 013 Issues {#stratego-release-013-issues .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Issues for [StrategoXT 0.13](StrategoRelease013){.twikiLink}.

[]{#Bug} Bug
------------

-   \[[STR-25](https://catamaran.labs.cs.uu.nl/jira/browse/STR-25)\] -
    Appl/2 or Cons/0 is a reserved term?
-   \[[STR-127](https://catamaran.labs.cs.uu.nl/jira/browse/STR-127)\] -
    ambiguity for negative numbers following colon in rules(..)
-   \[[STR-130](https://catamaran.labs.cs.uu.nl/jira/browse/STR-130)\] -
    dr old uses Pair constructor, which is not available in liblib
-   \[[STR-135](https://catamaran.labs.cs.uu.nl/jira/browse/STR-135)\] -
    Redefinition of external s not detected if s is not invoked in
    client code.
-   \[[STR-192](https://catamaran.labs.cs.uu.nl/jira/browse/STR-192)\] -
    sdf2rtg: support nice names for character classes
-   \[[STR-193](https://catamaran.labs.cs.uu.nl/jira/browse/STR-193)\] -
    sdf2rtg: support nice names for literals
-   \[[STR-194](https://catamaran.labs.cs.uu.nl/jira/browse/STR-194)\] -
    sdf2rtg: support literal alternatives
-   \[[STR-200](https://catamaran.labs.cs.uu.nl/jira/browse/STR-200)\] -
    rtg2sig: generates a Cons/1 constructor. Should be Cons/2
-   \[[STR-201](https://catamaran.labs.cs.uu.nl/jira/browse/STR-201)\] -
    Strc: programs that use a Cons/0, Cons/1, or Cons/3+ do not compile
-   \[[STR-203](https://catamaran.labs.cs.uu.nl/jira/browse/STR-203)\] -
    Quoted constructor caching causes illegal C identifier
-   \[[STR-204](https://catamaran.labs.cs.uu.nl/jira/browse/STR-204)\] -
    Congruences of quoted constructors are not desugared
-   \[[STR-205](https://catamaran.labs.cs.uu.nl/jira/browse/STR-205)\] -
    Strc: Programs that use a Nil/1+ constructor do not compile.
-   \[[STR-206](https://catamaran.labs.cs.uu.nl/jira/browse/STR-206)\] -
    Lift-dynamic-rules-old uses dummify of the new new lift-dynamic
    rules
-   \[[STR-209](https://catamaran.labs.cs.uu.nl/jira/browse/STR-209)\] -
    Aterm2xml implicit mode: produces an error for some annos.

[]{#New_Feature} New Feature
----------------------------

-   \[[STR-2](https://catamaran.labs.cs.uu.nl/jira/browse/STR-2)\] -
    Quoted constructors
-   \[[STR-146](https://catamaran.labs.cs.uu.nl/jira/browse/STR-146)\] -
    input option: check for multiple -i at command-line?
-   \[[STR-189](https://catamaran.labs.cs.uu.nl/jira/browse/STR-189)\] -
    sglri: accept flags to disable heuristic filters
-   \[[STR-190](https://catamaran.labs.cs.uu.nl/jira/browse/STR-190)\] -
    parse-stratego: support disabling sglr heuristic filters

[]{#Task} Task
--------------

-   \[[STR-23](https://catamaran.labs.cs.uu.nl/jira/browse/STR-23)\] -
    Make check fails at AIX/Power4
-   \[[STR-150](https://catamaran.labs.cs.uu.nl/jira/browse/STR-150)\] -
    Declare iowrap obsolete
-   \[[STR-202](https://catamaran.labs.cs.uu.nl/jira/browse/STR-202)\] -
    autoxt.m4: accept a flag \--with-strategoxt-util

[]{#Improvement} Improvement
----------------------------

-   \[[STR-148](https://catamaran.labs.cs.uu.nl/jira/browse/STR-148)\] -
    New dynamic rules: use a more special dummy
-   \[[STR-158](https://catamaran.labs.cs.uu.nl/jira/browse/STR-158)\] -
    strc \--version: use a C macro instead of generated .str module
-   \[[STR-191](https://catamaran.labs.cs.uu.nl/jira/browse/STR-191)\] -
    strc should report ambs and fail
-   \[[STR-207](https://catamaran.labs.cs.uu.nl/jira/browse/STR-207)\] -
    Needed-defs: refactor to new dr :+ feature.
-   \[[STR-208](https://catamaran.labs.cs.uu.nl/jira/browse/STR-208)\] -
    Sdf2rtg: use concrete syntax for [SDF](SDF){.twikiLink} in error
    reports.
-   \[[STR-212](https://catamaran.labs.cs.uu.nl/jira/browse/STR-212)\] -
    Ppgen: error reporting of [SDF](SDF){.twikiLink} productions is
    broken
-   \[[STR-221](https://catamaran.labs.cs.uu.nl/jira/browse/STR-221)\] -
    bootstrap scripts: use autoreconf
-   \[[STR-222](https://catamaran.labs.cs.uu.nl/jira/browse/STR-222)\] -
    configure.ac: share config aux files by using AC\_CONFIG\_AUX\_DIR
-   \[[STR-223](https://catamaran.labs.cs.uu.nl/jira/browse/STR-223)\] -
    All macros in autoxt.m4 should use the XT prefix.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
