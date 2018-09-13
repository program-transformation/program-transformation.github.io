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
    Page](http://www.program-transformation.org/edit/Sdf/SDF2o2?t=1536826616)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sdf/SDF2o2)
-   [Attach
    File](http://www.program-transformation.org/attach/Sdf/SDF2o2)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sdf/SDF2o2?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sdf/SDF2o2?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Sdf/SDF2o2?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sdf/SDF2o2?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Sdf/SDF2o2?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sdf/SDF2o2)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sdf/SDF2o2?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Sdf/SDF2o2?template=oopsmore&param1=1.2&param2=1.2)
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
SDF2 o 2 {#sdf2-o-2 .twikiTopicTitle}
========

::: {.twikiWebTitle}
Sdf
:::

**Proposed Changes**

A summary of changes from SDf.2.1 to SDF.2.2 :

-   The syntax of Tools.ATerms will be used for SDF attributes for
    example: A -\> B {left} B -\> C {aap(noot,mies)}

<!-- -->

-   SDF layout is defined in a separate module and imported at the top.
    This allows other modules to be reused without inheriting the SDF
    layout and comment conventions.

<!-- -->

-   Tools.ATerm and SDF unquoted literals are distinguished using the
    sort
    [UQSdfLiteral[^?^](http://www.program-transformation.org/edit/Sdf/UQSdfLiteral?topicparent=Sdf.SDF2o2)]{.twikiNewLink
    style="background : #FFFFCE;"}.

<!-- -->

-   The \"definition\" keyword is removed. An SDF definition is just a
    sequence of SDF modules: Module\* -\> Definition

<!-- -->

-   The following file extensions will be used for SDF modules and
    definitions:
    -   .sdf for SDF modules
    -   .def for SDF definitions

<!-- -->

-   The SDF grammar will contain constructor annotations which define
    the abstract syntax of SDF

<!-- -->

-   Three new constructors are introduced in
    [AsFix](../Tools/AsFix){.twikiLink}:
    -   qlit to represent quoted literals
    -   uqlit to represent unquoted literals
    -   flatlex to represent flattened lexicals

<!-- -->

-   The production sorts Symbols -\> Grammar has been replaced bu sorts
    Sorts -\> Grammar

**Unresolved Issues**

-   Do we need directly visible kernel syntax?

<!-- -->

-   Are there convincing examples of kernel syntax?
-   Why can these not be handled by lexical syntax?

<!-- -->

-   How do the sorts in kernel syntax and other sections relate?

<!-- -->

-   Do we need aliases?

<!-- -->

-   Why Symbols in parameter list following module name?

<!-- -->

-   Keyword \"Set\" should be \"set\"

<!-- -->

-   Do we need the \"(\" Symbol \"=\>\" Symbol \")\" syntax?

<!-- -->

-   Why are the lookaheads \"[\" {Lookahead \",\"}\*
    \"[^?^](http://www.program-transformation.org/edit/Sdf/Lookahead?topicparent=Sdf.SDF2o2)]{.twikiNewLink
    style="background : #FFFFCE;"}\" visible? Should belong to kernel
    syntax.

<!-- -->

-   How to add
    [GrammarAnnotations[^?^](http://www.program-transformation.org/edit/Tools/GrammarAnnotations?topicparent=Sdf.SDF2o2)]{.twikiNewLink
    style="background : #FFFFCE;"}?

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Sdf.SDF2o2 moved from Tools.SDF2o2 on 09 Feb 2004 - 14:40 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Sdf/SDF2o2?newweb=Tools&newtopic=SDF2o2&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
