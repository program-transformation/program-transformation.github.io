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
    Page](http://www.program-transformation.org/edit/SdfBackup/LexicalVersusContextFreeRestrictions?t=1536827746)
-   [Rename
    Page](http://www.program-transformation.org/rename/SdfBackup/LexicalVersusContextFreeRestrictions)
-   [Attach
    File](http://www.program-transformation.org/attach/SdfBackup/LexicalVersusContextFreeRestrictions)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/SdfBackup/LexicalVersusContextFreeRestrictions?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/SdfBackup/LexicalVersusContextFreeRestrictions?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/SdfBackup/LexicalVersusContextFreeRestrictions?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/SdfBackup/LexicalVersusContextFreeRestrictions?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/SdfBackup/LexicalVersusContextFreeRestrictions?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/SdfBackup/LexicalVersusContextFreeRestrictions?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/SdfBackup/LexicalVersusContextFreeRestrictions?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/SdfBackup/LexicalVersusContextFreeRestrictions)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/SdfBackup/LexicalVersusContextFreeRestrictions?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/SdfBackup/LexicalVersusContextFreeRestrictions?template=oopsmore&param1=1.3&param2=1.3)
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
Lexical Versus Context Free Restrictions {#lexical-versus-context-free-restrictions .twikiTopicTitle}
========================================

::: {.twikiWebTitle}
SDF: Modular Syntax Definition Formalism
:::

[LeonMoonen[^?^](http://www.program-transformation.org/edit/Main/LeonMoonen?topicparent=SdfBackup.LexicalVersusContextFreeRestrictions)]{.twikiNewLink
style="background : #FFFFCE;"} asked me what the difference is between
lexical and context-free
[FollowRestrictions[^?^](http://www.program-transformation.org/edit/SdfBackup/FollowRestrictions?topicparent=SdfBackup.LexicalVersusContextFreeRestrictions)]{.twikiNewLink
style="background : #FFFFCE;"} in SDF2. Here follows my response.
(Unfortunately it is in dutch.) \--
[EelcoVisser](../Main/EelcoVisser){.twikiLink} - 29 Mar 2001\

    > Ik ben een beetje in verwarring geraakt over lexicale versus context-vrije
    > restricties in SDF(2).
    > 
    > - is er wel verschil?
    > - zo ja, wanneer lexicaal en wanneer context-vrij gebruiken?

    Het verschil is:

      lexical restrictions 
         A -/- cc1
      context-free restrictions
         B -/- cc2

    wordt genormaliseerd naar

       restrictions
         <A-LEX> -/- cc1
         <B-CF> -/- cc2

    Zie pagina 207 proefschrift

    > "vroeger" dacht ik dat een lexicale restrictie (denk aan "longest match")
    > betekende dat er *geen* optionele layouit tussen soort en de
    > restricted chars mochten staan. Bij context-vrije zou dat dan wel mogen. 
    > Dat blijkt niet waar te zijn (experimenteel vastgesteld). 

    Nee, een restrictie S -/- cc (zie boven voor verschil tussen lex en cf)
    betekent dat characters uit cc die niet mogen voorkomen achter een boom van
    soort S. De implementatie van restricties (waarbij een enkele character set
    gegeven is) wordt gegeven op pagina 47 van proefschrift; regel (Fo4). Een
    restrictie heeft tot gevolg dat de follow set van soort S beperkt wordt. Dit
    sluit een reductie van een S boom uit in het geval er een karacter uit cc
    volgt.

    > Helaas ga je in jouw proefschrift niet in op context-vrije restricties 
    > (wel op lexicale) en uit de specs kan ik niet direct een verschil 
    > afleiden (behalve op welke soorten ze toegepast worden).

    Er staan inderdaad geen voorbeelden in van context-vrije restricties, maar de
    semantiek is dus hetzelfde als die van lexicale. (Pagina's 207 en 47)

    > De reden dat ik meer wil weten is dat ik bezig ben met island grammars 
    > en in sommige gevallen een ambiguiteit op kan lossen met een 
    > context-vrije restrictie op een verder lexicaal gedefinieerde soort 
    > ([a-z]+ -> Water). 

    Als je het voorbeeld wat uitgebreider beschrijft kan ik je misschien helpen.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Sdf.LexicalVersusContextFreeRestrictions moved from
Tools.LexicalVsContextFreeRestrictions on 09 Feb 2004 - 12:59 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}*
:::
:::
:::
:::
