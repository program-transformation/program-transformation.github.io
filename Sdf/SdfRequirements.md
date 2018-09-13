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
    Page](http://www.program-transformation.org/edit/Sdf/SdfRequirements?t=1536826616)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sdf/SdfRequirements)
-   [Attach
    File](http://www.program-transformation.org/attach/Sdf/SdfRequirements)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sdf/SdfRequirements?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sdf/SdfRequirements?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Sdf/SdfRequirements?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sdf/SdfRequirements?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Sdf/SdfRequirements?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sdf/SdfRequirements)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sdf/SdfRequirements?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Sdf/SdfRequirements?template=oopsmore&param1=1.2&param2=1.2)
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
Sdf Requirements {#sdf-requirements .twikiTopicTitle}
================

::: {.twikiWebTitle}
Sdf
:::

The design of SDF is the result of a number of requirements. This page
discusses these requirements.

**Completeness of Syntax Definition**

All aspects of the syntax of a language are defined in one specification
and in one formalism. This entails that lexical syntax, context-free
syntax and disambiguation information are all specified in the same
formalism.

In contrast to LEX/YACC where lexical and context-free syntax are
defined in separate formalisms.

**Orthogonality**

Features that are available for some type of expression in one context
should be available for that type of expression in another context as
well and should mean the same thing.

For example, the iteration construct {A B}\* should mean the same thing
when used in lexical syntax or context-free syntax.

**Modular**

It should be possible to extend a syntax definition with additional
productions, i.e., syntax definitions should be modular.

**Expressive**

Frequently occurring syntax patterns such as lists and optionals should
not have to be defined every time. In other words SDF should support the
common extensions of Extended BNF.

**Extensible**

The formalism itself should be extensible. It should possible to add
some new abstractions to the formalism.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Sdf.SdfRequirements moved from Tools.SdfRequirements on 09 Feb 2004 -
14:42 by [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* -
[put it
back](http://www.program-transformation.org/rename/Sdf/SdfRequirements?newweb=Tools&newtopic=SdfRequirements&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
