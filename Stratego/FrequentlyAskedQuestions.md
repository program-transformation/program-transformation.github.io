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
    Page](http://www.program-transformation.org/edit/Stratego/FrequentlyAskedQuestions?t=1536825560)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/FrequentlyAskedQuestions)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/FrequentlyAskedQuestions)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/FrequentlyAskedQuestions?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/FrequentlyAskedQuestions?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    17](http://www.program-transformation.org/view/Stratego/FrequentlyAskedQuestions?rev=1.17)
    [(diff 16)](http://www.program-transformation.org/rdiff/Stratego/FrequentlyAskedQuestions?rev1=1.17&rev2=1.16)
-   [Rev
    16](http://www.program-transformation.org/view/Stratego/FrequentlyAskedQuestions?rev=1.16)
    [(diff 15)](http://www.program-transformation.org/rdiff/Stratego/FrequentlyAskedQuestions?rev1=1.16&rev2=1.15)
-   [Rev
    15](http://www.program-transformation.org/view/Stratego/FrequentlyAskedQuestions?rev=1.15)
    [(diff 14)](http://www.program-transformation.org/rdiff/Stratego/FrequentlyAskedQuestions?rev1=1.15&rev2=1.14)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/FrequentlyAskedQuestions)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/FrequentlyAskedQuestions?template=oopsmore&param1=1.17&param2=1.17)
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
    \...](http://www.program-transformation.org/oops/Stratego/FrequentlyAskedQuestions?template=oopsmore&param1=1.17&param2=1.17)
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
Frequently Asked Questions {#frequently-asked-questions .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Installation](FrequentlyAskedQuestions#Installation)
    -   [Mac OS X](FrequentlyAskedQuestions#Mac_OS_X)
    -   [Microsoft Windows](FrequentlyAskedQuestions#Microsoft_Windows)
-   [Stratego
    interpreter](FrequentlyAskedQuestions#Stratego_interpreter)
-   [Debugging](FrequentlyAskedQuestions#Debugging)
-   [Stratego language](FrequentlyAskedQuestions#Stratego_language)
    -   [Dynamic rules](FrequentlyAskedQuestions#Dynamic_rules)
-   [Stratego Libary](FrequentlyAskedQuestions#Stratego_Libary)
:::

[]{#Installation} Installation
------------------------------

**Q:** I get errors when compiling Stratego programs or when running
compiled Stratego programs.\
**A:** If you\'ve carefully followed the [installation
instructions](InstallationInstructions){.twikiLink} and you are still
having problems, please file a [bug report](ReportingBugs){.twikiLink}.
Make sure to specify your configuration (OS, gcc version, Stratego
version), include the error message and if posisble try to reduce to
problem to a small piece of code.

### []{#Mac_OS_X} Mac OS X

**Q:** Does Stratego/XT support Mac OS X?\
**A:** Yes, Stratego/XT works on Mac OS X. We provide binary
distributions.

### []{#Microsoft_Windows} Microsoft Windows

**Q:** Does Stratego/XT support Microsoft Windows?\
Yes, Stratego/XT works on Microsoft Windows + Cygwin. We provide binary
distributions. Recently, we have started on support for native Microsoft
Windows (i.e. without Cygwin). We currently provide binary archives of
[JavaFront](JavaFront){.twikiLink} and Stratego Libraries for native
Microsoft Windows.

**Q:** How do I compile Stratego/XT on Microsoft Windows using Cygwin?\
**A:** You can follow the normal installation instructions, with a minor
twist. Cygwin prints lots of warnings about \'description fields\' when
compiling the Stratego Libraries. They are harmless, but this can go on
for minutes, so this might confuse you. To disable the warnings, set
`CFLAGS` to `-O2` before configuring Stratego/XT. By setting the CFLAGS,
configure will itself not initialize it to `-O2 -g`, where the `-g`
argument is the problematic one.

**Q:** How do I compile the Stratego Libraries on Microsoft Windows
using MinGW?\
**A:** Install the aterm library, and for the Stratego Libraries use the
configure option \--with-std=C99 and everything should work like a
charm.

[]{#Stratego_interpreter} Stratego interpreter
----------------------------------------------

**Q:** How do I proceed to write Stratego code that\'s both
interpretable and compilable? Is that a goal for the interpreter that
this is possible ?\
**A:** Yes, the compiler and the interpreter work on the same language.
You can consider the list of commands in a script as the main strategy
of a specification. There should be no difference in semantics between
the compiler and the interpreter. Except for the fact that there is a
definition before use regime in the script itself (not in modules
imported in the script). That is, that is defined in the script can only
be used (in a command) after it has been declared.

[]{#Debugging} Debugging
------------------------

**Q:** How do I get more debugging info ? The tools are awfully quiet
unless I chock my code full of `debug` invocations. Can I somehow set up
an \'exception handler\' that shows the traversed stack and line number
(or something similar) when a rewriting fails miserably?

**A:** See [debugging techniques](DebuggingTechniques){.twikiLink}

[]{#Stratego_language} Stratego language
----------------------------------------

**Q:** What is the difference between a strategy and a rule?\
**A:** See [rules versus strategies](RulesVersusStrategies){.twikiLink}

**Q:** In what ways can variables be bound?\
**A:** A variable is only bound during matching. That is, while applying
a pattern match `?t` to the subject term. All constructs that bind
variables, ultimately use this pattern matching construct to bind
variables.

### []{#Dynamic_rules} Dynamic rules

**Q:** I get unexpected behaviour with two different dynamic rules with
the same label.\
**A:** If you are not using [Stratego/XT
0.14](StrategoRelease014){.twikiLink} or later please upgrade. For more
information see [dynamic rule
semantics](DynamicRuleSemantics){.twikiLink}.

[]{#Stratego_Libary} Stratego Libary
------------------------------------

**Q:** `collect` removes duplicates, is there
`collect-with-duplicates`?\
**A:** Yes, there is. The collect strategy is an alias of `collect-om`.
`collect-om` has a variant that takes a strategy argument that is used
to combine intermediate results. If you pass `conc` instead of `union`,
then duplicates will not be removed.

**Q:** Is it possible to redirect the stderr of process to a file in
Stratego?\
**A:** Yes, this works exactly the same a redirection in C. Example:

        module example
        imports posix-file char-io

        strategies

          main =
              <open> "error.txt" => fd
            ; <dup2> (fd, <STDERR_FILENO>)
            ; <debug> "bla bla bla 1"
            ; <fputs> ("bla bla bla 2", <stderr-stream>)
            ; <close> fd

See \'man dup2\' for more information.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
