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
    Page](http://www.program-transformation.org/edit/Transform/RefactoringProject?t=1536826546)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/RefactoringProject)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/RefactoringProject)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/RefactoringProject?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/RefactoringProject?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/RefactoringProject?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/RefactoringProject?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/RefactoringProject?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/RefactoringProject)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/RefactoringProject?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/RefactoringProject?template=oopsmore&param1=1.2&param2=1.2)
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
Refactoring Project {#refactoring-project .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Contact**

-   Arne de Bruijn <arbruijn@students.cs.uu.nl>
-   Martin Bravenboer <mbravenb@students.cs.uu.nl>

**Topics**

Progress - Testing - Programs - Documents - Links - Ideas

**Progress**

Done:

-   Examination of the refactoring tool by Chris Seguin
-   Overview of the AST & the Java Grammer file for
    [JavaCC](JavaCC){.twikiLink} and JJTree
-   Tree view of the AST of a method from the UI
-   Source view of a method
-   Select statements view of a method (not finished yet)

To do:

-   Check the role and scope of variables
-   Create the parameter list of the method
-   Check if the method should return a value and the type of this
    value.
-   Create a new method
-   Remove the statements from the parent method

**Testing**

Maybe we could accept the example refactoring in the refactoring book of
Martin Fowler as a test case. We could devide it into several test
cases.

**Programs**

-   Source of the tool + extentions we\'ve done so far:
    <http://www.students.cs.uu.nl/people/arbruijn/sg/refactoring/jrefsg03.zip>

<!-- -->

-   First Java Parsing excercise with extra java code in the parser and
    ast:
    <http://www.students.cs.uu.nl/people/mbravenb/sg/refactoring/ParseSimpleJava.zip>
    Start with: parse.simpejava.JavaParser \<JAVA\_SOURCE\_FILE\>. The
    test only supports package, imports and class declarations. Extract
    the zip file into a directory called parse.

<!-- -->

-   *Java 2 Parser* genenerated by the grammar file and building the
    mentioned AST:
    <http://www.students.cs.uu.nl/people/mbravenb/sg/refactoring/JavaParser.zip>

**Documents**

-   To do list for extract method:
    <http://www.students.cs.uu.nl/people/mbravenb/sg/refactoring/extractMethod.doc>

<!-- -->

-   Complete *overview of the Abstract Syntax Tree* of the Java 2
    Language(Grammar file by David Williams) in quite a large Powerpoint
    document (Zoom to 100% to view the tree):
    <http://www.students.cs.uu.nl/people/arbruijn/sg/refactoring/Java2ParseTree.ppt>

<!-- -->

-   *Java 2 Grammar File* for Jjtree:
    <http://www.students.cs.uu.nl/people/arbruijn/sg/refactoring/Java1.2.jjt>

<!-- -->

-   Some comments and analysis of the Refactoring Tool by Chris Seguin
    (in dutch):
    <http://www.students.cs.uu.nl/people/mbravenb/sg/refactoring/RefactoringTool.doc>

<!-- -->

-   Provisional version of report (in dutch):
    <http://www.students.cs.uu.nl/people/arbruijn/sg/refactoring/verslag.doc>

**Links**

-   Javacc: the Parser Generator for Java. Jjtree: the Abstract Syntax
    Tree builder preprocessor for Javacc.
    <http://www.metamata.com/javacc/>

<!-- -->

-   The Refactoring book of Martin Fowler: <http://www.refactoring.com>

<!-- -->

-   *Refactoring Object-Oriented Frameworks*, Thesis by William D.
    Opdyke. More academical view on refactoring and one of the first
    papers on refactoring:
    <ftp://st.cs.uiuc.edu/pub/papers/refactoring/opdyke-thesis.ps.Z>
    Many information on safety and preserving behaviour.

**Ideas**

-   Make *method extraction* possible. Maybe we should extend the
    grammar for this.
-   You should be able to view the *code of a method* from the uml view.
    The pretty printer should be used for this. This feature can be used
    for code selection in the extract method refactoring.
-   Variable information (currently not supported): references should
    know what the type of the variable is and where it is defined etc.
-   Editing information: is a variable in a piece of code used for
    reading or also for writing purposes?

Other ideas which could be used to write a new tool:

-   Create a tool which supports *safe refactoring* by warning for any
    possible error which could occure. It should always create correct
    Java code or it should warn if this isn\'t possible.
-   *Refactorings* should be as *small* and reusable as possible to make
    it easy to add refactorings.
-   Make a *very good parse tree* which can be used for many
    refactorings and other program elements:
    -   Checking methods should be included in the parse tree to make
        them reusable for other refactorings.
    -   Methods should know where they are called to make refactorings
        efficient and easy.
    -   Classes should know where they are referenced so they can warn
        that items when classnames or other classitems change.
-   Try to use code of the Refactoring Tool by Chris Seguin when some
    problems are solved there in a nice way.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
