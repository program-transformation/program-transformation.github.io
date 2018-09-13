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
    Page](http://www.program-transformation.org/edit/SdfBackup/DisambiguationInSDF2?t=1536827746)
-   [Rename
    Page](http://www.program-transformation.org/rename/SdfBackup/DisambiguationInSDF2)
-   [Attach
    File](http://www.program-transformation.org/attach/SdfBackup/DisambiguationInSDF2)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/SdfBackup/DisambiguationInSDF2?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/SdfBackup/DisambiguationInSDF2?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/SdfBackup/DisambiguationInSDF2?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/SdfBackup/DisambiguationInSDF2?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/SdfBackup/DisambiguationInSDF2?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/SdfBackup/DisambiguationInSDF2?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/SdfBackup/DisambiguationInSDF2?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/SdfBackup/DisambiguationInSDF2)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/SdfBackup/DisambiguationInSDF2?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/SdfBackup/DisambiguationInSDF2?template=oopsmore&param1=1.3&param2=1.3)
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
Disambiguation In SDF2 {#disambiguation-in-sdf2 .twikiTopicTitle}
======================

::: {.twikiWebTitle}
SDF: Modular Syntax Definition Formalism
:::

There are a number of features for disambiguation in SDF2.

**Associativity**

Associativity declarations are used to solve ambiguities of an operator
with respect to itself. For example, the production

Exp \"+\" Exp -\> Exp {left}

is annotated with the attribute \'left\' which entails that addition is
left associative with respect to itself, i.e., a + b + c should be read
as (a + b) + c.

**Priorities**

Priorities can be used to solve ambiguities between operators. For
example, the priority declaration

Exp \"\*\" Exp -\> Exp \> Exp \"+\" Exp -\> Exp

declares multiplication to have higher priority than addition.

**Reject Productions**

Reject productions are used to exclude some phrases from a sort. The
standard application is the exclusion of keywords from lexical sorts.
For example, the reject production

\"if\" -\> Id {reject}

excludes \'if\' as an identifier.

**Restrictions**

Follow restrictions are used to declare that some sort cannot be
followed by some characters. For instance, the restriction

Id -/- \[a-z\]

declares that phrases of the sort Id cannot be followed by lower case
letters.

**Other Disambiguation Methods**

-   avoid
-   prefer

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Sdf.DisambiguationInSDF2 moved from Tools.DisambiguationInSDF2 on 09
Feb 2004 - 13:47 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}*
:::
:::
:::
:::
