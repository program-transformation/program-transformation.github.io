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
    Page](http://www.program-transformation.org/edit/Stratego/XTC?t=1536825368)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/XTC)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/XTC)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/XTC?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/XTC?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Stratego/XTC?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/XTC?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/XTC?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/XTC?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/XTC?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/XTC?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/XTC)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/XTC?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Stratego/XTC?template=oopsmore&param1=1.5&param2=1.5)
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
XTC {#xtc .twikiTopicTitle}
===

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[XTC](XTC){.twikiLink} \-- [Transformation Tool
Composition](TransformationToolComposition){.twikiLink}

[XTC](XTC){.twikiLink} implements the XT component model and provides
support for creating compositions of XT components. The xtc tool is used
to register components in an [XTC](XTC){.twikiLink} repository. For
example the command:

    > xtc -r /usr/share/StrategoXT/XTC register -t sglr -l /bin -V 3.8

registers version 3.8 of sglr which is installed in /bin in the
[XTC](XTC){.twikiLink} repository located in /usr/share/StrategoXT. The
generic Makefile.xt provided by [AutoXT](AutoXT){.twikiLink}
automatically registers all installed tools with the package repository.

[XTC](XTC){.twikiLink} repositories can be used to find the installation
location of a tool without needing to know all the installation paths.
For example, the following query can be used to find out where sglr is
installed:

    > xtc -r /usr/share/StrategoXT/XTC query -t sglr 
    sglr (3.8) : /bin/sglr

An existing repository can be inherited by importing it

    > xtc -r /home/user/share/tiger/XTC import /usr/share/StrategoXT/XTC

In addition to the command-line tool for registration and querying of
repositories, [XTC](XTC){.twikiLink} also provides a Stratego API for
approaching [XTC](XTC){.twikiLink} repositories. All that is required to
use this API is importing the xtc-lib module. To use
[XTC](XTC){.twikiLink} add the following to your Makefile.am:

    bin_PROGRAMS  = term-to-dot
    SCFLAGS       = --main $*
    STRINCLUDES  = -I $(XTC)/share/xtc

The [XTC](XTC){.twikiLink} API supports easy calling of external
Stratego components and mixing them with internally defined
transformations. Here is an example:

    module term-to-dot
    imports xtc-lib lib term-to-adot

    strategies

      term-to-dot =
        xtc-io-wrap(term-to-adot-options,
          xtc-io-transform(to-adot)
        ; xtc-transform(!"ast2abox", !["-p", <xtc-find> "Dot-pretty.pp"])
        ; xtc-transform(!"abox2text")
        )

Note that no code is needed to load the repository. Whenever a query is
done (e.g., by xtc-transform to find \"ast2abox\"), and no repository is
loaded the [XTC](XTC){.twikiLink} repository is loaded.

[AutoXT](AutoXT){.twikiLink} provides support for [XTC](XTC){.twikiLink}
by means of a package switch \--with-repository that can be used to
indicate the repository in which to register tools. The default is
\$prefix/share/\$PACKAGE/XTC, i.e., the [XTC](XTC){.twikiLink} file in
the package data directory. In the [StrategoXT](StrategoXT){.twikiLink}
distribution the sub-packages inherit the repository location from the
super-package, i.e., all [StrategoXT](StrategoXT){.twikiLink} tools are
registered in \$prefix/share/StrategoXT/XTC.

Makefile.xt implements an automake install hook to install all programs,
scripts, and data. Thus it is not necessary to include make rules for
this purpose. The Makefile example above is sufficient to register tools
and data.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 13 Dec 2002\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
