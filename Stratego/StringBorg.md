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
    Page](http://www.program-transformation.org/edit/Stratego/StringBorg?t=1536825711)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StringBorg)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StringBorg)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StringBorg?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StringBorg?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    14](http://www.program-transformation.org/view/Stratego/StringBorg?rev=1.14)
    [(diff 13)](http://www.program-transformation.org/rdiff/Stratego/StringBorg?rev1=1.14&rev2=1.13)
-   [Rev
    13](http://www.program-transformation.org/view/Stratego/StringBorg?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/Stratego/StringBorg?rev1=1.13&rev2=1.12)
-   [Rev
    12](http://www.program-transformation.org/view/Stratego/StringBorg?rev=1.12)
    [(diff 11)](http://www.program-transformation.org/rdiff/Stratego/StringBorg?rev1=1.12&rev2=1.11)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StringBorg)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StringBorg?template=oopsmore&param1=1.14&param2=1.14)
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
    \...](http://www.program-transformation.org/oops/Stratego/StringBorg?template=oopsmore&param1=1.14&param2=1.14)
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
StringBorg {#stringborg .twikiTopicTitle}
==========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Introduction](StringBorg#Introduction)
    -   [Supported languages](StringBorg#Supported_languages)
-   [Download](StringBorg#Download)
    -   [Stable Releases](StringBorg#Stable_Releases)
    -   [Latest Developments](StringBorg#Latest_Developments)
    -   [Latest Samples](StringBorg#Latest_Samples)
    -   [Installation](StringBorg#Installation)
    -   [Dependencies](StringBorg#Dependencies)
-   [Project Info](StringBorg#Project_Info)
    -   [Issue Tracking](StringBorg#Issue_Tracking)
    -   [Contact and Mailing List](StringBorg#Contact_and_Mailing_List)
    -   [Source Repository](StringBorg#Source_Repository)
    -   [Team](StringBorg#Team)
    -   [License](StringBorg#License)
-   [Related Software](StringBorg#Related_Software)
:::

[]{#Introduction} Introduction
------------------------------

[StringBorg](StringBorg){.twikiLink} is a solution to injection attacks
for arbitrary languages. [StringBorg](StringBorg){.twikiLink} prevents
injection attacks by embedding the syntax of guest languages (for
example SQL, LDAP, Shell, XPath) in the host language (PHP, Java) and
applying the *proper escaping* rules and *positive checking*
automatically to all direct or indirect user input.

Documentation:

-   Technical report: *\"Preventing Injection Attacks with Syntax
    Embeddings \-- A Host and Guest Language Independent Approach\"*
    [available](http://swerl.tudelft.nl/bin/view/Main/TechnicalReports)
    from the website of our research group
    ([pdf](http://swerl.tudelft.nl/twiki/pub/Main/TechnicalReports/TUD-SERG-2007-003.pdf)).
-   Blog: <http://mbravenboer.blogspot.com/search/label/stringborg>

### []{#Supported_languages} Supported languages

Currently, [StringBorg](StringBorg){.twikiLink} supports PHP and Java as
host languages.

Supported guest languages are:

-   SQL-92
-   LDAP search filters
-   Shell
-   XPath
-   XML

If you have suggestions or requests for languages that we should
support, then please let us know (contact one of the developers or join
our mailing list).

[]{#Download} Download
----------------------

### []{#Stable_Releases} Stable Releases

Currently no stable releases are available.

### []{#Latest_Developments} Latest Developments

Distributions (tarball, rpm, srpm) of the head revision are created
continuously. We advice to install StringBorg using
[Nix](http://nix.cs.uu.nl) one-click install or RPM.

-   <http://buildfarm.st.ewi.tudelft.nl/releases/strategoxt/stringborg-unstable-latest/>

The distributions contain the latest of the latest developments, but if
you really want to, the latest sources can be checked out using:

      svn checkout https://svn.strategoxt.org/repos/StrategoXT/stringborg/trunk

Before you can configure the package as described above you have to run
the `./bootstrap` script.

### []{#Latest_Samples} Latest Samples

Samples for [StringBorg](StringBorg){.twikiLink} are available in the
standard distribution (subdirectory `stringborg-samples`), but also as a
separate package to make the samples easier to use if you use a
deployment system (RPM, Nix) for the installation of StringBorg. The
latest tarball of the samples can be obtained from:

-   <http://buildfarm.st.ewi.tudelft.nl/releases/strategoxt/stringborg-samples-unstable-latest/>

You need to install the samples: a plain `./configure` will configure
the package (all its dependencies should be detected automatically) and
you can make the samples using `make check`. In the various
subdirectories you can of course also run the individual targets to
generate specific files. See `Makefile.samples` for information on the
targets.

### []{#Installation} Installation

Install the package with the usual sequence of commands:

    $ ./configure
    $ make
    $ make install

You might need to set your `PKG_CONFIG_PATH` if you did not install the
dependencies in a standard location. Configure will tell you to do this
if it cannot find aterm, sdf, strategoxt, java-front, or sql-front.

### []{#Dependencies} Dependencies

StringBorg depends on:

-   ATerm library (aterm)
-   Latest unstable SDF2 Bundle (sdf2-bundle)
-   Latest unstable [Stratego/XT](StrategoDownload){.twikiLink}
    (strategoxt)
-   Latest unstable [Java-front](JavaFront){.twikiLink} (java-front)
-   Latest unstable [SQL-front](SqlFront){.twikiLink} (sql-front)
-   Latest unstable [PHP-front](../PHP/PhpFront){.twikiLink} (php-front)
-   Java Development Kit providing `java` and `javac`.

[]{#Project_Info} Project Info
------------------------------

### []{#Issue_Tracking} Issue Tracking

We use JIRA to keep track of issues. Please report any issues that you
encounter!

-   <http://yellowgrass.org/BORG>

### []{#Contact_and_Mailing_List} Contact and Mailing List

Please send questions to the [stratego\@cs.uu.nl mailing
list](https://mail.cs.uu.nl/mailman/listinfo/stratego). Also, the
StringBorg developers are usually available on IRC at
[irc.freenode.net/stratego](irc://irc.freenode.net/stratego). Feel free
to drop by!

### []{#Source_Repository} Source Repository

The sources of StringBorg are available from Subversion.

-   <https://svn.cs.uu.nl:12443/repos/StrategoXT/stringborg/trunk>

### []{#Team} Team

Contributors:

-   [Martin Bravenboer](http://martin.bravenboer.name) (lead developer)
-   [Eelco Dolstra](http://www.cs.uu.nl/people/eelco/)
-   [Eelco Visser](http://www.cs.uu.nl/people/visser/)

Sponsors:

-   [Utrecht University, Department of Information and Computing
    Sciences](http://www.cs.uu.nl)
-   [Delft University of Technology, Software Engineering Research
    Group](http://swerl.tudelft.nl/)
-   [NWO Jacquard](http://www.jacquard.nl/) project
    [TraCE](http://www.cs.uu.nl/wiki/Trace/WebHome)

### []{#License} License

[StringBorg](StringBorg){.twikiLink} is [LGPL](LGPL){.twikiLink} (GNU
Lesser General Public License) software.

[]{#Related_Software} Related Software
--------------------------------------

-   [Java-front](JavaFront){.twikiLink} provides a syntax definition and
    pretty-printer for Java.
-   [SQL-front](SqlFront){.twikiLink} provides a syntax for definition
    for SQL.
-   [PHP-front](../PHP/PhpFront){.twikiLink} provides a syntax for
    definition for PHP.
-   [www.metaborg.org](http://www.metaborg.org) gives an overview of
    [MetaBorg](MetaBorg){.twikiLink} related software and publications.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
