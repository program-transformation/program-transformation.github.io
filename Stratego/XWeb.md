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
    Page](http://www.program-transformation.org/edit/Stratego/XWeb?t=1536825496)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/XWeb)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/XWeb)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/XWeb?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/XWeb?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    9](http://www.program-transformation.org/view/Stratego/XWeb?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Stratego/XWeb?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Stratego/XWeb?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/XWeb?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Stratego/XWeb?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/XWeb?rev1=1.7&rev2=1.6)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/XWeb)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/XWeb?template=oopsmore&param1=1.9&param2=1.9)
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
    \...](http://www.program-transformation.org/oops/Stratego/XWeb?template=oopsmore&param1=1.9&param2=1.9)
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
XWeb {#xweb .twikiTopicTitle}
====

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Introduction](XWeb#Introduction)
-   [Resources](XWeb#Resources)
-   [Download and installation](XWeb#Download_and_installation)
    -   [Configuration](XWeb#Configuration)
    -   [Extending xweb with new
        demos](XWeb#Extending_xweb_with_new_demos)
        -   [Creating a template](XWeb#Creating_a_template)
-   [Known Bugs (or features)](XWeb#Known_Bugs_or_features)
-   [TODO](XWeb#TODO)
:::

[]{#Introduction} Introduction
------------------------------

XWeb is a generic template-based transformation demonstration service;
it\'s implemented as a CGI application. The current version contains a
demo for [tiger](../Tiger/WebHome){.twikiLink} (simple and advanced
version) and [exp-tools](ExpTools){.twikiLink}, but other demos can be
added without to much effort.

The most recent version runs at
<http://stratego.insanity.nl/cgi/xweb/demo> This location will change to
catamaran.labs.cs.uu.nl when it has a better
[StrategoXT](StrategoXT){.twikiLink} environment (catamaran is the
actual Stratego server).

[]{#Resources} Resources
------------------------

-   [xml-tools](../Tools/XmlTools){.twikiLink} : XML tool package, used
    for XML parsing and generation
-   [stratego-net](StrategoNetworking){.twikiLink} : Package for
    implementing CGI based services
-   [exp-tools](ExpTools){.twikiLink} : Expression tool package, an
    incarnation of [XtApplet](XtApplet){.twikiLink}.
-   [tiger](../Tiger/WebHome){.twikiLink} : Tiger in Stratego, currently
    a demo for this package been implemented
-   [tiger-contract](TigerContract){.twikiLink} : Experimental tiger
    compiler package with contract support

[]{#Download_and_installation} Download and installation
--------------------------------------------------------

The source of XWeb can be checked out using:

      svn checkout https://svn.strategoxt.org/repos/StrategoXT/trunk/experimental/xweb

There\'s no distribution of XWeb available.

### []{#Configuration} Configuration

Configure the package:

-   `--with-xt` or if the packages are installed at different locations:
    -   `--with-aterm`
    -   `--with-sdf`
    -   `--with-strategoxt`
-   `--with-xml-tools`
-   `--with-stratego-net`
-   `--with-exp-tools`
-   `--with-tiger`
-   `--with-tiger-contract`
-   `--with-cgi-bin` if you want XWeb to be installed in the cgi-bin of
    your HTTP server

Flags `--with-exp-tools`, `--with-exp-tools` and `--with-tiger-contract`
are in some way optional. For example, if you don\'t want to deploy the
[exp-tools](ExpTools){.twikiLink} demo, then don\'t use its configure
flag and remove the associated XHTML template from your webserver.

### []{#Extending_xweb_with_new_demos} Extending xweb with new demos

The two bigger steps to undertake when extending XWeb with new demos
are:

-   Add a `--with-[package]` construct in the configure.ac and make sure
    the [XTC](XTC){.twikiLink} repository of the package is imported in
    the XWeb repository; see Makefile.am in the topdir of the package
-   Create a xhtml template in data/templates/demo directory and create
    a list of allowed components in the data/config directory. Example
    sources can be stored in data/sources/\[language\], see available
    sources\' Makefile.am\'s for how it\'s done.

#### []{#Creating_a_template} Creating a template

See data/templates/demo/tiger-simple.xhtml for a small example; all tags
in the xhtml namespace are rendered by your browser, tags in the xweb
namespace are transformed by the xweb cgi application. The application
is configured using a set of properties:

-   srcdir: Directory containing programs subject to program
    transformation with the demo web (make sure that your HTTP server
    can read/write in this directory, usually this is www-data or
    nobody)
-   components: File containing list of allowed components that can used
    in compositions on the demo web (it\'s in fact an ATerm containing a
    list of Strings). In tools/ there\'s a little program called
    dir2list that scans the current directory for files without an
    extension (usually binaries) and creates a component list that can
    be used for this purpose.
-   extension: The extension of program sources. For tiger, this is .tig
-   check: Component called to check whether saving a source is allowed;
    usually this is a parser (like parse-tiger). XWeb checks whether the
    transformation of the source with this component yields an ATerm.

A number of tags in the xweb namespace are transformed by the XWeb CGI
application (source can be found in src/demo.strxml); see
data/templates/demo directory in the package for some nice examples.

[]{#Known_Bugs_or_features}[]{#Known_Bugs_or_features_} Known Bugs (or features)
--------------------------------------------------------------------------------

-   When source is an ATerm and has been pretty-printed by pp-aterm, it
    might or will not be able to transform it. Regular ATerm\'s work
    fine as source.
-   Adding available components from their selectbox isn\'t very
    intuitive.
-   When saving a source; XWeb assumes that sources are programs and
    checks them using the specified component (usually a parser). ATerm
    sources can\'t be saved because this checker will fail, need to fix
    this.

[]{#TODO} TODO
--------------

-   Allow commandline parameters after component names in the dynamic
    composition - done
-   Create anonymous compositions/transformations for educational
    purposes (guess what composition or component has been invoked) -
    done
-   Support multiple inputs; this enables more complex transformation
    demos like [xml-tools](../Tools/XmlTools){.twikiLink} and Stratego
-   Seperate service (transformations) from user-interface (XML
    generation)
-   Allow saving of ATerm sources

\-- [NielsJanssen](../Main/NielsJanssen){.twikiLink} - 23 Oct 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
