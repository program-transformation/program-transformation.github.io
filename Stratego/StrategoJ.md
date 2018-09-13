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
    Page](http://www.program-transformation.org/edit/Stratego/StrategoJ?t=1536825463)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/StrategoJ)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/StrategoJ)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/StrategoJ?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/StrategoJ?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/StrategoJ?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/StrategoJ)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/StrategoJ?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/StrategoJ?template=oopsmore&param1=1.1&param2=1.1)
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
Stratego J {#stratego-j .twikiTopicTitle}
==========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#Stratego_J_A_Stratego_Core_Forma} Stratego/J: A Stratego Core Format Engine
===============================================================================

Stratego/J is an execution engine for the Stratego language, implemented
in Java. It allows the execution of the full Stratego language on the
Java virtual machine.

It may be easiest to think of Stratego/J as the implementation of an
abstract Stratego machine. The Stratego compiler can, using the -F
option, output a compiled Stratego program in a high-level
Stratego-specific format which Stratego/J can execute. It is currently
not possible to interactively evaluate Stratego source code on
Stratego/J \-- for that, use Stratego Shell.

For more details, see <http://www.spoofax.org/strategoj.html>

[]{#Embedding_the_Stratego_runtime} Embedding the Stratego runtime
------------------------------------------------------------------

Adding the Stratego interpreter to your Java project is pretty
straightforward.

First, add the Stratego/J runtime jar files in your classpath.

Second, compile your Stratego program using `strc -F` to obtain a
program in the Stratego Core Format.

Third, initialize and call the interpreter along these lines:

     
    String strategyName = ...
    IStrategoTerm initialTerm = ...
    InputStream program = ...
    Interpreter interp = new Interpreter();
    try {
      interp.load(program);
      interp.setCurrent(initialTerm);
      boolean success = interp.invoke(strategyName);
    } catch(Exception e) {
      e.printStackTrace();
    }

The `initialTerm` is the current term to be used when the interpreter
starts executing. Default is `()`. The `program` is an `InputStream` to
the `.ctree` file of your Stratego program. The `strategyName` is in
Core Format form, e.g. `main_0_0`.

The interpreter will return `false` if the invoked strategy fails.
Exceptions are reserved for exceptional circumstances and internal
errors; in practice, they should only arise when calling `prim()`
functions.

### []{#Factories} Factories

The interpreter represents both the program and the data as terms. By
default, this factory is the same, and knows how to read ATerms in
textual form. If you need other ATerm formats, consider invoking the
interpreter with the `WrappedATermFactory`, after you remeber to add
both the ATerm library and the ATerm wrapper library to your classpath:

    new Interpreter(new WrappedATermFactory())

It is possible to have separate factories for the program and the data:

    new Interpreter(new BasicTermFactory(), new WrappedATermFactory())

The first argument is for the program factory, the second for the data.

#### []{#POM_adapters} POM adapters

By using the POM adapter technique, you can rewrite any object graph for
which you have an adapter. All you need is to supplying an instance of
the factory for the adapter.

### []{#Adding_native_functions} Adding native functions

The interpreter supports the notion of operator registries. These are
basically sets of `prim()` strategies that may be added to the
interpreter when you instantiate it, e.g.:

    interp.addOperatorRegistry(ECJLibrary.REGISTRY_NAME, new ECJLibrary());
    interp.addOperatorRegistry(EFILibrary.REGISTRY_NAME, new EFILibrary());

Here, the Eclipse Compiler for Java registry is added, followed by the
Eclipse foreign functions. The first allows Stratego scripts to invoke
methods on some of the objects of the Eclipse Java Compiler. The second
allows scripts to call Eclipse file and UI functions, to open windows
and load resources. (These registries are available as separate jars).

\-- [KarlTrygveKalleberg](../Main/KarlTrygveKalleberg){.twikiLink} - 06
Jun 2008\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
