::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
  ----------------------------------------------------------------------------------
  [![](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)](WebHome)
  ----------------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

-   [Documentation](StrategoDocumentation){.twikiLink}
-   [Language](StrategoLanguage){.twikiLink}
-   [Research Papers](StrategoPublications){.twikiLink}
-   [Applications](StrategoApplication){.twikiLink}

**[Download](StrategoDownload){.twikiLink}**

-   [Continuous build](ContinuousBuild){.twikiLink}
-   [Extensions](AdditionalPackageDownload){.twikiLink}

**[Support](StrategoSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Users Days](StrategoUsersDay){.twikiLink}
-   [Bug Reports](http://yellowgrass.org/project/StrategoXT)

**[Developers](StrategoDev){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/StrategoXT/strategoxt/trunk)
-   [Buildfarm
    results](http://hydra.nixos.org/jobset/strategoxt/strategoxt-release/all)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Stratego/StrategoSyntax?t=1536825683)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoSyntax)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoSyntax)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoSyntax?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoSyntax?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    11](http://www.program-transformation.org/view/Stratego/StrategoSyntax?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/Stratego/StrategoSyntax?rev1=1.11&rev2=1.10)
-   [Rev
    10](http://www.program-transformation.org/view/Stratego/StrategoSyntax?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Stratego/StrategoSyntax?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Stratego/StrategoSyntax?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Stratego/StrategoSyntax?rev1=1.9&rev2=1.8)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoSyntax)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoSyntax?template=oopsmore&param1=1.11&param2=1.11)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoSyntax?template=oopsmore&param1=1.11&param2=1.11)
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
Stratego Syntax {#stratego-syntax .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The syntax of [StrategoLanguage](StrategoLanguage){.twikiLink} used to
be defined by a LEX/Transform.YetAnotherCompilerCompiler grammar. In
order to make maintenance and extension of the syntax definition easier
it is desirable to migrate the definition to
[SDF2](../Sdf/WebHome){.twikiLink}.

See
[FromStrategoInYaccToStrategoInSDF](../Tools/FromStrategoInYaccToStrategoInSDF){.twikiLink}
for a description of the derivation process.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 27 Oct 2001\

------------------------------------------------------------------------

XT release 0.9 contains the syntax definition corresponding to
[StrategoRelease062](StrategoRelease062){.twikiLink}. This does not yet
incorporate the extension with [TermWrap](TermWrap){.twikiLink} and
[TermProject](TermProject){.twikiLink} syntax.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 09 Dec 2001

------------------------------------------------------------------------

There is a nameclash in Stratego.def/r/pp: the strategy some(s) and the
constructor for Option(a), Some(a), have the same constructor: \'Some\'.
This causes another pretty printing problem.

\-- Hedzer Westra

------------------------------------------------------------------------

Ik probeer de stratego grammatica uit GB te gebruiken maar stuit op een
probleem:

sglr: error in /opt/xt-0.9/share/ssl/list-set.r, line 133, col 17:
character \`\|\' unexpected.

het betreft hier de paal (\|) constructie in onderstaande strategie:

      collect-all(s) =
        rec x(![<s> | <crush(![],union,x)>]
              <+ crush(![],union,x))

De grammatica zegt:

    "[" {Strategy ","}* "|" Strategy "]" -> Strategy {cons("ListCong")}

    "<" Strategy ">" Term -> Strategy {cons("BA")}
    "<" Strategy ">" -> StrategyAngle {cons("AngleStrat")}
    "<" Strategy ">" Term -> Term {cons("App")}

Kortom, `<s>` is een `StrategyAngle` maar `StrategyAngle` komt verder
nergens in de grammatica voor.

Hoe zullen we dit oplossen?

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 21 Dec 2001

------------------------------------------------------------------------

Dit is een uitbreiding van de syntax die in 0.6.3 is ingevoerd (zie
[TermProject](TermProject){.twikiLink} en
[TermWrap](TermWrap){.twikiLink} op de wiki). De syntax in gb gaat over
0.6.2 en moet dus uitgebreid worden tot 0.6.3. Ik zal proberen een dezer
dagen die uitbreiding te maken en aan jou opsturen (ik kan niet bij de
CVS).

Als je tools aan het testen bent kan je ook nog even de oude (0.6.2)
versie van de bibliotheek gebruiken.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 21 Dec 2001

------------------------------------------------------------------------

Aha, ik begrijp het.

Nog een probleem: parseren van module list-set.r van stratego-0.6.1
levert ambiguiteit op in inderstaande strategy:

      CollectSplit(s, splitter) :
        c#(as) -> (t, <union> (ys, <unions> xs))
        where <list(s); unzip> as => (bs, xs);
              <splitter> c#(bs) => (t, ys)

    amb([
    ExplodeCong(BA(CallNoArgs(SVar("splitter")),Inj(Var("c"))),ParenStrat(CallNoArgs(SVar("bs")))),
    BA(CallNoArgs(SVar("splitter")),Explode(Inj(Var("c")),Inj(Var("bs"))))
    ])

Nog een probleem: De pgen/sglr combinatie die wij in XT bundelen bevat
een bug: voor alternatieven wordt de constructor \"pair\" (i.p.v.
\"alt\") gebruikt. Omdat jij in he stratego syntax gebruik maakt van
alternativen, is de bijberende parseboom en AST incorrect.

Groet,

\-- [MerijnDeJonge](../Main/MerijnDeJonge){.twikiLink} - 21 Dec 2001

These problems have been solved in the stratego-0.7 version in the
[GrammarBase](../Sdf/GrammarBase){.twikiLink}. In addition other new
constructs such as
[GlobalChoice[^?^](http://www.program-transformation.org/edit/Stratego/GlobalChoice?topicparent=Stratego.StrategoSyntax)]{.twikiNewLink
style="background : #FFFFCE;"} and
[GuardedLeftChoice](GuardedLeftChoice){.twikiLink} have been added. The
desugaring has been adapted to
[FixedLengthTuples](FixedLengthTuple){.twikiLink}.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 03 Feb 2002

------------------------------------------------------------------------

[CategoryDone[^?^](http://www.program-transformation.org/edit/Stratego/CategoryDone?topicparent=Stratego.StrategoSyntax)]{.twikiNewLink
style="background : #FFFFCE;"} \| [ToDo](ToDo){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.StrategoSyntax moved from Stratego.SyntaxOfStratego on 08 Dec
2001 - 16:13 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}* - [put
it
back](http://www.program-transformation.org/rename/Stratego/StrategoSyntax?newweb=Stratego&newtopic=SyntaxOfStratego&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
