::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
::: {style="overflow:auto; height:1px; width:1px;"}
[incest porn](http://sexpace.net/)\
:::

[Home](WebHome){.twikiLink}

**Lecture**

-   [Material](CourseMaterial){.twikiLink}

**Lab**

-   [Exercises](CourseExercises){.twikiLink}
-   [Software](CourseSoftware){.twikiLink}

**Documentation**

-   [Stratego/XT
    Manual](http://nix.cs.uu.nl/dist/stratego/strategoxt-manual-unstable-latest/manual/)
-   [Stratego
    Library](http://nix.cs.uu.nl/dist/stratego/stratego-lib-docs-stable-latest/docs/)
-   [Java
    Syntax](http://nix.cs.uu.nl/dist/stratego/java-front-docs-stable-latest/docs/html/v1.5/languages/java-15/Main.sdf.html)
-   [Dryad
    Library](http://nix.cs.uu.nl/dist/stratego/dryad-docs-stable-latest/docs/)

**Contact**

-   [Mailing List](https://mail.cs.uu.nl/mailman/listinfo/stratego)
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Eelco Visser](http://swerl.tudelft.nl/bin/view/EelcoVisser/WebHome)
-   [Martin Bravenboer](http://martin.bravenboer.name)

**Links**

-   [Stratego/XT](http://www.stratego-language.org)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/IPA06/CourseExercises?t=1536827639)
-   [Rename
    Page](http://www.program-transformation.org/rename/IPA06/CourseExercises)
-   [Attach
    File](http://www.program-transformation.org/attach/IPA06/CourseExercises)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/IPA06/CourseExercises?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/IPA06/CourseExercises?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/IPA06/CourseExercises?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/IPA06/CourseExercises?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/IPA06/CourseExercises?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/IPA06/CourseExercises?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/IPA06/CourseExercises?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/IPA06/CourseExercises)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/IPA06/CourseExercises?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/IPA06/CourseExercises?template=oopsmore&param1=1.3&param2=1.3)
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
Course Exercises {#course-exercises .twikiTopicTitle}
================

::: {.twikiWebTitle}
Strategic Programming - IPA Basic Course on Software Technology 2006
:::

::: {.twikiToc}
-   [Getting Started](CourseExercises#Getting_Started)
-   [Java Tools](CourseExercises#Java_Tools)
-   [Rewriting strategies](CourseExercises#Rewriting_strategies)
    -   [Introduce Braces for Control-flow
        Statements](CourseExercises#Introduce_Braces_for_Control_flo)
    -   [Warn for Return Statements in Finally
        Clause](CourseExercises#Warn_for_Return_Statements_in_Fi)
-   [Type-unifying strategies](CourseExercises#Type_unifying_strategies)
    -   [Collect Literals](CourseExercises#Collect_Literals)
    -   [Collect Classes from
        Bytecode](CourseExercises#Collect_Classes_from_Bytecode)
-   [Context-sensitive
    transformations](CourseExercises#Context_sensitive_transformation)
:::

[]{#Getting_Started} Getting Started
------------------------------------

To start a proper shell and initialize your path, run the following
commands. (`martin` is on purpose. Don\'t change the username to your
own account).

    $ bash
    $ source /home/martin/strategoxt/env.sh

Don\'t forget to run these commands again if you open a new shell.

Download the file
[ipa06-templates.tar.gz](http://www.cs.uu.nl/people/martin/ipa06/ipa06-templates.tar.gz)
to your home directory, create a working directory for yourself, and
unpack the file:

    $ mkdir <working-dir>
    $ cd <working-dir>
    $ tar zxvf ~/ipa06-templates.tar.gz

The tarball contains a very small Stratego program to test the
Stratego/XT installation. If the following commands do not succeed, then
please scream for help.

    $ cd welcome
    $ strc -i welcome.str -la stratego-lib
    $ ./welcome
    Great, Stratego/XT works!
    $ cd ..

For experimenting with the Stratego language the Stratego Shell can be
useful. A small session that you can try to see if it works.:

    $ stratego-shell
    stratego> import libstratego-lib
    stratego> ![1, 2, 3]
    [1,2,3]
    stratego> fetch(?x)
    [1,2,3]
    stratego> :binding x
    x is bound to 1
    stratego> :quit
    $ 

[]{#Java_Tools} Java Tools
--------------------------

(work in directory `tools`)

In these exercises we will use the Java support packages of Stratego/XT.
The tool `parse-java` is used to parse Java programs to an abstract
syntax tree represented as an ATerm.

    $ echo "class Foo {}" | parse-java | pp-aterm
    CompilationUnit(
      None()
    , []
    , [ ClassDec(
          ClassDecHead([], Id("Foo"), None(), None(), None())
        , ClassBody([])
        )
      ]
    )

For parsing simple expressions, you don\'t have to create an entire
class:

    $ echo "1+2" | parse-java -s Expr | pp-aterm
    Plus(Lit(Deci("1")), Lit(Deci("2"))

You can also put the class in a file, which is useful if you are going
to try bigger examples. For files, use `parse-java -i Foo.java`.

Java-front also features a pretty-printer for Java. You can apply this
pretty-printer in a pipeline with the parser:

    $ parse-java -i HelloWorld.java | pp-java

Compile a simple Java source file to a .class file and decompile it
using the tool `class2aterm`:

    $ javac HelloWorld.java
    $ class2aterm -i HelloWorld.class | pp-aterm

Take a brief look at the structure of this aterm. This invocation does
not disassemble the code. For this, you have to pass `-c` as an argument
to class2aterm:

    $ class2aterm -i HelloWorld.class -c | pp-aterm

As you can see, the output is quite big. If you want to scroll through
the output, then you can add `less` to the pipeline. You can exit `less`
and return to the command-line using `q`.

    $ class2aterm -i HelloWorld.class -c | pp-aterm | less

[]{#Rewriting_strategies} Rewriting strategies
----------------------------------------------

### []{#Introduce_Braces_for_Control_flo} Introduce Braces for Control-flow Statements

(work in directory `introduce-braces`)

Implement a set of conditional rewrite rules that introduces blocks in
the branches of control-flow statements, but only if the blocks are
missing. Cover a few different control-flow statements. Use the template
`introduce-braces.str`.

Compile and apply:

    $ cd introduce-braces
    $ ./compile.sh
    $ parse-java -i Sample1.java | ./introduce-braces | pp-java
    public class Sample1
    {
      int foo()
      {
        if(true)
        {
          return 1;
        }
        else
        {
          return 2;
        }
      }
    }

    $ parse-java -i Sample2.java | ./introduce-braces | pp-java
    public class Sample2
    {
      void foo()
      {
        while(true)
        {
          doWhatever();
        }
        oops();
      }
    }

### []{#Warn_for_Return_Statements_in_Fi} Warn for Return Statements in Finally Clause

(work in directory `return-finally`)

Note: If the previous exercises took you more than an hour, then you
might want to skip to the next exercises on type-unifying strategies.

A return statement in a `finally` clause should be avoided, because this
return statement can completely change the original result of the
method: a returned value or a thrown exception in the `try` part. This
is not the purpose of a finally clause, therefore compilers often warn
about this:

    class ReturnFinally
    {
      boolean error;

      int g()
      {
        if(error)
          throw new IllegalStateException();
        else
          return 4;
      }

      int f()
      {
        try
        {
          return g();
        }
        finally
        {
          return 5;
        }
      }
    }

    $ javac ReturnFinally.java -Xlint
    ReturnFinally.java:22: warning: [finally] finally clause cannot complete normally
        }
        ^
    1 warning

For this exercise, write an transformation that inserts a comment before
return statements in a finally clause. This is not entirely trivial.
Thanks to local and anonymous class declarations, not every return
statement in a finally clause is incorrect. So, you need to handle these
constructs in a special way.

It is useful to think about this transformation as format checking. If a
Java source file does not use return statements in finally clauses, then
the program can be described as being written in two different
languages. First, in a finally clause the used language is a subset of
the complete Java language: no return statements are allowed. Second,
outside finally clauses, the full Java language is used. However, for
local and anonymous class declarations in finally clauses the full
language is supported as well.

A useful pattern for the implementation of these problems is to have two
strategies, one for the complete language and one for the subset. In
both strategies, specific cases are handled and maybe the context is
switched to the other strategy. By default, they just traverse.

You need about 10 lines of code for this, so if your strategy is much
longer, then you\'re doing something wrong ;)

Compile and apply:

    $ cd return-finally
    $ ./compile.sh
    $ parse-java -i ReturnFinally.java | ./return-finally | pp-java
    class ReturnFinally
    {
      boolean error;

      int g()
      {
        if(error)
          throw new IllegalStateException();
        else
          return 4;
      }

      int f()
      {
        try
        {
          return g();
        }
        finally
        {
          // WARNING: return in finally
          return 5;
        }
      }
    }

`ReturnFinallyTricky.java` is an example with a local class declaration.

[]{#Type_unifying_strategies} Type-unifying strategies
------------------------------------------------------

### []{#Collect_Literals} Collect Literals

(work in directory `collect-literals`)

Note: If you have less than 45 minutes left, then it is a good idea to
skip this exercise and only do the bytecode collect exercise.

Collect all literals (booleans, string, integers, etc) used in a Java
source file and return them as a list. Use the template
`collect-literals.str`.

Compile and apply:

    $ cd collect-literals
    $ ./compile.sh
    $ parse-java -i SimpleProxyServer.java | ./collect-literals | pp-aterm
    [ Deci("3")
    , String([Chars("Wrong number of arguments.")])
    , Deci("2")
    , String([Chars("Starting proxy for ")])
    , String([Chars(" on port ")])
    , String([Chars("Usage: java SimpleProxyServer ")])
    , String([Chars("<host> <remoteport> <localport>")])
    , Deci("1024")
    , Deci("4096")
    , Bool(True())
    , String([Chars("Proxy server cannot connect to ")])
    , String([Chars(":")])
    , String([Chars(":"), NamedEscape(110)])
    , Deci("1")
    , Deci("0")
    , Null()
    ]

### []{#Collect_Classes_from_Bytecode} Collect Classes from Bytecode

(work in directory `collect-classes`)

Given a Java .class file, return the classes that are referred to using
constructor calls (`NEW`), field accesses or method invocations. Use the
template `collect-classes.str`.

Compile and apply:

    $ cd collect-classes
    $ ./compile.sh
    $ javac YesNoDialog.java 

    $ class2aterm -c -i YesNoDialog.class | ./collect-classes | pp-aterm
    [ "java.awt.Dialog"
    , "java.awt.BorderLayout"
    , "MultiLineLabel"
    , "YesNoDialog$1"
    , "java.awt.FlowLayout"
    , "java.awt.Button"
    , "java.awt.Panel"
    , "java.awt.AWTEventMulticaster"
    , "java.awt.Frame"
    , "YesNoDialog$2"
    , "YesNoDialog"
    ]

    $ class2aterm -c -i MultiLineLabel.class | ./collect-classes | pp-aterm
    [ "java.awt.Canvas"
    , "java.awt.Dimension"
    , "java.awt.Graphics"
    , "java.util.StringTokenizer"
    , "java.awt.Toolkit"
    , "java.awt.FontMetrics"
    , "MultiLineLabel"
    ]

Note that is very easy to collect other information, for example
constructors invoked from this class, methods that are invoked, fields
that are accessed, etc.

[]{#Context_sensitive_transformation} Context-sensitive transformations
-----------------------------------------------------------------------

(work in the directory `trace-instrument`)

Implement a simple trace instrumentation tool that prints a message when
a program enters and exits a method. Include the fully qualified name of
the declaring class of the method in the message, wich you can propagate
during the traversal using a scoped dynamic rule. Support member
classes.

Compile and apply:

    $ cd trace-instrument
    $ ./compile.sh

    $ parse-java -i Factorial2.java | ./trace-instrument  | pp-java -o Factorial.java
    $ cat Factorial.java
    public class Factorial
    {
      public static long factorial(long x)
      {
        try
        {
          System.out.println("Enter Factorial.factorial");
          if(x == 1)
            return 1;
          else
            return x * factorial(x - 1);
        }
        finally
        {
          System.out.println("Exit Factorial.factorial");
        }
      }

      public static void main(String[] ps)
      {
        try
        {
          System.out.println("Enter Factorial.main");
          System.out.println("Factorial of 4 is " + factorial(4));
        }
        finally
        {
          System.out.println("Exit Factorial.main");
        }
      }
    }

    $ javac Factorial.java
    $ java Factorial
    Enter Factorial.main
    Enter Factorial.factorial
    Enter Factorial.factorial
    Enter Factorial.factorial
    Enter Factorial.factorial
    Exit Factorial.factorial
    Exit Factorial.factorial
    Exit Factorial.factorial
    Exit Factorial.factorial
    Factorial of 4 is 24
    Exit Factorial.main

`fact/Tricky2.java` is a bit more difficult:

    $ parse-java -i fact/Tricky2.java | ./trace-instrument | pp-java -o fact/Tricky.java
    $ javac fact/Tricky.java
    $ java fact.Tricky
    Enter fact.Tricky.main
    Enter fact.Tricky.Factorial.apply
    Enter fact.Tricky.Factorial.apply
    Enter fact.Tricky.Factorial.apply
    Enter fact.Tricky.Factorial.apply
    Exit fact.Tricky.Factorial.apply
    Exit fact.Tricky.Factorial.apply
    Exit fact.Tricky.Factorial.apply
    Exit fact.Tricky.Factorial.apply
    Factorial of 4 is 24
    Enter fact.Tricky.Multiply.apply
    Exit fact.Tricky.Multiply.apply
    4*4 is 16
    Exit fact.Tricky.main

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
