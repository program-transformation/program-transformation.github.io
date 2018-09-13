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
    Page](http://www.program-transformation.org/edit/Sdf/SdfDevelopment?t=1536825748)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sdf/SdfDevelopment)
-   [Attach
    File](http://www.program-transformation.org/attach/Sdf/SdfDevelopment)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sdf/SdfDevelopment?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sdf/SdfDevelopment?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/Sdf/SdfDevelopment?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Sdf/SdfDevelopment?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Sdf/SdfDevelopment?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Sdf/SdfDevelopment?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Sdf/SdfDevelopment?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Sdf/SdfDevelopment?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sdf/SdfDevelopment)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sdf/SdfDevelopment?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/Sdf/SdfDevelopment?template=oopsmore&param1=1.8&param2=1.8)
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
Sdf Development {#sdf-development .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Sdf
:::

SDF is an open-source project under the
[BSDLicense](BSDLicense){.twikiLink}.

### []{#Contributing} Contributing

-   Please contribute bug reports, patches, and ideas for enhancement
    using our [BugZilla
    instance](http://bugzilla.sen.cwi.nl:8080/index.cgi). Thank you!
-   If you would like to contribute a new component to the SDF project,
    or you would like to become a committer on existing SDF software,
    please contant [Jurgen Vinju](mailto:jurgen.vinju@cwi.nl).
    -   We are always interested in finding new colleagues!
    -   We are always interested in add-ons and tools that support SDF
        grammar engineering. If you have made a valuable tool for SDF,
        we invite you to apply for hosting it on syntax-definition.org.

[]{#People} People
------------------

### []{#Maintainers} Maintainers

SDF is an open source project, originating from [CWI](http://www.cwi.nl)
in the Netherlands as part of [The
Meta-Environment](http://www.meta-environment.org). It is an independent
piece of software now, developed by and contributed to by several people
from CWI, TU Eindhoven, TU Delft and others.

The current developers/maintainers are:

-   [PGEN](PGEN){.twikiLink} (SDF parse table generator)
    -   Rob Economopoulos
    -   Mark van den Brand
    -   Jurgen Vinju

<!-- -->

-   [SGLR](SGLR){.twikiLink} (SDF parse table interpreter, \"the
    parser\")
    -   Rob Economopoulos
    -   Jurgen Vinju
    -   Mark van den Brand

<!-- -->

-   [SDF2 Bundle](SdfBundle){.twikiLink}
    -   [Martin Bravenboer](http://martin.bravenboer.name) (Delft
        University of Technology)

Also note that SDF depends on other open source software such as the
ATerm library and the UPTR (pt-support) parse forest representation
library. For details about these components, please visit
<http://www.meta-environment.org>. Any full SDF distribution
**includes** these components, which are also open-source and released
under the same license.

### []{#Contributors} Contributors

Several people have contributed significantly to SDF:

-   Merijn de Jonge
-   Paul Klint
-   Eelco Visser
-   Jeroen Scheerder
-   Pieter Olivier
-   Hayco de Jong
-   Taeke Kooiker

Also note that previous versions of SDF (as implemented in Centaur LISP)
have been done by other people:

-   [See the Meta-Environment hall of
    fame](http://www.cwi.nl/htbin/sen1/twiki/bin/view/Meta-Environment/Contributing)

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
