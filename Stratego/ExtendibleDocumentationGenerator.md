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
    Page](http://www.program-transformation.org/edit/Stratego/ExtendibleDocumentationGenerator?t=1536825468)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ExtendibleDocumentationGenerator)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ExtendibleDocumentationGenerator)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ExtendibleDocumentationGenerator?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ExtendibleDocumentationGenerator?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    40](http://www.program-transformation.org/view/Stratego/ExtendibleDocumentationGenerator?rev=1.40)
    [(diff 39)](http://www.program-transformation.org/rdiff/Stratego/ExtendibleDocumentationGenerator?rev1=1.40&rev2=1.39)
-   [Rev
    39](http://www.program-transformation.org/view/Stratego/ExtendibleDocumentationGenerator?rev=1.39)
    [(diff 38)](http://www.program-transformation.org/rdiff/Stratego/ExtendibleDocumentationGenerator?rev1=1.39&rev2=1.38)
-   [Rev
    38](http://www.program-transformation.org/view/Stratego/ExtendibleDocumentationGenerator?rev=1.38)
    [(diff 37)](http://www.program-transformation.org/rdiff/Stratego/ExtendibleDocumentationGenerator?rev1=1.38&rev2=1.37)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ExtendibleDocumentationGenerator)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ExtendibleDocumentationGenerator?template=oopsmore&param1=1.40&param2=1.40)
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
    \...](http://www.program-transformation.org/oops/Stratego/ExtendibleDocumentationGenerator?template=oopsmore&param1=1.40&param2=1.40)
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
Extendible Documentation Generator {#extendible-documentation-generator .twikiTopicTitle}
==================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

xDoc: generate documentation for Stratego specifications

### []{#General} General

[Rob Vermaas](../Main/RobVermaas){.twikiLink} is working at the moment
on xDoc. Examples of generated documentation can be found at
<http://catamaran.labs.cs.uu.nl/docs/>.

### []{#Features} Features

-   Several kinds of indices
-   Pretty-printed, browsable code
-   Import graphs
-   [XTC](XTC){.twikiLink} visualization : Stratego applications consist
    of a number of transformation components glued together using
    [XTC](XTC){.twikiLink}. For program understanding it would be useful
    to extract the high-level data-flow graph of applications, i.e.,
    reduce an [XTC](XTC){.twikiLink} composition to a data-flow graph of
    component calls.

### []{#Most_wanted_features} Most wanted features

If you have a nice feature that you would like, please don\'t hesitate
to put it here.

-   Category views (see [message on
    stratego-dev](https://mail.cs.uu.nl/pipermail/stratego-dev/2003q2/000347.html))

<!-- -->

-   Index on specific attributes (related to category views). In my
    Stratego I\'m already using caps lock TODO comments to remind me of
    minor issues in the code. Visual Studio also
    [supports](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/vsent7/html/vxconCreatingTaskReminders.asp)
    this. todo attributes in xdoc comments could be used for this. How
    to get an overview of these attributes?
    -   also \@see, \@since, \@param

<!-- -->

-   Search: some kind of interactive search method that allows finding
    an appropriate strategy for some task.

<!-- -->

-   Another level of documentation is documentation of the use of
    components. One could say this is *user* documentation, but in XT
    components are used by developers to create transformation systems
    just as strategy definitions in the library are. It would be useful
    to have an API-like presentation of components derived from the
    source code. A description of the component could for example be
    included in an xdoc comment in front of the \'main\' or \'io-\...\'
    definition.

<!-- -->

-   When including tests in generated documentation, it might be clearer
    if all test modules are grouped into a (possibly bordered) subgraph
    in the dependency graphs.

<!-- -->

-   Highlight \'normal\' documentation as well (instead of plain black,
    as the rest of the code)

### []{#Known_bugs} Known bugs

-   When certain files cannot be parsed, xDoc gives unclear error
    messages.

### []{#Latest_sources} Latest sources

You can get the latest sources from the Subversion repository:

      svn checkout https://svn.strategoxt.org/repos/StrategoXT/xdoc/trunk

### []{#Related} Related

-   graph visualizations
    -   [Da Vinci](http://www.b-novative.com),
        [Graphviz](http://www.research.att.com/sw/tools/graphviz),
        [H3viewer](http://graphics.stanford.edu/~munzner/h3),
        [Walrus](http://www.caida.org/tools/visualization/walrus/)
-   Similar documentation generation systems
    -   [Docbuilder](http://www.docbuilder.de),
        [Docgen](http://www.software-improvers.com/DocGen.htm),
        [Doc-o-matic](http://www.doc-o-matic.com), [Imagix
        4d](http://www.imagix.com),
        [Javadoc](http://java.sun.com/j2se/javadoc/),
        [Haddock](http://www.haskell.org/haddock/), [Rigi
        System](http://www.rigi.csc.uvic.ca), [The Software
        Bookshelf](http://www.research.ibm.com/journal/sj/364/finnigan.html),
        [Python Documentation Utilities
        Project](http://docutils.sourceforge.net/)

------------------------------------------------------------------------

[CategoryToDo[^?^](http://www.program-transformation.org/edit/Stratego/CategoryToDo?topicparent=Stratego.ExtendibleDocumentationGenerator)]{.twikiNewLink
style="background : #FFFFCE;"} \|
[StrategoUtilities](StrategoUtilities){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.ExtendibleDocumentationGenerator moved from
Stratego.StrategoDoc on 19 Jun 2003 - 07:59 by
[RobVermaas](../Main/RobVermaas){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Stratego/ExtendibleDocumentationGenerator?newweb=Stratego&newtopic=StrategoDoc&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
