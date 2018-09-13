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
    Page](http://www.program-transformation.org/edit/Stratego/JavaFront?t=1536825468)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/JavaFront)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/JavaFront)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/JavaFront?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/JavaFront?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    58](http://www.program-transformation.org/view/Stratego/JavaFront?rev=1.58)
    [(diff 57)](http://www.program-transformation.org/rdiff/Stratego/JavaFront?rev1=1.58&rev2=1.57)
-   [Rev
    57](http://www.program-transformation.org/view/Stratego/JavaFront?rev=1.57)
    [(diff 56)](http://www.program-transformation.org/rdiff/Stratego/JavaFront?rev1=1.57&rev2=1.56)
-   [Rev
    56](http://www.program-transformation.org/view/Stratego/JavaFront?rev=1.56)
    [(diff 55)](http://www.program-transformation.org/rdiff/Stratego/JavaFront?rev1=1.56&rev2=1.55)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/JavaFront)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/JavaFront?template=oopsmore&param1=1.58&param2=1.58)
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
    \...](http://www.program-transformation.org/oops/Stratego/JavaFront?template=oopsmore&param1=1.58&param2=1.58)
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
Java-front {#java-front .twikiTopicTitle}
==========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Features](JavaFront#Features)
    -   [Available Versions of
        Java](JavaFront#Available_Versions_of_Java)
    -   [Quality and Compliance](JavaFront#Quality_and_Compliance)
-   [Documentation](JavaFront#Documentation)
    -   [Publications](JavaFront#Publications)
-   [Download](JavaFront#Download)
    -   [Stable Releases](JavaFront#Stable_Releases)
    -   [Latest Developments](JavaFront#Latest_Developments)
    -   [Installation](JavaFront#Installation)
-   [Project Info](JavaFront#Project_Info)
    -   [Issue Tracking](JavaFront#Issue_Tracking)
    -   [Contact and Mailing List](JavaFront#Contact_and_Mailing_List)
    -   [Source Repository](JavaFront#Source_Repository)
    -   [Team](JavaFront#Team)
    -   [License](JavaFront#License)
-   [Related Software](JavaFront#Related_Software)
:::

[]{#Features} Features
----------------------

[Java-front](JavaFront){.twikiLink} is a package you can use to generate
or transform Java code. It contains a handcrafted [SDF](SDF){.twikiLink}
grammar for [Java](../Transform/JavaLanguage){.twikiLink}, [Stratego
signatures](StrategoSignature){.twikiLink} generated from this grammar
and a handcrafted [pretty printer](PrettyPrinter){.twikiLink}.

Some of the unique features of Java-front are:

-   Modular and extensible syntax definition for Java
-   Full support for the new language features introduced in Java 5.0
-   Heavily tested pretty-printer, which inserts parentheses where
    necessary!
-   Option to preserve comments
-   Conversion of abstract syntax tree to XML possible

### []{#Available_Versions_of_Java} Available Versions of Java

Java-front supports Java 5.0. The syntax definition closely follows the
structure of the [Java Language Specifcation, Third
Edition](http://java.sun.com/docs/books/jls/) (JLS3). All new features
(generics, wildcards, varargs, static import, enums, foreach loop,
annotations) are supported. This syntax definition is called `Java-15`.

### []{#Quality_and_Compliance} Quality and Compliance

The Java grammar in Java-front is able to parse and pretty-print all the
Java sources in the GNU Classpath (over 2200 classes) and the Java 2 SDK
version 1.5.0 of Sun Microsystems (over 6500 classes). The results of
the pretty-printer are verified.

A note on compliance: [SDF](SDF){.twikiLink} assumes an ASCII world.
This means that only ASCII input characters are supported. Fortunately,
most sources do not use unescaped characters outside the ASCII range, so
this is not a big problem in practice.

[]{#Documentation} Documentation
--------------------------------

-   Manual: [Getting Started with
    java-front](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/java-front.html)
-   [Browse](http://releases.strategoxt.org/docs/syntax/java-front/stable/docs/html/languages/java-15/Main.sdf.html)
    the syntax definition of Java online.
-   [Embedding of Java in
    Stratego](http://releases.strategoxt.org/docs/syntax/java-front/stable/docs/html/languages/java/EmbeddedJava.sdf.html)

### []{#Publications} Publications

Java-front has been used for the following research publications:

-   Lennart C. L. Kats, Martin Bravenboer, and Eelco Visser. *Mixing
    Source and Bytecode. A Case for Compilation by Normalization.* In
    Proceedings of the 23st ACM SIGPLAN *Conference on Object-Oriented
    Programming, Systems, Languages, and Applications ([OOPSLA
    2008](http://www.oopsla.org/2008/))*, Nashville, Tennessee, USA,
    October 2008.
    ([pdf](http://www.lclnet.nl/publications/TUD-SERG-2008-030.pdf))

<!-- -->

-   Martin Bravenboer, Éric Tanter, and Eelco Visser. *Declarative,
    Formal, and Extensible Syntax Definition for AspectJ - A Case for
    Scannerless Generalized-LR Parsing*. In Proceedings of the 21st ACM
    SIGPLAN *Conference on Object-Oriented Programming, Systems,
    Languages, and Applications ([OOPSLA
    2006](http://www.oopsla.org/2006/))*, Portland, USA, October 2006.
    ([pdf](http://martin.bravenboer.name/docs/oopsla06.pdf))

<!-- -->

-   Eric Tanter. *An Extensible Kernel Language for AOP*. In Proceedings
    of the AOSD Workshop on Open and Dynamic Aspect Languages (ODAL
    2006). March 2006, Bonn, Germany.

<!-- -->

-   Mina Askari and Raihan Al-Ekram. *Bringing Smalltalk Blocks to Java
    Through Transformation Techniques*. 2005 IBIMA Conference on Theory
    and Practice of Software Engineering for the 21st Century (TPSE
    2005). Cairo, Egypt. December 13 - 15, 2005
    ([pdf](http://swag.uwaterloo.ca/~rekram/publications/tpse2005--bringing-smalltalk-blocks-to-java-through-transformation.pdf))

<!-- -->

-   Martin Bravenboer, Rob Vermaas, Jurgen Vinju and Eelco Visser.
    *Generalized Type-Based Disambiguation of Meta Programs with
    Concrete Object Syntax*. In *Proceedings of the Fourth International
    Conference on Generative Programming and Component Engineering
    ([GPCE 2005](../Gpce05/index.html))*, Tallinn, Estonia,
    September 2005.
    ([pdf](http://www.cs.uu.nl/~martin/docs/disamb-gpce05.pdf),
    [presentation](http://www.cs.uu.nl/~martin/docs/gpce05-slides.pdf))

<!-- -->

-   Anya Helene Bagge, Martin Bravenboer, Karl Trygve Kalleberg, Koen
    Muilwijk, and Eelco Visser. *Adaptive Code Reuse by Aspects, Cloning
    and Renaming*. Technical Report UU-CS-2005-031, Department of
    Information and Computing Sciences, Universiteit Utrecht, Utrecht,
    The Netherlands, August 2005.
    ([pdf](http://archive.cs.uu.nl/pub/RUU/CS/techreps/CS-2005/2005-031.pdf))

<!-- -->

-   Martin Bravenboer, Rene de Groot, and Eelco Visser. *MetaBorg in
    Action: Examples of Domain-specific Language Embedding and
    Assimilation using Stratego/XT*. In *Proceedings of the Summer
    School on Generative and Transformational Techniques in Software
    Engineering ([GTTSE 2005](http://www.di.uminho.pt/GTTSE2005))*,
    Braga, Portugal, July, 2005. (draft:
    [pdf](http://www.cs.uu.nl/~martin/docs/metaborg-gttse05.pdf))

<!-- -->

-   Martin Bravenboer and Eelco Visser. *Concrete Syntax for Objects.
    Domain-Specific Language Embedding and Assimilation without
    Restrictions*. In Douglas C.Schmidt (ed.) *Proceedings of the 19th
    ACM SIGPLAN conference on Object-Oriented Programing, Systems,
    Languages, and Applications ([OOPSLA\'04](http://www.oopsla.org)).*
    Vancouver, Canada. October 2004.
    ([pdf](http://www.cs.uu.nl/~visser/ftp/BV04.pdf))

[]{#Download} Download
----------------------

### []{#Stable_Releases} Stable Releases

The current release is:

-   [java-front-0.9](JavaFrontRelease09){.twikiLink}

Older releases:

-   [java-front-0.8](JavaFrontRelease08){.twikiLink}
-   [java-front-0.7](JavaFrontRelease07){.twikiLink}
-   [java-front-0.6](JavaFrontRelease06){.twikiLink}
-   [java-front-0.5](JavaFrontRelease05){.twikiLink}

### []{#Latest_Developments} Latest Developments

Distributions (tarball, rpm, srpm) of the head revision are created
continuously:

-   <http://hydra.nixos.org/jobset/strategoxt-java/java-front-trunk>

The distributions contain the latest of the latest developments, but if
you really want to, the latest sources can be checked out using:

      svn checkout https://svn.strategoxt.org/repos/StrategoXT/java-front/trunk

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

[]{#Project_Info} Project Info
------------------------------

### []{#Issue_Tracking} Issue Tracking

We use JIRA to keep track of issues. Please report any issues that you
encounter!

-   <http://yellowgrass.org/project/JavaFront>

### []{#Contact_and_Mailing_List} Contact and Mailing List

Please send questions to the [users\@strategoxt.org mailing
list](https://mailman.st.ewi.tudelft.nl/listinfo/users). Also, the
Java-front developers are usually available on IRC at
[irc.freenode.net/stratego](irc://irc.freenode.net/stratego). Feel free
to drop by!

### []{#Source_Repository} Source Repository

The sources of Java-front are available from Subversion.

-   <https://svn.strategoxt.org/repos/StrategoXT/java-front/trunk>

### []{#Team} Team

Contributors:

-   [Martin Bravenboer](http://martin.bravenboer.name) (lead developer)
-   [Rob Vermaas](../Main/RobVermaas){.twikiLink}
-   [Rene de Groot](../Main/ReneDeGroot){.twikiLink}
-   [Eelco Dolstra](http://www.cs.uu.nl/people/eelco/)

Feedback and bug reports:

-   [Eelco Visser](../Main/EelcoVisser){.twikiLink}
-   Jurgen Vinju
-   Mikal Ziane
-   Pankaj Risbood
-   [Valentin
    David](http://www.lrde.epita.fr/cgi-bin/twiki/view/Main/ValentinDavid)
-   [Arthur van Dam](http://arthur.van-dam.net/twiki)

Sponsors:

-   [Department of Information and Computing Sciences, University of
    Utrecht](http://www.cs.uu.nl)
-   [NWO Jacquard](http://www.jacquard.nl/) project
    [TraCE](http://www.cs.uu.nl/wiki/Trace/WebHome)

### []{#License} License

Java-front is [LGPL](LGPL){.twikiLink} (GNU Lesser General Public
License) software.

[]{#Related_Software} Related Software
--------------------------------------

-   [Java-borg](JavaBorg){.twikiLink}, which is based on Java-front,
    illustrates how to implement Java extensions.

<!-- -->

-   [Dryad](TheDryad){.twikiLink} is a set of Java compiler components.
    The application of these components is not restricted to compilers:
    Java program transformations profit from the disambiguation and
    semantics analysis components in Dryad. Dryad is based on
    Java-front.

<!-- -->

-   [AspectJ-front](AspectJFront){.twikiLink} provides a syntax
    definition and parser for AspectJ. AspectJ-front is based on
    Java-front.

<!-- -->

-   [Jimple-front](JimpleFront){.twikiLink} provides support for the
    [Jimple](http://www.sable.mcgill.ca/soot/) 3-address representation
    of Java bytecode, which is a useful representation for program
    analysis and transformation.

<!-- -->

-   [STRJ](STRJ){.twikiLink} compiles
    [Stratego](StrategoLanguage){.twikiLink} to Java.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
