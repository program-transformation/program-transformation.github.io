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
    Page](http://www.program-transformation.org/edit/Stratego/TheDryadCompiler?t=1536825465)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/TheDryadCompiler)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/TheDryadCompiler)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/TheDryadCompiler?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/TheDryadCompiler?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    18](http://www.program-transformation.org/view/Stratego/TheDryadCompiler?rev=1.18)
    [(diff 17)](http://www.program-transformation.org/rdiff/Stratego/TheDryadCompiler?rev1=1.18&rev2=1.17)
-   [Rev
    17](http://www.program-transformation.org/view/Stratego/TheDryadCompiler?rev=1.17)
    [(diff 16)](http://www.program-transformation.org/rdiff/Stratego/TheDryadCompiler?rev1=1.17&rev2=1.16)
-   [Rev
    16](http://www.program-transformation.org/view/Stratego/TheDryadCompiler?rev=1.16)
    [(diff 15)](http://www.program-transformation.org/rdiff/Stratego/TheDryadCompiler?rev1=1.16&rev2=1.15)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/TheDryadCompiler)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/TheDryadCompiler?template=oopsmore&param1=1.18&param2=1.18)
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
    \...](http://www.program-transformation.org/oops/Stratego/TheDryadCompiler?template=oopsmore&param1=1.18&param2=1.18)
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
The Dryad Compiler {#the-dryad-compiler .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The Dryad Compiler is an open compiler for the Java platform, based on
[The Dryad](TheDryad){.twikiLink}.

::: {.twikiToc}
-   [Overview of Features](TheDryadCompiler#Overview_of_Features)
    -   [The Java/bytecode
        Language](TheDryadCompiler#The_Java_bytecode_Language)
    -   [Source Tracing](TheDryadCompiler#Source_Tracing)
    -   [Type Checker and
        Verifier](TheDryadCompiler#Type_Checker_and_Verifier)
    -   [Extensions](TheDryadCompiler#Extensions)
-   [Example applications](TheDryadCompiler#Example_applications)
-   [Project Info](TheDryadCompiler#Project_Info)
    -   [Publications](TheDryadCompiler#Publications)
    -   [Contact and Mailing
        List](TheDryadCompiler#Contact_and_Mailing_List)
    -   [Downloads](TheDryadCompiler#Downloads)
    -   [Development](TheDryadCompiler#Development)
    -   [License](TheDryadCompiler#License)
-   [See also](TheDryadCompiler#See_also)
:::

[]{#Overview_of_Features} Overview of Features
----------------------------------------------

The Dryad Compiler is a compiler for a language formed by the *mixture
of Java and bytecode*. This means that it can be used to compile regular
Java programs, as well as programs that may already be partially or
completely compiled to bytecode. The compiler uses transformation rules
that *normalize* the input language to pure bytecode, i.e., the core
language. This makes it well-suited for composition mechanisms, such as
traits or aspects, as well as statement-level and expression-level
language extensions. These can operate by transformation to Java source
code or bytecode as required, and may include fragments of previously
compiled code.

The Dryad Compiler makes use of [The Dryad](TheDryad){.twikiLink}, which
provides semantic analyis for the Java language and an interface for
reading and writing Java class files.

### []{#The_Java_bytecode_Language} The Java/bytecode Language

The mixed Java/bytecode language is formed by extension of the
[Java-front](JavaFront){.twikiLink} syntax definition for the Java
language with an assembly language for bytecode. Bytecode fragments and
Java fragments can be used interchangeably using the backtick operator
(\`), and allow direct interoperability through local variables,
expression values, and fields. Fragments of the two constituent
languages can be nested up to arbitrary depth.

An example program:

    class Calculator {
      public static void main(String[] args) {
        // inline "goto" instruction for unstructured control flow in generated code
        `goto label; 

        System.out.println("Hello, Java world");

        label:
          // bytecode instruction in an expresion
          System.out.println(`ldc "Hello Java+bytecode world!");
      }
    }

The complete syntax definition can be found online in the [Stratego/XT
repository](https://svn.cs.uu.nl:12443/repos/StrategoXT/dryad-compiler/trunk/syntax).

### []{#Source_Tracing} Source Tracing

The parser maintains position information when parsing. Throughout the
normalization process that transforms Java/bytecode to the core bytecode
language, this origin information is maintained and used for errors and
run-time exception/debugging information.

### []{#Type_Checker_and_Verifier} Type Checker and Verifier

The Dryad Compiler performs full type checking and verification of the
mixed language. This is implemented as a modular extension of the Dryad
type checker with a Stratego-based bytecode verifier. In the traversal
of the typechecker, the two are used as required and share their
environments.

### []{#Extensions} Extensions

A number of language extensions for Java have been implemented based on
the Dryad Compiler, each compiling to the mixed Java/bytecode language.
For instance, we have implemented an extension with separately compiled
*traits*, an extension of Java for modular reuse of code, where the
Dryad Compiler is used to combine code of compiled traits and source
code classes. Other extensions include assimilation of *yield
continuations* (or \"iterator generators) and new operators into Java
code, that compile to a mixture of bytecode instructions and Java code.

Extensions of the Dryad Compiler can make use of *source tracing* for
accurate error reporting.

*Unit tests* for extension-generated code can be performed by pattern
matching on the generated Java/bytecode output, or by direct compilation
and evaluation of the fragments in the Java Virtual Machine.

[]{#Example_applications} Example applications
----------------------------------------------

A number of small example Stratego programs that use the Dryad Compiler
are available from Subversion.

-   <https://svn.strategoxt.org/repos/StrategoXT/dryad-compiler/trunk/samples>

[]{#Project_Info} Project Info
------------------------------

### []{#Publications} Publications

*Mixing Source and Bytecode. A Case for Compilation by Normalization*.
Lennart C. L. Kats, Martin Bravenboer, and Eelco Visser. The 23rd ACM
SIGPLAN Conference on Object-Oriented Programming, Systems, Languages,
and Applications ([OOPSLA 2008](http://www.oopsla.org/oopsla2008/)).ACM
SIGPLAN Notices 43(10), pages 91---108. Nashville, Tenessee, USA in
October 2008.
\[[pdf](http://www.lclnet.nl/publications/TUD-SERG-2008-030.pdf)\]
\[[bib](http://www.lclnet.nl/publications/KBV08.bib)\]
\[[doi](http://dx.doi.org/10.1007/978-3-540-69927-9_13)\]

*Supporting Language Extension and Separate Compilation by Mixing Java
and Bytecode*. Lennart C. L. Kats. Master\'s thesis INF/SCR-07-02,
Institute of Information and Computing Sciences, Utrecht University,
2007. August 31, 2007.
\[[pdf](http://www.lclnet.nl/publications/kats-mastersthesis.pdf)\]
\[[bib](http://www.lclnet.nl/publications/kats-mastersthesis.bib)\]

### []{#Contact_and_Mailing_List} Contact and Mailing List

Please send questions to the [stratego\@cs.uu.nl mailing
list](https://mail.cs.uu.nl/mailman/listinfo/stratego). Also, the Dryad
and Dryad Compiler developers are usually available on IRC at
[\#stratego on freenode.net](irc://irc.freenode.net/stratego). Feel free
to drop by!

### []{#Downloads} Downloads

Distributions are build continuously:

-   <http://releases.strategoxt.org/dryad-compiler/unstable>

The sources of the Dryad Compiler are available from Subversion.

-   <https://svn.strategoxt.org/repos/StrategoXT/dryad-compiler/trunk>

### []{#Development} Development

Contributors

-   [Lennart Kats](http://www.lennartkats.net/) (main development of the
    Dryad Compiler)
-   [Martin Bravenboer](http://martin.bravenboer.name/) ([the
    Dryad](TheDryad){.twikiLink}; feedback and suggestions)

### []{#License} License

The Dryad Compiler is [LGPL](LGPL){.twikiLink} (GNU Lesser General
Public License) software. This means that you can use the Dryad Compiler
library (and tools) without being required to distribute your software
under the GPL.

[]{#See_also} See also
----------------------

-   [The Dryad](TheDryad){.twikiLink}
-   [Java Front](JavaFront){.twikiLink}

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
