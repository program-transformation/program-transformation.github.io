::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

[![](../pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Transform/RigiRSFSpecification?t=1536826555)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/RigiRSFSpecification)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/RigiRSFSpecification)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/RigiRSFSpecification?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/RigiRSFSpecification?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/RigiRSFSpecification?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/RigiRSFSpecification)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/RigiRSFSpecification?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/RigiRSFSpecification?template=oopsmore&param1=1.1&param2=1.1)
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
Rigi RSFSpecification {#rigi-rsfspecification .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

The original specification was posted in the Rigi mailing list (now
defunct):
<http://www.rigi.csc.uvic.ca/list-archives/rigi-developer-archive/2000-02-10-15.26.16-19165>

    ---------- Forwarded message ----------
    Date: Thu, 19 Aug 1999 11:58:34 -0700 (PDT)
    From: Johannes Martin <jmartin@csr.csc.uvic.ca>
    To: cliffmcc@csr, edwardyu@csr, hausi@csr, ianmunro@csr, jpettit@csr, kenw@csr,
         mingdu@csr, mstorey@csr, mwang@csr, pingyu@csr, pkaminsk@gulf, shadian@csr,
         tracywen@csr, veronica@csr, wintb@csr, wjw@csr, tsysta@csr.csc.uvic.ca
    Subject: RSF file format
    Resent-Date: Thu, 10 Feb 2000 23:21:38 +0000 (GMT)
    Resent-From: Johannes Martin <jmartin@csr.csc.uvic.ca>
    Resent-To: rigi-developer-archive@rigi.uvic.ca
    Resent-Subject: RSF file format

    Hi folks,

    while discussing the various RSF file formats with Jamie yesterday, we
    noticed once again that RSF is not properly documented (in particular the
    various structured formats).

    Below is an attempt to write up a more or less formal definition of the
    various RSF formats, as well as a proposal on how to fix some of the
    deficiencies of unstructured RSF.

    Also included is a list showing which tool supports which format.

    I invite you to submit your comments and suggestions.

    Johannes

    P.S.: I hereby call for volunteers to document the format of Rigi view
           files.

    =====================================================================

    RSF format description:
    -----------------------

    In the productions:
    - literals are in double quotes,
    - regular expressions are unquoted,
    - \n denotes newline character,
    - whitespace can be either space or tab,
    - <...> referes to a non-literal


    1. Unstructured RSF:
    --------------------

    rsf-file:      <rsf-tuples>

    rsf-tuples:      <rsf-tuple>
              <rsf-tuple> \n <rsf-tuples>
              <comment> \n <rsf-tuples>
              \n <rsf-tuples>

    comment:       ^#.*$

    rsf-tuple:      <node-definition>
              <arc-definition>
              <attribute-definition>

    node-definition:   "type" <node-spec> <node-type>

    arc-definition:      <arc-type> <node-spec> <node-spec>

    attribute-definition:   <attribute-type> <node-spec> <attribute-value>

    node-spec:      <identifier>
    node-type:      <identifier>
    arc-type:      <identifier>
    attribute-type:      <identifier>
    attribute-value:   <identifier>

    identifier:      [^[[:space:]]]+
              "[^"]+"


    2. Partly structured RSF (differences from 1.):
    --------------------------------------------------
    rigiedit

    node-spec:      <node-ID>!<identifier>

    node-ID:      [1-9][0-9]*

    Reserved node identifiers: "Root" (the root node of the graph)
    Reserved arc types: "level" (connect parent to children nodes)


    3. Stuctured RSF (differences from 2.):
    ------------------------------------------

    node-definition:   n!type <node-spec> <node-type>

    arc-definition:      a!<arc-type> <node-ID>!<arc-ID> <node-spec>

    attributed-definition:  <node-attribute-def>
              <arc-attribute-def>

    node-attribute-def:   n!<attribute-type> <node-spec> <attribute-value>

    arc-attribute-def:   a!<attribute-type> <arc-ID> <attribute-value>

    arc-ID:         [1-9][0-9]*


    4. 4-tuple unstructured RSF (differences from 1.):
    --------------------------------------------------

    rsf-tuple:      <rsf-tuple2> <source-location>?

    rsf-tuple2:      <node-definition>
              <arc-definition>
              <attribute-definition>

    source-location:   <file-name>";"<line-number>(";"<column-number>)?

    file-name:      identifier
    line-number:      [0-9]+
    column-number:      [0-9]+


    5. Proposal for a better unstructured RSF (differences from 4.):
    ----------------------------------------------------------------

    RSF, and in particular unstructured RSF, has some deficiencies:
    - there is no way to express arc attributes in unstructured RSF
    - and RSF files does not contain domain information
    - strings with embedded double quotes cause problems

    Here is a working proposal on how to fix RSF without breaking existing
    tools:

    a) allow for arc attributes and the possibility to exactly identify nodes/arcs:

    arc-definition:      <arc-type> <node-spec2> <node-spec2>

    attribute-definition:   <attribute-type> <spec> <attribute-value>

    spec:         <arc-spec>
              <node-spec2>

    node-spec2:      <node-spec>
              "("<node-type>","<node-spec>","<node-spec>")"

    arc-spec:      "("<arc-type>","<node-spec2>","<node-spec2>")"

    identifier:      [^[[:space:]],()]+
              "[^"]+"
              '[^']+'
              `[^`]+`

    b) include domain definition:

    rsf-file:      <domain-definition>
              <rsf-tuples>

    domain-definition:   <nodetype-definition>
              <arctype-definition>
              <attrtype-definition>

    nodetype-definition:   "type" <node-type> "nodetype"
    arctype-definition:   "type" <arc-type> "arctype"
    attrtype-definition:   "type" <attribute-type> "attrtype"

    Your comments and suggestions for this proposal are appreciated.


    Appendix: Tool support
    ----------------------
    Here's a list showing which of our tools supports which of the above
    formats:

                    | Support for ... RSF:
    Tool           | unstructured | partly structured | structured | 4-tuple
    ---------------+--------------+-------------------+------------+-----------
    C parser       | write        |                   |            | write
    Java parser    | write        |                   |            |
    C++ parser     |              |                   |            | write
    sortrsf        | read/write   |                   |            | read/write
    htmlrsf        | read/write   |                   |            | read/write
    rigiedit       | read         | read              | write      |

------------------------------------------------------------------------

[CategoryRigi](CategoryRigi){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
