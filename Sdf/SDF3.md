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
    Page](http://www.program-transformation.org/edit/Sdf/SDF3?t=1536826617)
-   [Rename Page](http://www.program-transformation.org/rename/Sdf/SDF3)
-   [Attach File](http://www.program-transformation.org/attach/Sdf/SDF3)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sdf/SDF3?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sdf/SDF3?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev 2](http://www.program-transformation.org/view/Sdf/SDF3?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sdf/SDF3?rev1=1.2&rev2=1.1)
-   [Rev 1](http://www.program-transformation.org/view/Sdf/SDF3?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sdf/SDF3)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sdf/SDF3?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Sdf/SDF3?template=oopsmore&param1=1.2&param2=1.2)
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
SDF3 {#sdf3 .twikiTopicTitle}
====

::: {.twikiWebTitle}
Sdf
:::

(note: this is not an official release plan and probably quite out of
date. Please update if some info is incorrect!)

Below is a list of considerations for the next generation (version 3) of
the Syntax Definition Formalism SDF:

-   An improved mechanism to deal with multiple types of layout is
    desirable
    -   Idea: No longer specify layout using the sort LAYOUT but rather
        make layout a parameter of context-free syntax sections
        context-free syntax (C-Layout) foo bar -\> C context-free syntax
        (Sdf-Layout) hello world -\> Sdf

<!-- -->

-   In the current version of SDF the priority of alternatives is
    strange and differs from alternative syntax definition formalisms. A
    B \| C D is grouped as A (B\|C) D instead of (A B) \| (C D). Can SDF
    be redesigned to improve this?
    -   Idea: use explicit sequence operator: A . B \| C . D

<!-- -->

-   What are the top sorts of a grammar? Currently all declared sorts
    automatically become top sorts. This behavior allows sentences over
    a sub part of a language to be accepted by the parser. Parsing over
    a part of a language is required during development of a grammar and
    corresponding tooling. In general however, the number of top sorts
    needs to be restricted in order for the parser to only accept
    sentences that really belong to a language.
    -   Idea: Add \"top sorts\" section to SDF
    -   Idea: Adapt the parser generator to support multiple start
        states which are independent of the declared top sorts.

<!-- -->

-   What naming scheme to use to specify and locate Sdf modules?
    -   Idea: use Java\'s Internet-wide unique package naming scheme.
        imports nl.cwi.gb.sdf.\* nl.cwi.gb.aterms.\*

<!-- -->

-   What flattening methods of lexicals are required?
    -   Idea: flattening with structure preservation. This approach
        would for instance preserve the lexical structure of URL\'s
        (\[\"http:\",\"//\", \"www.cwi.nl\", \"/\"\]) \* Idea:
        flattening without structure preservation. For example:
        \"http://www.cwi.nl/\"

<!-- -->

-   To decrease the dependency of tools on the abstract syntax format of
    Sdf and to ease manipulation of Sdf parse trees, an
    [AsFix](../Tools/AsFix){.twikiLink} API is required. This API should
    provide efficient access functions to
    [AsFix](../Tools/AsFix){.twikiLink} terms and preferably should be
    generated from the Sdf syntax.

<!-- -->

-   Do we really need hidden and exported grammars?

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Sdf.SDF3 moved from Tools.SDF3 on 09 Feb 2004 - 13:51 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Sdf/SDF3?newweb=Tools&newtopic=SDF3&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
