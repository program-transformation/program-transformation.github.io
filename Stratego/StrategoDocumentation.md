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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoDocumentation?t=1536825357)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoDocumentation)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoDocumentation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoDocumentation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoDocumentation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    57](http://www.program-transformation.org/view/Stratego/StrategoDocumentation?rev=1.57)
    [(diff 56)](http://www.program-transformation.org/rdiff/Stratego/StrategoDocumentation?rev1=1.57&rev2=1.56)
-   [Rev
    56](http://www.program-transformation.org/view/Stratego/StrategoDocumentation?rev=1.56)
    [(diff 55)](http://www.program-transformation.org/rdiff/Stratego/StrategoDocumentation?rev1=1.56&rev2=1.55)
-   [Rev
    55](http://www.program-transformation.org/view/Stratego/StrategoDocumentation?rev=1.55)
    [(diff 54)](http://www.program-transformation.org/rdiff/Stratego/StrategoDocumentation?rev1=1.55&rev2=1.54)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoDocumentation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoDocumentation?template=oopsmore&param1=1.57&param2=1.57)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoDocumentation?template=oopsmore&param1=1.57&param2=1.57)
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
Documentation {#documentation .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

------------------------------------------------------------------------

[Note that Stratego is now part of the [Spoofax Language
Workbench](http://metaborg.org/spoofax), which provides an Eclipse
plugin for developing SDF and Stratego, and creating Eclipse IDE plugins
for your own language. See the Spoofax website for information and
downloads: <http://metaborg.org>. This website is still available for
historical purposes. Refer the new site for up-to-date documentation.
]{style="color:red;font-size:24px"}

------------------------------------------------------------------------

Stratego is a language for program transformation and XT is a collection
of tools for building and generating program transformation components.
Important components of the tool collection are the
[ATerm](http://www.aterm.org) exchange format and the syntax definition
formalism [SDF](../Sdf/WebHome){.twikiLink}. Together these ingredients
provide a very powerful toolbox for constructing program transformation
systems.

However, they are tools that need to be applied in construction, not a
ready made environment that magically solves your particular
transformation problem. The system is not restricted to a single trick,
nor is there a single way to solve a problem using these tools. To learn
to use these tools you\'ll need to invest some effort in learning the
concepts and architecture of Stratego/XT.

Note: This documentation here is kept in sync with the latest
integration build. If you are looking for documentation for an older,
stable release of Stratego, consult the corresponding [release
page](StrategoDownload){.twikiLink} of your version (bottom of that
page).

-   [Stratego/XT
    Manual](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/index.html)\
    The Stratego/XT Manual is a series of three books:

    -   [Stratego/XT
        Tutorial](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/tutorial.html)\
        Practical introduction to the Stratego language and XT tools.
    -   [Stratego/XT
        Examples](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/examples.html)\
        Introduction to Stratego/XT by example.
    -   [Stratego/XT Reference
        Manual](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/reference-manual.html)\
        Detailed description of the Stratego language and XT tools.

-   API and Source Documentation

    -   [libstratego-lib](http://releases.strategoxt.org/docs/api/libstratego-lib/stable/docs/)\
        Main Stratego Library providing generic traversals, I/O, and
        basic strategies for lists, hashtables, handling command-line
        options.
    -   [libstratego-sglr](http://releases.strategoxt.org/docs/api/libstratego-sglr/stable/docs/)\
        Stratego SGLR Library for parsing.
    -   [libstratego-gpp](http://releases.strategoxt.org/docs/api/libstratego-gpp/stable/docs/)\
        Stratego GPP Library for pretty-printing, based on the Box
        language for formatting text.
    -   [libstratego-rtg](http://releases.strategoxt.org/docs/api/libstratego-rtg/stable/docs/)\
        Stratego RTG Library for format checking, based on regular tree
        grammars.
    -   [libstratego-xtc](http://releases.strategoxt.org/docs/api/libstratego-xtc/stable/docs/)\
        Stratego XTC Library for finding and invoking external programs
        and resources.

    Extensions

    -   [libdryad](http://releases.strategoxt.org/docs/api/libdryad/stable/docs/)\
        Dryad library for Java program transformation
    -   [libphp-front](http://releases.strategoxt.org/docs/api/libphp-front/stable/docs/)\
        PHP-front library for PHP program transformation
    -   [more \...](http://releases.strategoxt.org/docs/api/)

    Search engine

    -   [XDoc Search](http://xdoc.martkolthof.nl)\
        All API documentation listed above can be searched with XDoc
        Search

-   Syntax Definitions

    -   [AspectJ](http://releases.strategoxt.org/docs/syntax/aspectj-front/stable/docs/html/languages/aspectj/JavaExtension.sdf.html)
    -   [Java](http://releases.strategoxt.org/docs/syntax/java-front/stable/docs/html/languages/java-15/Main.sdf.html)
    -   [Jimple](http://releases.strategoxt.org/docs/syntax/jimple-front/stable/docs/html/languages/jimple/Main.sdf.html)
    -   [PHP4](http://releases.strategoxt.org/docs/syntax/php-front/stable/docs/html/languages/php/version4/Main.sdf.html)
    -   [PHP5](http://releases.strategoxt.org/docs/syntax/php-front/stable/docs/html/languages/php/version5/Main.sdf.html)

-   [Publications](StrategoPublications){.twikiLink}\
    Research papers on the main principles, including examples.
-   [Program Transformation Course](http://www.cs.uu.nl/wiki/Pt)\
    Course about program transformation with Stratego at Universiteit
    Utrecht

Some documentation is not up to date or has been subsumed within the
previously mentioned documents. See [obsolete
documentation](ObsoleteDocumentation){.twikiLink}.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
