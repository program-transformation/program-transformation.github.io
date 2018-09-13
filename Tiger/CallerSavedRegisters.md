::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![Stratego
logo](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)

------------------------------------------------------------------------

***Tiger in Stratego***

------------------------------------------------------------------------

**[WebHome](WebHome){.twikiLink}**\
[Tiger Compiler](TigerCompiler){.twikiLink}\
[Architecture](CompilerArchitecture){.twikiLink}\
[Packages](CompilerPackages){.twikiLink}\
[Components](CompilerComponent){.twikiLink}\
[Glossary](WebGlossary){.twikiLink}

[Download](DownloadAndInstallation){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Tiger/CallerSavedRegisters?t=1536826658)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tiger/CallerSavedRegisters)
-   [Attach
    File](http://www.program-transformation.org/attach/Tiger/CallerSavedRegisters)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tiger/CallerSavedRegisters?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tiger/CallerSavedRegisters?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Tiger/CallerSavedRegisters?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Tiger/CallerSavedRegisters?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Tiger/CallerSavedRegisters?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tiger/CallerSavedRegisters)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tiger/CallerSavedRegisters?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Tiger/CallerSavedRegisters?template=oopsmore&param1=1.2&param2=1.2)
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
Caller Saved Registers {#caller-saved-registers .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Tiger in Stratego \-- Compilation by Program Transformation
:::

(in dutch)

\> Instructieselectie werkt nu aardig maar wat mij nog onduidelijk is,
is hoe\
\> je bij het aanroepen van een andere functie code genereert om de\
\> callee-saved registers te bewaren: je weet immers nog niet welke dat
zijn,\
\> want de RA komt pas na IS.\

Precies. En daarom wil je dat overlaten aan RA. De overlay definitie
voor de jal instructie is als volgt gedefinieerd:

      jal(lab, ra, use) =
        OPER(["    jal    ", L(1)], use, CallerSavedRegisters, [lab, ra]) 

Dit betekent dat de
[CallerSavedRegisters](CallerSavedRegisters){.twikiLink} (zie
[MIPS](http://www.program-transformation.org/Tiger/MIPS){.twikiLink}-registers.r)
overschreven kunnen worden. Dit is genoeg om aan RA te melden dat de
callersavedregisters niet gebruikt kunnen worden waarden te bewaren die
moet leven na de procedure aanroep. \`use\' is een lijst met registers
die \`gebruikt\' wordt door de jal instructie. Dit is noidg om te zorgen
dat de waarden in de parameter registers blijven leven tot de instructie
wordt uitgevoerd. lab is het label van de aangeroepen functie. ra is het
label van het return adres. Dit moet je genereren na het aanroepen van
jal

       SEQ(jal("f", "a_0", [TEMP("a_1")]), label("a_0"))

om te zorgen dat de control flow duidelijk is voor RA.

Als je deze informatie verstrekt zal RA zorgen dat de registers zo
gekozen worden dat ze niet in een callersaved register zitten als ze een
functie aanroep moet overleven. Als dat het niet aanders kan zal RA een
register spillen en ruimte op de stack alloceren.

De callee-saved registers moet je aan het begin van een functie aanroep
moven naar een temp en aan het einde weer terug. Als het register niet
nodig is wordt de move gecoalesced anders worden er spill instructies
gegenereerd.

Hoop dat het zo duidelijk is. Appel vertelt dit ook in de sectie over
CALLER-SAVE AND CALLEE-SAVE REGISTERS in hoofdstuk 11 sectie 3.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 10 Jan 2002\
\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Hpc.CallerSavedRegisters moved from Hpc.CalleeSavedRegisters on 10 Jan
2002 - 21:26 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}*
:::
:::
:::
:::
