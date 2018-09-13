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
    Page](http://www.program-transformation.org/edit/Sdf/SdfLanguage?t=1536825746)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sdf/SdfLanguage)
-   [Attach
    File](http://www.program-transformation.org/attach/Sdf/SdfLanguage)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sdf/SdfLanguage?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sdf/SdfLanguage?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Sdf/SdfLanguage?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Sdf/SdfLanguage?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Sdf/SdfLanguage?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Sdf/SdfLanguage?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Sdf/SdfLanguage?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Sdf/SdfLanguage?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sdf/SdfLanguage)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sdf/SdfLanguage?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Sdf/SdfLanguage?template=oopsmore&param1=1.6&param2=1.6)
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
Sdf Language {#sdf-language .twikiTopicTitle}
============

::: {.twikiWebTitle}
Sdf
:::

[]{#Overview} Overview
----------------------

The SDF syntax definition formalism allows a concise and natural
expression of the syntax of a context-free language. SDF integrates
lexical and context-free syntax in a single syntax formalism. The
complete syntax of a language is thus defined in a single definition.
SDF supports arbitrary context-free grammars. Therefore, SDF does not
restrict the grammars to a subclass of the context-free grammars, such
as LL or LALR. SDF syntax definitions can be modular. SDF modules can be
reused in different syntax definitions. Disambiguation of grammars is
not done by grammar hacking, but by applying special purpose
disambiguation facilities in SDF, such as priorities, reject
productions, and follow restrictions.

SDF is a declarative language. This means that a syntax definition can
be used for different purposes then the usual application: the
generation of a parser. Instead, SDF syntax definitions can be used to
generate other tools from syntax definitions, e.g. pretty-printers and
data type definitions.

[]{#Language_Features} Language Features
----------------------------------------

-   Modules
-   Integration of lexical and context-free syntax
-   Character classes
-   Regular expressions
-   Disambiguation by relative priorities
-   Disambiguation by associativity
-   Disambiguation by preference
-   Aliases
-   Renaming and parameterization of modules
-   Lookahead restrictions
-   Reject productions
-   Case-insensitive keywords

[]{#Design_Features} Design Features
------------------------------------

Implementers of SDF2 will appreciate its orthogonality. Language
features are defined, as much as possible, orthogonal with respect to
each other. Despite providing a rich formalism at the level of the user
language, the implementation only has to work on a small kernel
formalism to which syntax definitions are transformed. Most features are
expressed by a translation to the kernel formalism, which is performed
by the SDF normalizer.

All symbols are first-class. For example, symbols can be used at the
right-hande side of a production. This means that it is possible to
define production rules that construct lists of symbols, optional
symbols, and even literals.

[]{#Implementation_Features} Implementation Features
----------------------------------------------------

![](http://www.cwi.nl/themes/sen1/twiki/pub/Meta-Environment/SDF/parse-architecture.png)

-   Parser generation: SLR1 with special treatment of priorities
-   [Scannerless Generalized LR](ScannerlessGeneralizedLR){.twikiLink}
    no separate scanner needed

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Sdf.SdfLanguage moved from Tools.FeaturesOfSDF2 on 24 Jan 2004 - 17:11
by [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Sdf/SdfLanguage?newweb=Tools&newtopic=FeaturesOfSDF2&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
