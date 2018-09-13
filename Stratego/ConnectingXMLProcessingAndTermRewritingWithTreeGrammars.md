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
    Page](http://www.program-transformation.org/edit/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars?t=1536825426)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/ConnectingXMLProcessingAndTermRewritingWithTreeGrammars?template=oopsmore&param1=1.4&param2=1.4)
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
[Martin Bravenboer](http://martin.bravenboer.name). **Connecting XML
Processing and Term Rewriting with Tree Grammars** . Institute of
Information and Computing Sciences, Utrecht University, The Netherlands.
Master\'s thesis INF/SCR-04-08, November 20, 2003.
([ps](http://www.cs.uu.nl/people/martin/docs/master-thesis.ps),
[pdf](http://www.cs.uu.nl/people/martin/docs/master-thesis.pdf))

### []{#Abstract} Abstract

The widespread acceptance of xml for exchanging tree-like data between
software tools has resulted in a growing interest in tools for binding
xml to native data structures of a language and the design of dedicated
languages for processing xml.

In the Stratego/XT project the components of transformation system
operate on term representations of programs. These representations are
encoded in the aterm format, which has a more explicit structure than
xml. Most of these components are implemented in Stratego, a
transformation language that supports a separation of rewrite rules and
rewriting strategies.

We have developed a set of tools that unifies xml processing and term
rewriting. The different needs of xml processing application are served
by providing several levels of term representations of xml. The tool kit
consists of syntax, document and data-oriented representations of xml
and the tools for manipulating them. In modular and reusable tools we
apply the basic principles of tree and hedge grammars to obtain a
natural, more explicitly structured representation of an xml document in
a term.

Our tools enable interoperability of xml and aterm tools. All term
representations of xml can be transformed using Stratego. This enables
the implementation of complex xml transformations using the strategic
rewriting paradigm and the generic traversals of Stratego.

[]{#Links} Links
----------------

-   [Stratego/XT](http://www.stratego-language.org/)
-   [stratego-regular](StrategoRegular){.twikiLink}
-   [xml-front](../Tools/XmlFront){.twikiLink}
-   [xml-tools](../Tools/XmlTools){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
