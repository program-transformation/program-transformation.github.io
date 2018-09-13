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
    Page](http://www.program-transformation.org/edit/Stratego/SamplesNetXml?t=1536825666)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/SamplesNetXml)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/SamplesNetXml)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/SamplesNetXml?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/SamplesNetXml?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Stratego/SamplesNetXml?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/SamplesNetXml?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/SamplesNetXml?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/SamplesNetXml?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/SamplesNetXml?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/SamplesNetXml?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/SamplesNetXml)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/SamplesNetXml?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Stratego/SamplesNetXml?template=oopsmore&param1=1.6&param2=1.6)
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
Samples Net Xml {#samples-net-xml .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

\[under construction \--
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 23 Jul 2003\]

The [samples-net-xml](SamplesNetXml){.twikiLink} package is a bundle of
server-side and client-side example applications using the xml and
networking facilities of [xml-tools](../Tools/XmlTools){.twikiLink} and
[stratego-net](StrategoNetworking){.twikiLink}.

[]{#Contents} Contents
----------------------

-   cgi
    -   calculator
    -   hello-xhtml
    -   hello-form
    -   hello-upload
-   \...

[]{#Download_and_installation} Download and installation
--------------------------------------------------------

The source of [samples-net-xml](SamplesNetXml){.twikiLink} can be
checked out using:

      svn checkout https://svn.strategoxt.org/repos/StrategoXT/trunk/samples-net-xml

Configure the package:

-   `--with-xt` or if the packages are installed at different locations:
    -   `--with-aterm`
    -   `--with-sdf`
    -   `--with-strategoxt`
-   `--with-xml-tools`
-   `--with-stratego-net`
-   `--with-cgi-bin` if you want to samples to be installed in the
    cgi-bin of your HTTP server

[]{#See_also} See also
----------------------

-   [query-compiler](QueryCompiler){.twikiLink} \-- a set of tools for
    compilation of [SQL](SqlFront){.twikiLink} to [relational
    algebra](RelationalAlgebra){.twikiLink}. There is also a web
    interface to the tools, using
    [stratego-net](StrategoNetworking){.twikiLink},
    [xml-tools](../Tools/XmlTools){.twikiLink} and
    [MathML[^?^](http://www.program-transformation.org/edit/Stratego/MathML?topicparent=Stratego.SamplesNetXml)]{.twikiNewLink
    style="background : #FFFFCE;"} presentation in a browser (Mozilla
    for example).
-   [xdoc](ExtendibleDocumentationGenerator){.twikiLink} uses
    [xml-tools](../Tools/XmlTools){.twikiLink} for documentation
    generation in XHTML

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
