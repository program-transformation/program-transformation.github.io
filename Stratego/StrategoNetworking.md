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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoNetworking?t=1536825677)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoNetworking)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoNetworking)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoNetworking?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoNetworking?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    15](http://www.program-transformation.org/view/Stratego/StrategoNetworking?rev=1.15)
    [(diff 14)](http://www.program-transformation.org/rdiff/Stratego/StrategoNetworking?rev1=1.15&rev2=1.14)
-   [Rev
    14](http://www.program-transformation.org/view/Stratego/StrategoNetworking?rev=1.14)
    [(diff 13)](http://www.program-transformation.org/rdiff/Stratego/StrategoNetworking?rev1=1.14&rev2=1.13)
-   [Rev
    13](http://www.program-transformation.org/view/Stratego/StrategoNetworking?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/Stratego/StrategoNetworking?rev1=1.13&rev2=1.12)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoNetworking)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoNetworking?template=oopsmore&param1=1.15&param2=1.15)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoNetworking?template=oopsmore&param1=1.15&param2=1.15)
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
Stratego Networking {#stratego-networking .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Client-side](StrategoNetworking#Client_side)
-   [Server-side](StrategoNetworking#Server_side)
-   [Resources](StrategoNetworking#Resources)
-   [Download and
    installation](StrategoNetworking#Download_and_installation)
-   [See also](StrategoNetworking#See_also)
:::

[stratego-net](StrategoNetworking){.twikiLink} is a package you can use
to implement CGI based services or access a service at a certain URL
using HTTP.

Scenarios :

-   write an [ATermService](../Tools/ATermService){.twikiLink}
-   access an [ATermService](../Tools/ATermService){.twikiLink}
-   write an XML
    [WebService[^?^](http://www.program-transformation.org/edit/Stratego/WebService?topicparent=Stratego.StrategoNetworking)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   dynamicly generate XHTML

[]{#Client_side} Client-side
----------------------------

Use stratego-net on the client-side to:

-   download an
    [ATerm[^?^](http://www.program-transformation.org/edit/Stratego/ATerm?topicparent=Stratego.StrategoNetworking)]{.twikiNewLink
    style="background : #FFFFCE;"} from an URL
-   apply a transformation by invoking an
    [ATermService](../Tools/ATermService){.twikiLink}

Both strategies are implemented in the `http-client` module. Use
`http-get-term` to download an ATerm from the given URL. With
`xtc-http-get` you can download any file. This strategy should be used
in an [XTC](XTC){.twikiLink} composition.

      <http-get-term> URL("http://www.foo.com/foo.aterm")

With `xtc-http-transform` you can invoke an
[ATermService](../Tools/ATermService){.twikiLink} to do some
transformation. This strategy should be used with in an
[XTC](XTC){.twikiLink} composition. The `http-transform` operates on
terms an can be used outside an [XTC](XTC){.twikiLink} composition.

      xtc-io-wrap(
        xtc-http-transform(!URL("http://127.0.0.1/cgi-bin/calculator"))
      )

[]{#Server_side} Server-side
----------------------------

TODO

[]{#Resources} Resources
------------------------

-   The second part of the presentation [xml transformations and
    distributed
    services](http://www.students.cs.uu.nl/~mbravenb/docs/pt-xml.pdf) is
    devoted and introduction to services and shows some services and
    clients from the samples package in action.
-   XML-RPC [specification](http://www.xml-rpc.org/spec) and
    [homepage](http://www.xml-rpc.org/)

[]{#Download_and_installation} Download and installation
--------------------------------------------------------

The latest distribution is available at:

-   [Latest unstable
    release](http://releases.strategoxt.org/stratego-net-unstable-latest/)

For tarballs configure the package with the locations of the
dependencies:

-   `--with-aterm`
-   `--with-sdf`
-   `--with-strategoxt`
-   `--with-curl`

The daily distributions contain the latest of the latest developments,
but if you really want to, the latest sources can be checked out using:

      svn checkout https://svn.strategoxt.org/repos/StrategoXT/stratego-net/trunk

Before you can configure the package as described above you have to run
the `./bootstrap` script.

[]{#See_also} See also
----------------------

-   [samples-net-xml](SamplesNetXml){.twikiLink} \-- a samples package
    using [xml-front](../Tools/XmlFront){.twikiLink} and
    [stratego-net](StrategoNetworking){.twikiLink}.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
