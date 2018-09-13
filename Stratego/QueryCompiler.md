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
    Page](http://www.program-transformation.org/edit/Stratego/QueryCompiler?t=1536825660)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/QueryCompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/QueryCompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/QueryCompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/QueryCompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/QueryCompiler?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/QueryCompiler?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/QueryCompiler?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/QueryCompiler?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/QueryCompiler?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/QueryCompiler?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/QueryCompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/QueryCompiler?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/QueryCompiler?template=oopsmore&param1=1.4&param2=1.4)
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
Query Compiler {#query-compiler .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#Introduction} Introduction
------------------------------

The [query-compiler](QueryCompiler){.twikiLink} package is a set of
tools for the inspection of the process of query compilation. It shows
how a SQL query is parsed, desugared, translated in relational algebra
and optimized. The user interface is web-based, implemented using
[stratego-net](StrategoNetworking){.twikiLink} and
[xml-tools](../Tools/XmlTools){.twikiLink}. Of course the components of
the query-compiler are also available as command-line utils.

The [query-compiler](QueryCompiler){.twikiLink} is based on the
[sql-front](SqlFront){.twikiLink} and
[relational-algebra](RelationalAlgebra){.twikiLink} packages.
[sql-front](SqlFront){.twikiLink} is used to parse a SQL query to an
abstract syntax for SQL. The relatonal-algebra packages implements the
optimization of relational algebra and the renderering of relational
algebra expressions in
[MathML[^?^](http://www.program-transformation.org/edit/Stratego/MathML?topicparent=Stratego.QueryCompiler)]{.twikiNewLink
style="background : #FFFFCE;"}.

[]{#Download_and_installation} Download and installation
--------------------------------------------------------

       svn checkout https://svn.strategoxt.org/repos/StrategoXT/trunk/experimental/query-compiler

The packages requires (configuration with):

-   [stratego-net](StrategoNetworking){.twikiLink}
-   [sql-front](SqlFront){.twikiLink}
-   [relational-algebra](RelationalAlgebra){.twikiLink}

Configure the package `--with-cgi-bin` if you want to install the
web-based user interface directly into your cgi-bin.

[]{#Online_Demo} Online Demo
----------------------------

The query compiler is available online. The testsuite lists some example
queries that can be compiled:

-   <http://stratego.insanity.nl/cgi/query-compiler/query-testsuite>

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
