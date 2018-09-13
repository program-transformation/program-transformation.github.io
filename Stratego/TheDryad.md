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
    Page](http://www.program-transformation.org/edit/Stratego/TheDryad?t=1536825509)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/TheDryad)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/TheDryad)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/TheDryad?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/TheDryad?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    33](http://www.program-transformation.org/view/Stratego/TheDryad?rev=1.33)
    [(diff 32)](http://www.program-transformation.org/rdiff/Stratego/TheDryad?rev1=1.33&rev2=1.32)
-   [Rev
    32](http://www.program-transformation.org/view/Stratego/TheDryad?rev=1.32)
    [(diff 31)](http://www.program-transformation.org/rdiff/Stratego/TheDryad?rev1=1.32&rev2=1.31)
-   [Rev
    31](http://www.program-transformation.org/view/Stratego/TheDryad?rev=1.31)
    [(diff 30)](http://www.program-transformation.org/rdiff/Stratego/TheDryad?rev1=1.31&rev2=1.30)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/TheDryad)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/TheDryad?template=oopsmore&param1=1.33&param2=1.33)
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
    \...](http://www.program-transformation.org/oops/Stratego/TheDryad?template=oopsmore&param1=1.33&param2=1.33)
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
Dryad - The Tree Nymph {#dryad---the-tree-nymph .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

Dryad is a natural [female tree
spirit](http://en.wikipedia.org/wiki/Dryad), associated with trees.
Also, it is a collection of tools for developing transformation systems
for Java source and bytecode.

::: {.twikiToc}
-   [Overview of Features](TheDryad#Overview_of_Features)
    -   [Dryad Bytecode Interface](TheDryad#Dryad_Bytecode_Interface)
    -   [Dryad Front: Disambiguation and
        Type-Checking](TheDryad#Dryad_Front_Disambiguation_and_T)
    -   [Dryad Library for
        Stratego](TheDryad#Dryad_Library_for_Stratego)
-   [Documentation](TheDryad#Documentation)
-   [Download](TheDryad#Download)
    -   [Dependencies](TheDryad#Dependencies)
-   [Project Info](TheDryad#Project_Info)
    -   [Issue Tracking](TheDryad#Issue_Tracking)
    -   [Contact and Mailing List](TheDryad#Contact_and_Mailing_List)
    -   [Source Repository](TheDryad#Source_Repository)
    -   [Team](TheDryad#Team)
    -   [License](TheDryad#License)
-   [Related Software](TheDryad#Related_Software)
:::

[]{#Overview_of_Features} Overview of Features
----------------------------------------------

### []{#Dryad_Bytecode_Interface} Dryad Bytecode Interface

Dryad implements a conversion from the class file format to ATerm and
vice versa.

`class2aterm` is a disassembler for Java bytecode. It produces an ATerm
representation of a Java `.class` file. `class2aterm` can be used to
obtain just the types of the members of a class, or it can be used to
decompile the full .class file (i.e. including code). Pass the `-c`
option to disassemble code.

`aterm2class` is an assembler for Java bytecode. It accepts an ATerm
representation of a `.class` file and constructs a real `.class` file
from that.

The format of the bytecode representation in ATerms is defined in a tree
grammar:
[ClassTree.rtg](https://svn.cs.uu.nl:12443/repos/StrategoXT/dryad/trunk/classtree/ClassTree.rtg).

### []{#Dryad_Front_Disambiguation_and_T} Dryad Front: Disambiguation and Type-Checking

`dryad-front` is a composition of some compiler components in the
front-end of the Dryad compiler. Currently, its main component is the
qualification and reclassification of names. This is an essential
component for any tool that needs to analyse or transform Java code.

After parsing a Java source files, the tree contains many ambiguous
constructs. For example, the parser on its own cannot determine whether
the identifier `System` in `System.out.println("Hello world!")` refers
to a package, class, field or local variable. Similarly, `out` might be
a package, a class, an inner classes of the `System`, a field of the
class `System` and so on. Dryad-front resolves these ambiguities by
analyzing the sources and reading the bytecode of the classes that are
used. It returns a fully disambiguated abstract syntax tree.

`dryad-front` also provides a type checker for Java, which annotates all
expressions with their type. This type checker is still under
development, but you can already use it by passing `--tc on` to
`dryad-front`.

### []{#Dryad_Library_for_Stratego} Dryad Library for Stratego

Dryad also provides a large library of functions useful for developing
Java transformation systems in Stratego. All of the components of Dryad
are based on this library. The main feature of the library is a unified
representation of Java bytecode and source code classes in the *Dryad
Model*. Classes can be loaded from the Dryad Repository and a
`java.lang.reflect` like API provides access to members, types,
superclasses, etc.

[]{#Documentation} Documentation
--------------------------------

-   [Presentation](ftp://ftp.stratego-language.org/pub/stratego/SUD05/dryad.pdf)
    of Dryad at the [Sixth Stratego User
    Days](SixthStrategoUserDays){.twikiLink}
-   [Tutorial](http://martin.bravenboer.name/docs/gpce06-tutorial-slides.pdf)
    on Building Java Transformations with Stratego/XT at [GPCE
    2006](http://hope.cs.rice.edu/twiki/bin/view/GPCE06/)
-   [API
    documentation](http://releases.strategoxt.org/docs/api/libdryad/stable/docs/)
    for the Dryad library is available online.

[]{#Download} Download
----------------------

Distributions are build continuously:

-   <http://releases.strategoxt.org/dryad/unstable/>

We advice to use [Nix](http://www.cs.uu.nl/wiki/Trace/Nix) for
installing Dryad. Nix provides one-click installation of Dryad and all
its dependencies. Nix will make it very easy to stay up-to-date with the
latest developments without any installation and configuration problems.

### []{#Dependencies} Dependencies

Installation from a source tarball requires the following packages:

-   Latest Stratego/XT
-   [JavaFront](JavaFront){.twikiLink}, latest pre-release
-   [JDK 5.0](http://java.sun.com/j2se/1.5.0/download.jsp) (Dryad uses
    5.0 language features)

The `configure` script does not require any explicit configuration.
Dryad will try to find the JDK by searching the path for `javac`.
Stratego/XT and Java-front will be found by `pkg-config`.

If you build Dryad from Subversion, then there are some additional
dependencies:

-   [BCEL](http://jakarta.apache.org/bcel/index.html) 5.1
    (`--with-bcel`)
    -   jakarta-regexp 1.3 (`--with-regexp`)
-   [ATerm Library](../Tools/ATermLibrary){.twikiLink} for Java
    -   aterm-java 1.6 (`--with-aterm-java`)
    -   jjtraveler 0.4.3 (`--with-jjtraveler`)
    -   shared-objects 1.4 (`--with-shared-objects`)

[]{#Project_Info} Project Info
------------------------------

### []{#Issue_Tracking} Issue Tracking

We use JIRA to keep track of issues. Please report any issues that you
encounter!

-   <http://yellowgrass.org/project/Dryad>

### []{#Contact_and_Mailing_List} Contact and Mailing List

Please send questions to the [stratego\@cs.uu.nl mailing
list](https://mail.cs.uu.nl/mailman/listinfo/stratego). Also, the Dryad
developers are usually available on IRC at
[irc.freenode.net/stratego](irc://irc.freenode.net/stratego). Feel free
to drop by!

### []{#Source_Repository} Source Repository

The sources of Dryad are available from Subversion.

-   <https://svn.strategoxt.org/repos/StrategoXT/dryad/trunk>

### []{#Team} Team

Committers:

-   [Martin Bravenboer](http://martin.bravenboer.name) (lead developer)
-   [Karl Trygve Kalleberg](../Main/KarlTrygveKalleberg){.twikiLink}
-   [Rob Vermaas](../Main/RobVermaas){.twikiLink}
-   [Lennart Kats](http://www.lennartkats.nl/)

Committers emeritus:

-   [Dave Clarke](http://homepages.cwi.nl/~dave/) developed a first
    prototype of the bytecode to aterm conversion.
-   [Rene de Groot](../Main/ReneDeGroot){.twikiLink}

Feedback and bug reports:

-   [Eelco Visser](../Main/EelcoVisser){.twikiLink} - design feedback
-   Gerrit van den Geest - bug reports for bytecode interface
-   Huib van den Brink - bug reports for bytecode interface
-   [Valentin
    David](http://www.lrde.epita.fr/cgi-bin/twiki/view/Main/ValentinDavid) -
    bug reports for disambiguation and type checking

Sponsors:

-   [Department of Information and Computing Sciences, University of
    Utrecht](http://www.cs.uu.nl)
-   [NWO Jacquard](http://www.jacquard.nl/) project
    [TraCE](http://www.cs.uu.nl/wiki/Trace/WebHome)

### []{#License} License

Dryad is [LGPL](LGPL){.twikiLink} (GNU Lesser General Public License)
software. This means that you can use the Dryad Library (and tools)
without being required to distribute your software under the GPL.

[]{#Related_Software} Related Software
--------------------------------------

-   [Java-front](JavaFront){.twikiLink} is a package for generation or
    transformation of Java code, and forms the foundation of Dryad.

<!-- -->

-   [The Dryad Compiler](TheDryadCompiler){.twikiLink} uses Dryad to
    compile a mixed language of Java and bytecode to Java class files.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
