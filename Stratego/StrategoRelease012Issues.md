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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoRelease012Issues?t=1536825680)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoRelease012Issues)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoRelease012Issues)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoRelease012Issues?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoRelease012Issues?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoRelease012Issues?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease012Issues?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoRelease012Issues?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoRelease012Issues)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease012Issues?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoRelease012Issues?template=oopsmore&param1=1.2&param2=1.2)
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
Stratego Release 012 Issues {#stratego-release-012-issues .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Issues closed and resolved in [StrategoXT
0.12](StrategoRelease012){.twikiLink}

[]{#Bug} Bug
------------

-   \[[STR-90](https://catamaran.labs.cs.uu.nl/jira/browse/STR-90)\] -
    sdf2rtg (or maybe just pp-rtg) does not support quoted constructors
-   \[[STR-96](https://catamaran.labs.cs.uu.nl/jira/browse/STR-96)\] -
    Generic application of dynamic rewrite rule
-   \[[STR-140](https://catamaran.labs.cs.uu.nl/jira/browse/STR-140)\] -
    pack-sdf does not check that module name corresponds to file name
-   \[[STR-152](https://catamaran.labs.cs.uu.nl/jira/browse/STR-152)\] -
    format-check \--xhtml: in worstcase pp list format errors are not
    red.
-   \[[STR-153](https://catamaran.labs.cs.uu.nl/jira/browse/STR-153)\] -
    format-check \--vis: list format errors are not red.
-   \[[STR-155](https://catamaran.labs.cs.uu.nl/jira/browse/STR-155)\] -
    sdf2parenthesize: must use transitive closure of chain priorities
-   \[[STR-161](https://catamaran.labs.cs.uu.nl/jira/browse/STR-161)\] -
    pack-sdf: fix .dep generation support
-   \[[STR-187](https://catamaran.labs.cs.uu.nl/jira/browse/STR-187)\] -
    sdf2ast-conflicts: injections result in illegal conflict
    descriptions.

[]{#New_Feature} New Feature
----------------------------

-   \[[STR-131](https://catamaran.labs.cs.uu.nl/jira/browse/STR-131)\] -
    pack-sdf should search directory of input file for modules.
-   \[[STR-149](https://catamaran.labs.cs.uu.nl/jira/browse/STR-149)\] -
    Remove built-in tuple nonterm and replace by built-in terminals 1,
    2, etc.
-   \[[STR-166](https://catamaran.labs.cs.uu.nl/jira/browse/STR-166)\] -
    asfix-anno-comment: add argument for comment sort names.
-   \[[STR-169](https://catamaran.labs.cs.uu.nl/jira/browse/STR-169)\] -
    if then end
-   \[[STR-181](https://catamaran.labs.cs.uu.nl/jira/browse/STR-181)\] -
    xml-info2data: support the \--very-explicit mode of data2xml-doc

[]{#Task} Task
--------------

-   \[[STR-167](https://catamaran.labs.cs.uu.nl/jira/browse/STR-167)\] -
    Remove obsolete \'display\' strategies in module tables.
-   \[[STR-171](https://catamaran.labs.cs.uu.nl/jira/browse/STR-171)\] -
    Use the improved autoxt.m4 contributed by Akim
-   \[[STR-182](https://catamaran.labs.cs.uu.nl/jira/browse/STR-182)\] -
    Create a testsuite for the \--explicit mode used by xml2aterm and
    aterm2xml
-   \[[STR-183](https://catamaran.labs.cs.uu.nl/jira/browse/STR-183)\] -
    aterm2xml \--very-explicit: create a RELAX NG schema for the XML of
    this mode.

[]{#Improvement} Improvement
----------------------------

-   \[[STR-38](https://catamaran.labs.cs.uu.nl/jira/browse/STR-38)\] -
    ast2abox should use the arity of a constructor when looking for
    pp-entries.
-   \[[STR-53](https://catamaran.labs.cs.uu.nl/jira/browse/STR-53)\] -
    Support nested block comments /\* /\* \*/ \*/
-   \[[STR-99](https://catamaran.labs.cs.uu.nl/jira/browse/STR-99)\] -
    treeviz contains a signature of
    [GraphXML[^?^](http://www.program-transformation.org/edit/Stratego/GraphXML?topicparent=Stratego.StrategoRelease012Issues)]{.twikiNewLink
    style="background : #FFFFCE;"}. Use graph-tools.
-   \[[STR-102](https://catamaran.labs.cs.uu.nl/jira/browse/STR-102)\] -
    Lift the open-file table to the Stratego level by using the new
    hashtable pointers.
-   \[[STR-104](https://catamaran.labs.cs.uu.nl/jira/browse/STR-104)\] -
    gen-renamed-sdf-module: declare the new sorts
-   \[[STR-147](https://catamaran.labs.cs.uu.nl/jira/browse/STR-147)\] -
    format-check: improve error reporting and effiency
-   \[[STR-151](https://catamaran.labs.cs.uu.nl/jira/browse/STR-151)\] -
    sdf2rtg: use more attractive generated non terminal names
-   \[[STR-156](https://catamaran.labs.cs.uu.nl/jira/browse/STR-156)\] -
    Make syntax \'Stratego\' the default for pp-stratego-latex-alltt
-   \[[STR-157](https://catamaran.labs.cs.uu.nl/jira/browse/STR-157)\] -
    temp-dir: prefer environment variable TMPDIR
-   \[[STR-159](https://catamaran.labs.cs.uu.nl/jira/browse/STR-159)\] -
    Auto-trim counter-part of \`newname\'-input for use as prefix
-   \[[STR-162](https://catamaran.labs.cs.uu.nl/jira/browse/STR-162)\] -
    pack-sdf: report importing module for missing [SDF](SDF){.twikiLink}
    moulde
-   \[[STR-163](https://catamaran.labs.cs.uu.nl/jira/browse/STR-163)\] -
    pack-sdf: -I option, warn if directory does not exist or value is
    not a directory.
-   \[[STR-173](https://catamaran.labs.cs.uu.nl/jira/browse/STR-173)\] -
    parse-unit must accept testsuites in concrete syntax.
-   \[[STR-174](https://catamaran.labs.cs.uu.nl/jira/browse/STR-174)\] -
    parse-unit: support the execution of a single test.
-   \[[STR-176](https://catamaran.labs.cs.uu.nl/jira/browse/STR-176)\] -
    Add a composition of data2xml-doc and pp-xml-doc.
-   \[[STR-177](https://catamaran.labs.cs.uu.nl/jira/browse/STR-177)\] -
    Support a \'naive\' roundtrip from aterm to xml.
-   \[[STR-180](https://catamaran.labs.cs.uu.nl/jira/browse/STR-180)\] -
    parse-unit: still uses local tmp files (which are not removed)

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
