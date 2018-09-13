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
    Page](http://www.program-transformation.org/edit/Stratego/Aster?t=1536825549)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/Aster)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/Aster)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/Aster?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/Aster?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    13](http://www.program-transformation.org/view/Stratego/Aster?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/Stratego/Aster?rev1=1.13&rev2=1.12)
-   [Rev
    12](http://www.program-transformation.org/view/Stratego/Aster?rev=1.12)
    [(diff 11)](http://www.program-transformation.org/rdiff/Stratego/Aster?rev1=1.12&rev2=1.11)
-   [Rev
    11](http://www.program-transformation.org/view/Stratego/Aster?rev=1.11)
    [(diff 10)](http://www.program-transformation.org/rdiff/Stratego/Aster?rev1=1.11&rev2=1.10)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/Aster)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/Aster?template=oopsmore&param1=1.13&param2=1.13)
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
    \...](http://www.program-transformation.org/oops/Stratego/Aster?template=oopsmore&param1=1.13&param2=1.13)
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
Aster {#aster .twikiTopicTitle}
=====

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Aster is an [attribute
grammar](../Transform/AttributeGrammar){.twikiLink} system based on
[Stratego](StrategoLanguage){.twikiLink}. It makes use of the standard
Stratego facilities such as [pattern
matching](PatternMatching){.twikiLink} and [concrete
syntax](ConcreteSyntax){.twikiLink} to specify attribute equations and
associate them with nodes of an abstract syntax tree. To abstract from
these basic equations, users can specify *attribute decorators* that
provide an abstract evaluation mechanism for attributes. Inspired by
Stratego\'s [rewriting strategies](StrategoLanguage){.twikiLink}, these
can be used to provide separation of concerns between the basic
equations and high-level global search or traversal patterns to be taken
on the tree for their evaluation. For example, these can be used to
specify *automatic copy rules*, such as a downward copy rule that copies
an attribute value from the parent node if it is not defined at the
current node, and recursively higher up in the tree.

Attribute decorators can be used to describe different various
high-level attribution patterns, and are not limited to basic copy rule
specifications. For example, these include providing support for
collection attributes, declaration lookup attributes, and attributes
that require fix-point evaluation of circular dependencies (e.g., for
data-flow equations). These patterns are often implemented as extensions
of the basic attribute grammar paradigm in other systems, \"baked into\"
different attribute evaluator systems. Rather than supporting these in
the attribute evaluation system itself, Aster allows to provide these as
a library of decorators, and lets users specify their own, often
domain-specific decorators by hand.

[]{#Project_Information} Project Information
--------------------------------------------

Aster has been developed by [Lennart
Kats](../Main/LennartKats){.twikiLink}.

### []{#Contact_and_Mailing_List} Contact and Mailing List

Please send questions to the [users\@strategoxt.org mailing
list](https://mailman.st.ewi.tudelft.nl/listinfo/users) or [contact
Lennart Kats](http://www.lclnet.nl/contact) directly. Also, the
developers are usually available on IRC at [\#stratego on
freenode.net](irc://irc.freenode.net/stratego) ([web
version](http://java.freenode.net/index.php?channel=stratego)). Feel
free to drop by!

### []{#License} License

Aster is [LGPL](LGPL){.twikiLink} (GNU Lesser General Public License)
software. This means that you can use it without being required to
distribute your software under the GPL.

[]{#Downloads} Downloads
------------------------

### []{#Source_Repository} Source Repository

The full source code is available from Subversion:

-   <https://svn.strategoxt.org/repos/StrategoXT/aster/trunk/>

### []{#Daily_builds} Daily builds

Distributions are built continuously:

-   <http://releases.strategoxt.org/aster/aster-unstable/>

[]{#Publications} Publications
------------------------------

Lennart C. L. Kats, Anthony M. Sloane, Eelco Visser. *Decorated
Attribute Grammars. Attribute Evaluation Meets Strategic Programming*.
In Proceedings of the 18th International Conference on Compiler
Construction ([CC 2009](http://www.brics.dk/%7Emis/CC2009/)), Volume
5501 of Lecture Notes in Computer Science, pages 142---157. York, United
Kingdom, Springer-Verlag, March 2009.
\[[abstract](http://www.lclnet.nl/publications/decorated-attribute-grammars)\] \[[pdf](http://www.lclnet.nl/publications/decorated-attribute-grammars.pdf)\] \[[bib](http://www.lclnet.nl/publications/decorated-attribute-grammars.bib)\]

### []{#Presentation} Presentation

[Decorated Attribute
Grammars](http://www.lclnet.nl/publications/decorated-attribute-grammars-presentation.pdf)
(CC 2009)

[]{#Related_Software} Related Software
--------------------------------------

The [Transformers
project](http://www.lrde.epita.fr/cgi-bin/twiki/view/Transformers/)
incorporates a Stratego-based attribute grammar system into
[SDF](SDF){.twikiLink} for disambiguation of context-free grammars.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
