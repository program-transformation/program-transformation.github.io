::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

[![](../pub/rss.gif "RSS 1.0 feed")](WebRss@skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Transform/JavaAbstractSyntax?t=1536826502)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/JavaAbstractSyntax)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/JavaAbstractSyntax)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/JavaAbstractSyntax?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/JavaAbstractSyntax?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Transform/JavaAbstractSyntax?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/JavaAbstractSyntax?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Transform/JavaAbstractSyntax?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/JavaAbstractSyntax?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/JavaAbstractSyntax?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/JavaAbstractSyntax?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/JavaAbstractSyntax)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/JavaAbstractSyntax?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Transform/JavaAbstractSyntax?template=oopsmore&param1=1.7&param2=1.7)
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
Java Abstract Syntax {#java-abstract-syntax .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Program transformation systems for Java programs (that is, Java is the
object language) usually operate on an abstract syntax representation of
the Java source code. Java has no standardized or de facto standard for
its abstract syntax.

[]{#Eclipse_JDT_Core_3_x} Eclipse JDT Core 3.x
----------------------------------------------

The [JDT Core](http://www.eclipse.org/jdt/index.html) component of
Eclipse provides a \'Java Document Model\' in the package
`org.eclipse.jdt.core.dom`. This [API](API){.twikiLink} can be used for
manipulating a structured Java source document.

-   AST can be serialized. However, this is an unformatted String
    representation which is not guaranteed to be correct. The real
    formatter can only be applied to a String and the pretty-printer of
    the AST can only be applied if the original Java source has also
    been parsed by the Eclipse JDT Core parser
-   The [API](API){.twikiLink} looks attractive and feature-rich, but
    many of these features only work inside Eclipse. For example,
    resolving bindings outside of Eclipse is nearly impossible.

<!-- -->

-   Basic AST implementation is not required to be executed in an
    Eclipse plugin.
-   Classes are written by hand and contain useful accessor methods.
-   Representation is \'type-safe\': it is not based on generic
    superclasses for storing nodes.

[]{#Eclipse_JDT_Core_before_3_0_Mile} Eclipse JDT Core before 3.0 Milestone 8
-----------------------------------------------------------------------------

The [JDT Core](http://www.eclipse.org/jdt/index.html) component of
Eclipse provides a \'Java Document Model\' in the package
`org.eclipse.jdt.core.dom`. This [API](API){.twikiLink} can be used for
manipulating a structured Java source document.

-   An application of this AST must itself be an Eclipse plugin.It
    cannot be used from ordinary Java programs since an instance of the
    Eclipse Runtime is required. It is not dependent on the UI however.
-   No proper pretty printing. `toString` methods can be used to produce
    Java concrete syntax, but these methods are intended for debugging
    only.

[]{#OpenJava} OpenJava
----------------------

More on this soon \...

[]{#JavaCC_JRefactory} JavaCC/JRefactory
----------------------------------------

The [JRefactory](http://jrefactory.sourceforge.net/) refactoring tool
for Java uses an abstract syntax tree generated by
[JavaCC](JavaCC){.twikiLink}/JJTree. JRefactory contains a configurable
pretty printer for this abstract syntax tree. Mike Atkinson has taken
over the development from Chris Seguin and is working on the extensions
of the j2sdk 1.5.

-   AST is not really abstract. The presence of literals makes it feel
    more like a parse tree/CST.
-   AST is not type safe. Generic superclasses are used to store
    \'nodes\' and \'specials\'
-   AST feels very generated. The number of hand-written accessor
    methods is limited

<!-- -->

-   Configurable pretty printer

[]{#SableCC} SableCC
--------------------

[SableCC](SableCC){.twikiLink} is a compiler compiler producing Java. It
generates strictly typed abstract syntax tree classes for the object
language. There is a Java 1.4 grammar for
[SableCC](SableCC){.twikiLink}, which therefore defines an abstract
syntax for Java. As far as I know that is no pretty printer for this
AST.

-   No pretty printer available for the abstract syntax tree
-   No facility to add user defined to the generated classes without
    making regeneration impossible

<!-- -->

-   Choose between the CST and AST representation in
    [SableCC](SableCC){.twikiLink} 3 (not yet implemented in the Java
    grammar although).
-   Generates tree walkers.
-   Representation is \'type-safe\': it is not based on generic
    superclasses for storing nodes.

[]{#Stratego_XT_and_java_front} Stratego/XT and java-front
----------------------------------------------------------

Stratego/XT\'s [java-front](../Stratego/JavaFront){.twikiLink} defines
the concrete syntax for Java in [SDF](../Sdf/WebHome){.twikiLink} and
generates abstract syntax tree definitions from this concrete syntax
definition. [java-front](../Stratego/JavaFront){.twikiLink} contains a
pretty-printer implemented in Stratego for this Java abstract syntax.

-   ASTs are exchanged in the [ATerm
    format](../Tools/ATermFormat){.twikiLink}, which is limited to ASCII
    characters
-   Type safety is not enforced by the [ATerm
    format](../Tools/ATermFormat){.twikiLink}. The meta language or the
    programmer is responsible for this.
-   Tools are not implemented in Java. Requires a POSIX compatible
    operating system

<!-- -->

-   Lexical constructs like string and characters literals are
    structured
-   Representation is abstract: syntactical details like literals are
    not present
-   High quality pretty-printer
-   Parser and pretty-printer support comment preservation
-   Full support for 1.5
-   Option to parse Java to an AST concisely represented in an
    [XML](XML){.twikiLink} document

[]{#Java_Compiler_API} Java Compiler API
----------------------------------------

A future goal of [JSR 199: Java Compiler
API](http://www.jcp.org/en/jsr/detail?id=199) is to standardize the
structured representation of Java source code in an abstract syntax
tree.

-   It doesn\'t exist.

### []{#Maintainer} Maintainer

This page is maintained by [Martin
Bravenboer](../Main/MartinBravenboer){.twikiLink}. This is Wiki, so you
can contribute if you want to provide additional information. Of course
you can also just send me your comments by e-mail.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
