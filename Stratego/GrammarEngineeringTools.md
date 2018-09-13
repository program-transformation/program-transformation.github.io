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
    Page](http://www.program-transformation.org/edit/Stratego/GrammarEngineeringTools?t=1536825585)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/GrammarEngineeringTools)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/GrammarEngineeringTools)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/GrammarEngineeringTools?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/GrammarEngineeringTools?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    8](http://www.program-transformation.org/view/Stratego/GrammarEngineeringTools?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/GrammarEngineeringTools?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Stratego/GrammarEngineeringTools?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/GrammarEngineeringTools?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Stratego/GrammarEngineeringTools?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/GrammarEngineeringTools?rev1=1.6&rev2=1.5)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/GrammarEngineeringTools)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/GrammarEngineeringTools?template=oopsmore&param1=1.8&param2=1.8)
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
    \...](http://www.program-transformation.org/oops/Stratego/GrammarEngineeringTools?template=oopsmore&param1=1.8&param2=1.8)
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
Stratego/XT Grammar Engineering Tools {#strategoxt-grammar-engineering-tools .twikiTopicTitle}
=====================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Introduction](GrammarEngineeringTools#Introduction)
-   [Documentation](GrammarEngineeringTools#Documentation)
    -   [Research Papers](GrammarEngineeringTools#Research_Papers)
    -   [Blogs](GrammarEngineeringTools#Blogs)
    -   [Samples](GrammarEngineeringTools#Samples)
    -   [Simple Examples](GrammarEngineeringTools#Simple_Examples)
-   [Download](GrammarEngineeringTools#Download)
    -   [Latest
        Developments](GrammarEngineeringTools#Latest_Developments)
    -   [Installation](GrammarEngineeringTools#Installation)
-   [Success Stories](GrammarEngineeringTools#Success_Stories)
-   [Project Info](GrammarEngineeringTools#Project_Info)
    -   [Contact and Mailing
        List](GrammarEngineeringTools#Contact_and_Mailing_List)
    -   [Source Repository](GrammarEngineeringTools#Source_Repository)
    -   [Team](GrammarEngineeringTools#Team)
    -   [License](GrammarEngineeringTools#License)
-   [Related Projects and
    Tools](GrammarEngineeringTools#Related_Projects_and_Tools)
:::

[]{#Introduction} Introduction
------------------------------

The Stratego/XT Grammar Engineering Tools is a collection of tools for
the recovery, development, testing, and maintenance of grammars.
Currently, the package mainly provides tools to support the recovery and
comparison of *precedence rules* from YACC and [SDF](SDF){.twikiLink}
grammars. Also, the package could be used as the basis of other tools
that analyze YACC generated parsers.

[]{#Documentation} Documentation
--------------------------------

### []{#Research_Papers} Research Papers

-   Eric Bouwers, Martin Bravenboer, and Eelco Visser. **Grammar
    Engineering Support for Precedence Rule Recovery and Compatibility
    Checking**. In *Proceedings of LDTA\'07, Seventh Workshop on
    Language Descriptions, Tools and Applications* at ETAPS\'07, Braga,
    Portugal, March 2007.
    ([pdf](http://martin.bravenboer.name/docs/ldta07.pdf),
    [slides](http://martin.bravenboer.name/docs/ldta07-slides.pdf))

### []{#Blogs} Blogs

-   [Martin Bravenboer](http://mbravenboer.blogspot.com)
    -   [Blogs tagged with Grammar Engineering
        Tools](http://mbravenboer.blogspot.com/search/label/grammar%20engineering%20tools)

<!-- -->

-   [Eric Bouwers](http://ericbouwers.blogspot.com)
    -   [Blogs tagged with Grammar Engineering
        Tools](http://ericbouwers.blogspot.com/search/label/Grammar%20Engineering%20Tools)

### []{#Samples} Samples

Examples of how to use the tools are available in the `samples`
directory. The samples are currently **not** distributed in the tarball,
so you need to check them out from [their location in
Subversion](https://svn.cs.uu.nl:12443/repos/StrategoXT/grammar-engineering-tools/trunk/samples/).

The `samples/expr` directory provides a series of examples based on a
variety of simple expression grammars. The `samples/c` and `samples/php`
grammars are used for larger examples of how to apply the tools to a
series of C and PHP grammars.

Every sample directory has a script `maak` (Dutch for make) that you can
invoke to run the tools on the sample.

### []{#Simple_Examples} Simple Examples

The following example illustrate how to invoke the various tools.

Precedence rules of a YACC grammar:

    $ bison expr.y -o expr.c --report=all
    $ yacc-precedence -i expr.output -s E
    <E -> <E -> E '+' E> '*' E>
    <E -> E '*' <E -> E '*' E>>
    <E -> E '*' <E -> E '+' E>>
    <E -> E '+' <E -> E '+' E>>

Precedence rules of an [SDF](SDF){.twikiLink} grammar:

    $ sdf2table -i expr.sdf
    $ sglr-precedence -i expr.tbl -s E
    <E -> E "+" <E -> E "+" E>>
    <E -> <E -> E "+" E> "*" E>
    <E -> E "*" <E -> E "+" E>>
    <E -> E "*" <E -> E "*" E>>

Comparing two precedence rule sets (example of unequal grammars) :

    $ sglr-precedence -i expr.tbl -s E --common -o expr.sglrprec
    $ yacc-precedence -i expr.output -s E --common -o expr.yaccprec
    $ common-precedence-equality -i expr.sglrprec expr.yaccprec
    Some precedence rules of first are not defined in second:
      <E -> <E -> E "+" E> "-" E>
      <E -> E "-" <E -> E "+" E>>
      <E -> E "-" <E -> E "-" E>>
      <E -> <E -> E "-" E> "*" E>
      <E -> E "*" <E -> E "-" E>>
    Some precedence rules of second are not defined in first:
      <E -> E "*" <E -> E "*" E>>

Or using bash process subtitution:

    $ common-precedence-equality -i \
      <(sglr-precedence -i expr.tbl -s E --common) \
      <(yacc-precedence -i expr.output -s E --common)

Example of two equal grammars:

    $ common-precedence-equality -i expr.sglrprec expr.yaccprec
    All precedence rules of first are defined in second.
    All precedence rules of second are defined in first.

Before comparing precedence rules it is useful to compare productions
first.

    $ common-precedence-production-equality -i expr.sglrprec expr.yaccprec
    Some productions of first are not defined in second:
      E -> E "-" E
    All productions of second are defined in first.

Extract productions used in YACC precedence rules:

    $ yacc-precedence -i expr.output --common -s E  | common-precedence-productions
    E -> E "*" E
    E -> E "+" E

Extract productions used in [SDF](SDF){.twikiLink}/SGLR precedence
rules:

    $ sglr-precedence -i expr.tbl --common -s E  | common-precedence-productions
    E -> E "+" E
    E -> E "*" E

[]{#Download} Download
----------------------

### []{#Latest_Developments} Latest Developments

Distributions (tarball, rpm, srpm) of the head revision are created
continuously:

-   <http://releases.strategoxt.org/strategoxt-grammar-engineering-tools-unstable-latest/>

The distributions contain the latest of the latest developments, but if
you really want to, the latest sources can be checked out using:

      svn checkout https://svn.strategoxt.org/repos/StrategoXT/grammar-engineering-tools/trunk

Before you can configure the package as described above you have to run
the `./bootstrap` script.

### []{#Installation} Installation

Install the package with the usual sequence of commands:

    $ ./configure
    $ make
    $ make install

You might need to set your `PKG_CONFIG_PATH` if you did not install the
dependencies in a standard location. Configure will tell you to do this
if it cannot find aterm, sdf or strategoxt.

[]{#Success_Stories} Success Stories
------------------------------------

Until now, the precedence tools have reported precedence issues for
every single grammar that is a derivative from some standard (try your
grammar and see if you can make this statement invalid ;) )

-   The precedence tools have reported a bug in the
    [C-Transformers](http://www.lrde.epita.fr/cgi-bin/twiki/view/Transformers/CTransformers)
    grammar for C99, which has now been fixed (revision 1613).

<!-- -->

-   The precedence tools have reported several problems in the open
    source [PHP Compiler](http://www.phpcompiler.org/), which was
    [reported by
    us](https://altoure.vm.bytemark.co.uk/pipermail/phc-general/2006-December/thread.html#168)
    and fixed soon after by the developers. These problems have been
    found by comparing the precedence rules of the PHP Compiler to the
    official PHP implementation.

<!-- -->

-   The precedence tools have reported several problems in the ANSI C
    grammar of the [SDF Library](http://www.meta-environment.org), which
    have been reported to the maintainers as issues
    [669](http://bugzilla.sen.cwi.nl:8080/show_bug.cgi?id=669),
    [670](http://bugzilla.sen.cwi.nl:8080/show_bug.cgi?id=670), and
    [671](http://bugzilla.sen.cwi.nl:8080/show_bug.cgi?id=671).

<!-- -->

-   In an ongoing effort to define the precise syntax of PHP in
    [SDF](SDF){.twikiLink} (see [PHP-front](../PHP/PhpFront)), the
    precedence tools are used to recover the precedence rules from the
    YACC grammar that is part of the official PHP implementation. These
    precedence rules are now being used to derive the appropriate
    [SDF](SDF){.twikiLink} priority definitions.

[]{#Project_Info} Project Info
------------------------------

### []{#Contact_and_Mailing_List} Contact and Mailing List

Please send questions to the [stratego\@cs.uu.nl mailing
list](https://mail.cs.uu.nl/mailman/listinfo/stratego). Also, the
developers are usually available on IRC at
[irc.freenode.net/stratego](irc://irc.freenode.net/stratego). Feel free
to drop by!

### []{#Source_Repository} Source Repository

The sources are available from Subversion.

-   <https://svn.cs.uu.nl:12443/repos/StrategoXT/grammar-engineering-tools/trunk>

### []{#Team} Team

Contributors:

-   [Martin Bravenboer](http://martin.bravenboer.name) (lead developer)
-   [Eric Bouwers](http://ericbouwers.blogspot.com/)

Feedback and bug reports:

-   [Eelco Visser](../Main/EelcoVisser){.twikiLink}

### []{#License} License

Stratego/XT Grammar Engineering Tools are GPL (GNU General Public
License) software.

[]{#Related_Projects_and_Tools} Related Projects and Tools
----------------------------------------------------------

-   [Amsterdam Engineering of
    Grammarware](http://www.cs.vu.nl/grammarware/)
    -   [Grammar Deployment Kit](http://gdk.sourceforge.net/)
    -   [Grammar Recovery Kit](http://www.cs.vu.nl/grammarware/grk/)

<!-- -->

-   [Meta-Environment](http://www.meta-environment.org), in particular
    its instantiations the ASF+SDF Meta-Environment and the
    [SDF](SDF){.twikiLink} Meta-Environment.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
