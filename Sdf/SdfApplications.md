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
    Page](http://www.program-transformation.org/edit/Sdf/SdfApplications?t=1536825748)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sdf/SdfApplications)
-   [Attach
    File](http://www.program-transformation.org/attach/Sdf/SdfApplications)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sdf/SdfApplications?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sdf/SdfApplications?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Sdf/SdfApplications?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Sdf/SdfApplications?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Sdf/SdfApplications?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Sdf/SdfApplications?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Sdf/SdfApplications?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Sdf/SdfApplications?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sdf/SdfApplications)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sdf/SdfApplications?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Sdf/SdfApplications?template=oopsmore&param1=1.6&param2=1.6)
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
Sdf Applications {#sdf-applications .twikiTopicTitle}
================

::: {.twikiWebTitle}
Sdf
:::

SDF is used by many individuals for many different purposes. This page
lists the original applications of SDF and some of its premier
applications.

The SDF syntax definition formalism is applied in two projects related
to meta programming: the ASF+SDF Meta-Environment and Stratego/XT.
Companies and researchers are using these environments for implementing
various (source-to-source) program transformations.

[]{#ASF_SDF_Meta_Environment} ASF+SDF Meta-Environment
------------------------------------------------------

The [ASF+SDF Meta-Environment](http://www.meta-environment.org) is
applied for the description of syntax, semantics, analysis, and
transformation of (programming) languages and programs written in such
programming languages. As the name suggests, SDF originated as a
component of the ASF+SDF Meta-Environment.

The Meta-Environment uses SDF to parse input source code and to
implement concrete syntax for source code patterns. The patterns are
part of rewrite rules (equation) in the ASF formalism. ASF is used to
implement source-to-source transformations, source analyses, compilers
and interpreters.

More information can be found at <http://www.meta-environment.org>

[]{#Stratego_XT} Stratego/XT
----------------------------

Stratego/XT is the combination of the The [Stratego program
transformation
language[^?^](http://www.program-transformation.org/edit/Sdf/Strategoxtorg?topicparent=Sdf.SdfApplications)]{.twikiNewLink
style="background : #FFFFCE;"} for strategic rewriting and the XT bundle
of transformation tools.

In Stratego/XT SDF is used to define the syntax of (programming)
languages and to generate tools like pretty-printers from these
definitions. The power of SDF becomes especially clear in the use of
concrete object syntax. This technique is applied by many Stratego/XT
applications. At the Stratego/XT web you can find a list of applications
of Stratego/XT.

[]{#Rascal} Rascal
------------------

[Rascal](http://www.rascal-mpl.org) is a domain specific language for
source code analysis, transformation and generation. It was bootstrapped
using SDF and used SDF as a method for implementing parsers for object
languages and for concrete syntax patterns. Currently Rascal implements
embeds syntax definitions, very much like SDF2 but it is not using the
SDF2 implementation anymore. Instead Rascal uses a general scannerless
top-down parsing algorithm which is completely Java based.

[]{#Software_Improvement_Group}[]{#Software_Improvement_Group_} Software Improvement Group.
-------------------------------------------------------------------------------------------

The [Software Improvement Group](http://www.sig.nl) is a spin-off of the
Dutch National Centre for Mathematics and Computer Science (CWI). The
SIG is active in all fields of software renovation: the adaptation,
integration and rebuilding of existing software systems. Currently the
SIG provides services for documentation heneration, portfolio
monitoring, risk assessments and migrations.

[]{#First_Result} First Result
------------------------------

The company [First Result](http://www.firstresult.nl) applies SDF
technology in the ASF+SDF Meta-Environment for the generation of code.

[]{#EPITA_Research_Development_Labor} EPITA Research & Development Laboratory
-----------------------------------------------------------------------------

The [EPITA Research & Development Laboratory](http://www.lrde.epita.fr/)
has developed C and C++ grammars in the [Transformers
Project](http://www.lrde.epita.fr/cgi-bin/twiki/view/Projects/Transformers).
Disambiguation of C++ is performed on parse trees. Stratego/XT tools are
used to implement parse and abstract syntax tree transformations.

-\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
