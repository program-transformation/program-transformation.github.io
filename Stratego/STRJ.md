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
    Page](http://www.program-transformation.org/edit/Stratego/STRJ?t=1536825367)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/STRJ)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/STRJ)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/STRJ?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/STRJ?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    14](http://www.program-transformation.org/view/Stratego/STRJ?rev=1.14)
    [(diff 13)](http://www.program-transformation.org/rdiff/Stratego/STRJ?rev1=1.14&rev2=1.13)
-   [Rev
    13](http://www.program-transformation.org/view/Stratego/STRJ?rev=1.13)
    [(diff 12)](http://www.program-transformation.org/rdiff/Stratego/STRJ?rev1=1.13&rev2=1.12)
-   [Rev
    12](http://www.program-transformation.org/view/Stratego/STRJ?rev=1.12)
    [(diff 11)](http://www.program-transformation.org/rdiff/Stratego/STRJ?rev1=1.12&rev2=1.11)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/STRJ)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/STRJ?template=oopsmore&param1=1.14&param2=1.14)
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
    \...](http://www.program-transformation.org/oops/Stratego/STRJ?template=oopsmore&param1=1.14&param2=1.14)
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
Stratego / [STRJ](STRJ){.twikiLink} {#stratego-strj .twikiTopicTitle}
===================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[STRJ](STRJ){.twikiLink} compiles
[Stratego](StrategoLanguage){.twikiLink} to Java, and is a Java-based
variation of the [Stratego Compiler](StrategoCompiler){.twikiLink}.

::: {.twikiToc}
-   [Introduction](STRJ#Introduction)
    -   [Known Issues and
        Limitations](STRJ#Known_Issues_and_Limitations)
    -   [Using External Applications and
        Libraries](STRJ#Using_External_Applications_and)
    -   [Java Integration](STRJ#Java_Integration)
-   [Download](STRJ#Download)
-   [Project Information](STRJ#Project_Information)
    -   [Source Code](STRJ#Source_Code)
    -   [Contributors](STRJ#Contributors)
    -   [License](STRJ#License)
    -   [Contact and Mailing List](STRJ#Contact_and_Mailing_List)
-   [Related Software](STRJ#Related_Software)
:::

[]{#Introduction} Introduction
------------------------------

The compiler comes in two flavors: one called `strj`, compiled with the
standard C-based
[strc](http://releases.strategoxt.org/strategoxt-manual/unstable/manual/chunk-chapter/ref-strc.html).
The second is a bootstrapped, cross-platform compiler that lives in
strategoxt.jar. Note that Stratego executables compiled with strj do not
support [XTC](XTC){.twikiLink} (since it depends on forking native
executables and assumes filesystem access) and the strategoxt.jar
compiler is no exception. This means that you have to explicitly specify
the import path of dependencies that would otherwise be resolved using
[XTC](XTC){.twikiLink}. Another difference between the two is that strj
still uses the C-based [SGLR](SGLR){.twikiLink} parser, while
strategoxt.jar uses [JSGLR](JSGLR){.twikiLink}.

Compiling a simple application from the command line with either
compiler is similar to doing so with the
[strc](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/ref-strc.html)
command:

      strj -i foo.str -la stratego-lib

or

      java -jar strategoxt.jar -i foo.str -la stratego-lib

It should be noted that at this time the compiler only outputs `.java`
source files and not `.class` files. Subsequent compilation should be
done using a standard Java compiler (ideally, in an automated fashion
using an Ant build script or Eclipse). The (non-portable) `strj-jar`
shell script can also help with command-line or scripted builds.

### []{#Known_Issues_and_Limitations} Known Issues and Limitations

The Stratego/J runtime implements most of the primitives of the natively
compiled version of Stratego, but some compatibility issues might arise.
In particular, the parsing primitives are implemented using
[JSGLR](JSGLR){.twikiLink}, the Java version of
[SGLR](SGLR){.twikiLink}, which may not be bug-for-bug compatible with
the C version of [SGLR](SGLR){.twikiLink}. Mainly, the post-parse filter
implementation might not always produce the same results. This
especially impacts the heuristic filters, which are disabled by default,
but used for Stratego\'s concrete syntax embedding. To work around any
problems, the native `strj` executable can be used to compile these
files, or they can be pre-parse them to `.rtree` files using
[parse-stratego](http://hydra.nixos.org/job/strategoxt-docs/strategoxt-manual/html/latest/download/1/manual/chunk-chapter/ref-parse-stratego.html).
A general recommendation may be to disable the heuristic filters in the
`.meta` files using the `HeuristicFilters(Off())` directive.

The standard Sun compiler can be quite slow when compiling large
Stratego projects. We recommend using ECJ (Eclipse Compiler for Java)
instead, which is much faster and less memory-intensive. ECJ is
distributed as part of Eclipse, and can be executed as follows:

      java -cp plugins/org.eclipse.jdt.core_*.jar  org.eclipse.jdt.internal.compiler.batch.Main

Many Linux distributions also provide a stand-alone version of ECJ
through their package manager. (Note that ECJ 3.3 and lower have a bug
that can be worked around with the `-Xecj33` flag.) When using the Sun
compiler, you may need to add option `-J-mx256m` to increase the
available heap space, and likely need to have a fair amount of patience
;)

Stratego programs compiled to Java do not have the same performance
characteristics as those compiled using the native Stratego compiler
strc. The exact numbers vary per application (some, such as the somewhat
artificial ASF+SDF benchmark, actually run faster on Java), but natively
compiled Stratego applications that include parsing and pretty-printing
are typically a factor two faster. Future optimizations, particularly in
the term library and in I/O, may make this gap smaller.

A final open issue is the stack usage by typical Stratego programs,
putting JVM implementations with a small default stack size at risk of
throwing a `StackOverflowException` (notably the Sun JVM on Linux). For
these systems, running the JVM with option `-ss4m` avoids the stack
overflow problem. (When this parameter is not set and a stack overflow
occurs, compiled applications will hint at this setting.)

While the [XTC](XTC){.twikiLink} standard library strategies (such as
`xtc-io-wrap`) are supported, support for the [XTC](XTC){.twikiLink}
repository is not implemented as this time because of portability
concerns. Any `xtc-transform` or `xtc-call` invocations report a
warning, and simply invoke executables on the path. For the interest of
portability, applications that make use of these strategies should use
library strategies instead, as discussed in the following section.

### []{#Using_External_Applications_and}[]{#Using_External_Applications_and_} Using External Applications and Libraries

A trend in Stratego programs has been to use the standard libraries in
favor of the (slower, less portable) [XTC](XTC){.twikiLink} interface.
For example, the `parse-file` strategy from `libstratego-sglr` can be
used to parse files. Since [XTC](XTC){.twikiLink} depends on native
executables and a centralized repository, it is not portable and not
supported on the Java platform. As an alternative, library calls should
be used instead, which is generally the preferred method for invoking
external components.

Libraries in the Java environment have a package name. For example, the
Stratego standard library resides in the `org.strategoxt.stratego_lib`
package. To maintain compatibility, these package names are not used
within the Stratego language, but only at compile time and when the
components are linked. For example, to link a program to the standard
library the option `-la org.strategoxt.stratego_lib` can be specified.
The standard libraries also have aliases that correspond to the
[XTC](XTC){.twikiLink} names commonly used with strc; `-la stratego-lib`
is also accepted. To define a package name for your own library, use the
`-p` and `--library` options. For example:

      java -jar strategoxt.jar -i foo.str --library --clean -p org.foo -o bin/org/foo/Main.java

Note that each Stratego component may specify a different main class
(`Main` in this case), but that they must still reside in different
packages as to avoid overlap between strategy classes.

### []{#Java_Integration} Java Integration

A typical use case of compiling Stratego applications to Java is to
integrate them into an existing Java application or environment.
Interaction with the other Java components is possible in a number of
ways:

-   Java components can directly call Stratego strategies, by calling
    the `Main.init()` method in the appropriate package and invoking a
    Strategy using `some_strategy_0_0.instance.invoke()`. If the `exit`
    strategy is called at any point, a `StrategoExit` exception will be
    thrown; a call to `fatal-err` will throw a `StrategoErrorExit`
    exception.

<!-- -->

-   Normal Java components can be used to implement or override Stratego
    strategies, allowing for tighter coupling between Stratego and a
    Java application. See for example
    <https://svn.strategoxt.org/repos/StrategoXT/>
    strc-java/trunk/java/runtime/org/strategoxt/lang/compat/libstratego\_rtg\_compat
    where two strategies (originally implemented natively in C) are
    implemented in Java. Every strategy has an `instance` field that
    allows it to be dynamically redefined.

<!-- -->

-   Instead of just plain ATerms, Stratego can operate on any Java
    object tree or graph that implements the `IStrategoTerm` and
    associated interfaces. This way, it can operate on arbitrary object
    structures, or deeply integrate into a Java-based compiler front-end
    or editor. See also [Fusing a transformation language with an open
    compiler](http://www.ii.uib.no/~karltk/phd/papers/ldta07-pomadapter.pdf)
    by Kalleberg and Visser, and [Domain-Specific Languages for
    Composable Editor
    Plugins](http://www.lclnet.nl/publications/composable-editor-plugins)
    by Kats, Kalleberg, and Visser.

<!-- -->

-   []{#hybrid}Compiled Stratego components can be dynamically loaded
    from JAR files and may be combined with interpreted components using
    the `HybridInterpreter` class. To interpret a Stratego component,
    pre-compile it to a `.ctree` file using [STRJ](STRJ){.twikiLink} and
    the `-F --library` options.

[]{#Download} Download
----------------------

Native builds of the Jompiler (\"strc-java\") are available from Hydra:

-   <http://hydra.nixos.org/view/strategoxt-java/strc-java-trunk>

the pure Java version (included in the above distribution) can also be
downloaded from:

-   <http://hydra.nixos.org/job/strategoxt-java/strc-java-trunk/build/latest/download-by-type/file/jar>

The Java version of [STRJ](STRJ){.twikiLink} is also integrated in the
[Spoofax plugin](../Spoofax/WebHome){.twikiLink} that allows you to
develop languages and Eclipse plugins with Stratego.

[]{#Project_Information} Project Information
--------------------------------------------

### []{#Source_Code} Source Code

Source code is available directly from SVN at

-   <https://svn.strategoxt.org/repos/StrategoXT/strategoxt-java-backend/trunk>

or can be downloaded as a package at
[hydra.nixos.org](http://hydra.nixos.org).

### []{#Contributors} Contributors

Contributors

-   Lennart Kats (main STRJ development and maintainer; Stratego/J
    compatibility components)
-   Karl Trygve Kalleberg (main Stratego/J and
    [JSGLR](JSGLR){.twikiLink} development; original s2j prototype)
-   Valentin David (parts of the Stratego/J runtime)

The development of STRJ would not have been possible without the efforts
of Eelco Visser and his team in developing the STRC reference stratego
compiler. Martin Bravenboer\'s [Java-front](JavaFront){.twikiLink}
library and syntax definition have also been indispensable for the
development STRJ.

### []{#License} License

STRJ is licensed under the GNU Lesser General Public License
([LGPL](LGPL){.twikiLink}).

### []{#Contact_and_Mailing_List} Contact and Mailing List

Please send questions to the [users\@strategoxt.org mailing
list](https://mailman.st.ewi.tudelft.nl/listinfo/users) or [contact
Lennart Kats](http://www.lclnet.nl/contact/) directly. Also, we can
usually be found online on IRC at [\#stratego on
freenode.net](irc://irc.freenode.net/stratego) ([web
version](http://java.freenode.net/index.php?channel=stratego)). Feel
free to drop by!

[]{#Related_Software} Related Software
--------------------------------------

[]{#Spoofax_IMP} The [Spoofax/IMP](Spoofax-IMP){.twikiLink} IDE
development environment incorporates the STRJ compiler. By default, it
interprets Stratego definitions, using the [hybrid
interpreter](STRJ#hybrid){.twikiAnchorLink}, but by changing the
`build.xml` and `<myproject>-Analysis.esv` files, it can also compile
them.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
