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
    Page](http://www.program-transformation.org/edit/Sdf/SdfRelatedSoftware?t=1536825748)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sdf/SdfRelatedSoftware)
-   [Attach
    File](http://www.program-transformation.org/attach/Sdf/SdfRelatedSoftware)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sdf/SdfRelatedSoftware?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sdf/SdfRelatedSoftware?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Sdf/SdfRelatedSoftware?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sdf/SdfRelatedSoftware?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Sdf/SdfRelatedSoftware?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sdf/SdfRelatedSoftware)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sdf/SdfRelatedSoftware?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Sdf/SdfRelatedSoftware?template=oopsmore&param1=1.2&param2=1.2)
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
Sdf Related Software {#sdf-related-software .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Sdf
:::

[]{#Related_Software} Related Software
--------------------------------------

This page lists known third-party software that is available for SDF

### []{#IDE} IDE

-   [The SDF Meta-Environment is an IDE for
    SDF](http://www.meta-environment.org). It is currently not released
    separatedly from the ASF+SDF Meta-Environment. Contact us if this is
    needed.
-   [The ASF+SDF Meta-Environment is an IDE for
    ASF+SDF](http://www.meta-environment.org). This IDE can be used as
    an IDE for SDF.

### []{#Grammar_manipulation} Grammar manipulation

-   [SDF weaver](http://www.repleo.nl/downloads.html) is a tool for
    merging production attributes into a grammar.

### []{#Code_Generation} Code Generation

-   [ApiGen](http://www.cwi.nl/htbin/sen1/twiki/bin/view/SEN1/ApiGen)
    generates C or Java APIs from an SDF syntax definition.

<!-- -->

-   [Strafunski and Sdf2Haskell](http://www.cs.vu.nl/Strafunski/)
    provide support for generic programming and language processing in
    the functional programming language Haskell. Sdf2Haskell implements
    the derivation of algebraic datatypes from SDF syntax definitions.
    The Haskell ATerm library can be used to import the results of the
    [SGLR](SGLR){.twikiLink} parser.

<!-- -->

-   [HaGLR](http://wiki.di.uminho.pt/wiki/bin/view/PURe/HaGLR) is an
    implementation of Generalized LR parsing in Haskell, and also
    implements an SDF front-end, which is an extension of the
    Sdf2Haskell generator.

<!-- -->

-   [Repleo](http://www.repleo.nl) is a template based code generated
    based on SDF which features static syntactic correctness.

### []{#Pretty_Printer_Generation} Pretty-Printer Generation

-   GPP is a collection of tools for pretty-printing and pretty-printer
    generation. It supports the SDF syntax definition formalism. GPP is
    part of [StrategoXT](http://www.stratego-language.org).
-   Pandora is a pretty printing tool for SDF parse trees. It is
    included in the 2.6 release of SDF. Older versions are part of [The
    Meta-Environment](http://www.meta-environment.org)

### []{#Testing} Testing

-   [parse-unit](../Tools/ParseUnit){.twikiLink} is a tool for
    unit-testing SDF syntax definitions. It is part of
    [StrategoXT](http://www.stratego-language.org).

### []{#Metrics} Metrics

-   [SdfMetz](http://wiki.di.uminho.pt/wiki/bin/view/PURe/SdfMetz) \-- A
    SDF monitoring tool. From the website: *\"is a tool to support
    grammar engineering. It calculates metrics and performs miscellaneus
    analyzes (like output the grammar graph or view the non-singleton
    levels of a grammar). This tool was implemented to fill the gap of
    grammar measuring and analyzes tools.\"*
-   [Meta-Environment](http://www.meta-environment.org) contains a set
    of SDF metrics and visualizations, as inspired by SdfMetz.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
