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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoBox?t=1536825672)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoBox)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoBox)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoBox?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoBox?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/StrategoBox?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/StrategoBox?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/StrategoBox?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/StrategoBox?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/StrategoBox?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/StrategoBox?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoBox)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoBox?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoBox?template=oopsmore&param1=1.4&param2=1.4)
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
Stratego Box {#stratego-box .twikiTopicTitle}
============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[StrategoBox](StrategoBox){.twikiLink} is a syntax defintion for using
[ConcreteSyntax](ConcreteSyntax){.twikiLink} for the
[BoxLanguage](../Tools/BoxLanguage){.twikiLink} inside the
[StrategoLanguage](StrategoLanguage){.twikiLink}. With
[StrategoBox](StrategoBox){.twikiLink} you can write powerful
[PrettyPrinters](PrettyPrinter){.twikiLink} that target the
[BoxLanguage](../Tools/BoxLanguage){.twikiLink}. You can use this
approach when you need more control over pretty-printing than provided
by [PrettyPrintTables](../Tools/PrettyPrintTable){.twikiLink} .

To use the [StrategoBox](StrategoBox){.twikiLink} language you have to
declare in a `.meta` file that you want to use the
[StrategoBox](StrategoBox){.twikiLink} grammar:

      Meta([Syntax("Stratego-Box")])

In your `Makefile.am` you also have to include the directory
`$(GPP)/share/sdf/gpp` in `STRINCLUDES`.

This is an example pretty print rule in Stratego. It rewrites an empty
XML element to a Box.

      simple-element-to-box:
        EmptyElement(qname, []) -> box |[ H hs=0 [KW["<"] ~qname KW["/>"]] ]|

In general using [StrategoBox](StrategoBox){.twikiLink} is more verbose
than using [PrettyPrintTables](../Tools/PrettyPrintTable){.twikiLink}.
[StrategoBox](StrategoBox){.twikiLink} becomes interesting when you want
different pretty-printing, depending on the structure of a term. The
following rules rewrite an start tag in XML to Boxes. If there are no
attributes in the element we can pretty print the tag more attractive by
leaving out the space between the element name and the attributes.

      open-tag-to-box:
        (qname, []) -> box |[ H hs=0 [KW["<"] ~qname KW[">"]] ]|
          
      open-tag-to-box:
        (qname, atts) -> box |[ H hs=0 [KW["<"] H hs=1 [ ~qname ~*atts ] KW[">"]] ]|
           where <gt> (<length> atts, 0)

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
