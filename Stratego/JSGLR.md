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
    Page](http://www.program-transformation.org/edit/Stratego/JSGLR?t=1536825367)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/JSGLR)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/JSGLR)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/JSGLR?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/JSGLR?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Stratego/JSGLR?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/JSGLR?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/JSGLR?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/JSGLR?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/JSGLR?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/JSGLR?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/JSGLR)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/JSGLR?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Stratego/JSGLR?template=oopsmore&param1=1.5&param2=1.5)
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
JSGLR {#jsglr .twikiTopicTitle}
=====

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#JSGLR_An_SGLR_Parse_Table_Evalua} [JSGLR](JSGLR){.twikiLink}: An [SGLR](SGLR){.twikiLink} Parse Table Evaluator for Java
============================================================================================================================

The jsglr library implements scannerless [GLR](GLR){.twikiLink}
([SGLR](SGLR){.twikiLink}) parsing in Java. The library provides an
interpreter for parse tables generated from grammars written using
[SDF](SDF){.twikiLink}. The jsglr library can load parse tables for the
`sglr` version 3.16 from textual ATerms, TAF or BAFs (compressed, binary
ATerms).

Note that the parse tables cannot be generated from
[SDF](SDF){.twikiLink} grammars by the jsglr package. You will have to
install the [SDF](SDF){.twikiLink} package for this.

For more details, see <http://www.spoofax.org/jsglr.html>

### []{#Usage} Usage

Initializing and using `jsglr` from your application is easy:

    String inputFile = ...
    ParseTableManager ptm = new ParseTableManager();
    SGLR sglr = new SGLR(ptm.getFactory(), ptm.loadFromFile(parseTable));
    ATerm t = sglr.parse(new FileInputStream(inputFile));

First, the `ParseTableManager` is instantiated. This is a registry of
all loaded parse tables. Loading large parse tables takes a bit of time,
so pre-loading all the parse tables you need into the registry will save
you time if you need to parse repeatedly.

Second, the an `SGLR` instance is created, and \"inherits\" the ATerm
factory from the `ParseTableFactory`. Here, we use the
`ParseTableManager` to cache the `ParseTable` while it is loaded.

Third, parsing is just a matter of calling the `parse()` method on an
object of class `SGLR`. The result is an ATerm, or `null`, if the parse
failed.

### []{#SDF_Manual} [SDF](SDF){.twikiLink} Manual

A copy of the CWI manual for the Syntax Definition Formalism is
available at <http://www.spoofax.org/sdf/sdf-manual-2007-10-22.pdf>

### []{#Error_Recovery_in_JSGLR} Error Recovery in [JSGLR](JSGLR){.twikiLink}

[JSGLR](JSGLR){.twikiLink} provides supports for parse error recovery,
which is essential for applying the parser in an interactive
environment. The [Permissive Grammars](PermissiveGrammars){.twikiLink}
project provides further information on this topic.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
