::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[SDF Home](WebHome){.twikiLink}**

-   [About](SdfLanguage){.twikiLink}
-   [Documentation](SdfDocumentation){.twikiLink}
-   [Publications](SdfPublications){.twikiLink}
-   [Download](SdfSoftware){.twikiLink}
-   [Grammars](SdfGrammars){.twikiLink}

**Users**

-   [Applications](SdfApplications){.twikiLink}
-   [Mailing Lists](MailingList){.twikiLink}
-   [ASF+SDF Users
    Day](http://www.cwi.nl/htbin/sen1/twiki/bin/view/SEN1/ASFSDFUsersDay)
-   [Stratego Users Day](../Stratego/StrategoUsersDay){.twikiLink}

**Development**

-   [Organization](SdfDevelopment){.twikiLink}
-   [Reporting Bugs](SdfBugs){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/SdfBackup/SdfDevelopment?t=1536827696)
-   [Rename
    Page](http://www.program-transformation.org/rename/SdfBackup/SdfDevelopment)
-   [Attach
    File](http://www.program-transformation.org/attach/SdfBackup/SdfDevelopment)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/SdfBackup/SdfDevelopment?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/SdfBackup/SdfDevelopment?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/SdfBackup/SdfDevelopment?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/SdfBackup/SdfDevelopment?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/SdfBackup/SdfDevelopment?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/SdfBackup/SdfDevelopment?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/SdfBackup/SdfDevelopment?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/SdfBackup/SdfDevelopment?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/SdfBackup/SdfDevelopment)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/SdfBackup/SdfDevelopment?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/SdfBackup/SdfDevelopment?template=oopsmore&param1=1.5&param2=1.5)
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
Development {#development .twikiTopicTitle}
===========

::: {.twikiWebTitle}
SDF: Modular Syntax Definition Formalism
:::

The SDF parser generator and [SGLR](SGLR){.twikiLink} are an open source
project, released with a BSD license.

[]{#Reporting_Bugs} Reporting Bugs
----------------------------------

The SDF bugzilla system is located here. Use the package \'sglr\' and
\'pgen\' to report bugs in the core SDF system. \'sdf-meta\' for IDE
bugs and \'unknown\' if you just don\'t know.

-   [bugzilla](http://bugzilla.sen.cwi.nl:8080/index.cgi)

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

Also not that SDF depends on other open source software such as the
ATerm library and the UPTR (pt-support) parse forest representation
library.

### []{#Contributors} Contributors

-   Merijn de Jonge
-   Paul Klint
-   Eelco Visser
-   Jeroen Scheerder
-   Karl Trygve Kalleberg

Also not that previous versions of SDF (as implemented in Centaur LISP)
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
