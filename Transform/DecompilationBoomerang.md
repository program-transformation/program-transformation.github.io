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
    Page](http://www.program-transformation.org/edit/Transform/DecompilationBoomerang?t=1536826456)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilationBoomerang)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilationBoomerang)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilationBoomerang?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilationBoomerang?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Transform/DecompilationBoomerang?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/DecompilationBoomerang?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Transform/DecompilationBoomerang?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/DecompilationBoomerang?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/DecompilationBoomerang?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/DecompilationBoomerang?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilationBoomerang)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilationBoomerang?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilationBoomerang?template=oopsmore&param1=1.7&param2=1.7)
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
Decompilation Boomerang {#decompilation-boomerang .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#The_Boomerang_Decompiler_and_Tes} The Boomerang Decompiler and Tests
========================================================================

Boomerang is an attempt at a complete, retargetable decompiler for
native executable programs, released under a BSD style (open source)
license.

::: {.twikiToc}
-   [The Boomerang Decompiler and
    Tests](DecompilationBoomerang#The_Boomerang_Decompiler_and_Tes)
    -   [Introduction](DecompilationBoomerang#Introduction)
    -   [Tests](DecompilationBoomerang#Tests)
        -   [Fibo](DecompilationBoomerang#Fibo)
        -   [TwoProc](DecompilationBoomerang#TwoProc)
        -   [Switch](DecompilationBoomerang#Switch)
:::

[]{#Introduction} Introduction
------------------------------

It was intended to be highly modular, so that different parts of the
decompiler can be replaced with experimental modules. (As of mid 2004,
this is slowly being implemented, using [XML](XML){.twikiLink} to join
the various modules.) It is envisaged to one day become interactive, a
la IDA Pro, because some things (not just variable names and comments,
though these are obviously very important) require expert intervention.

In July 2004, there was a preview binary distribution (version alpha
0.1). Source code is available via [CVS](CVS){.twikiLink}. Boomerang is
now at the stage where it can decompile correctly several small Pentium
and SPARC programs. The dataflow design is finally complete; it uses a
combination of fairly standard SSA (Static Single Assignment) and a
small theorem prover. It recovers parameters and return values fairly
well.

Boomerang was used in a small, successful commercial decompilation
project. An experience report will be published at
[WCRE](WCRE){.twikiLink} 2004 (November), titled \"Using a Decompiler
for Real-World Source Recovery\". During this project, several
significant enhancements were made to Boomerang, including the ability
to specify names and types in a symbol file, support for the `thiscall`
calling convention, and so on.

The next major step is that of type analysis; work has started.

The [SourceForge](http://www.sourceforge.net) page is
<http://boomerang.sourceforge.net>.

[]{#Tests} Tests
----------------

### []{#Fibo} Fibo

The original source code for Fibo is:

    #include < stdio.h >
    int fib (int x)
    {
        if (x > 1)
            return (fib(x - 1) + fib(x - 2));
        else return (x);
    }
    int main (void)
    {   int number, value;

        printf ("Input number: ");
        scanf ("%d", &number);
        value = fib(number);
        printf("fibonacci(%d) = %d\n", number, value);
        return (0);
    }

As of August 2003, this is the output from Boomerang
(`test/pentium/switch_gcc`):

    int main()
    {
    int local0;
    ...
    int local9;
        printf("Input number: ");
        scanf("%d", &local7);
        if (local7 <= 1) {
            local9 = local7;
        } else {
            local9 = fib(local7 - 1);
            local8 = fib(local7 - 2);
            local9 = local8 + local9;
        }
        printf("fibonacci(%d) = %d\n", local7, local9);
        local9 = 0;
        return local9;
    }

    int fib(int param8)
    {
    int local0;
    ...
    int local7;
        if (param8 <= 1) {
            local7 = param8;
        } else {
            local7 = fib(param8 - 1);
            local6 = fib(param8 - 2);
            local7 = local6 + local7;
        }
        return local7;
    }

Boomerang is finally able to process Fibo. The outout compiles and runs
correctly with no modifications. There are a few more local variables
that I would like, but this is a minor point, and could be fixed soon
anyway. The Pentium and Sparc versions both decompile to very similar
code, despit the very different code at the machine language level.

### []{#TwoProc} TwoProc

Here is a very simple test program:

    int proc1(int a, int b) {
        return a + b;
    }

    int main() {
        printf("%i\n", proc1(3, 4));
    }

The Boomerang output is

    int main()
    {
    int local0;
    ...
    int local5;
        local5 = proc1(4, 3);
        local5 = printf("%i\n", local5);
        return local5;
    }

    int proc1(int param4, int param7)
    {
    int local0;
    int local1;
        local1 = param4 + param7;
        return local1;
    }

Again, the code recompiles and runs correctly with no modifications.
Again, there are too many local variables. At one stage, with global
dataflow analysis, main transformed to essentially
\"`printf("%i\n", 7)`\", but this no longer happens (dataflow is local
to a procedure again).

### []{#Switch} Switch

Original C source code:

    int main(int argc) {
        switch(argc) {
            case 2:
                printf("Two!\n"); break;
            case 3:
                printf("Three!\n"); break;
            case 4:
                printf("Four!\n"); break;
            case 5:
                printf( "Five!\n"); break;
            case 6:
                printf( "Six!\n"); break;
            case 7:
                printf( "Seven!\n"); break;
            default:
                printf( "Other!\n"); break;
        }
        return 0;
    }

Here is the Boomerang output (July 2004), using the -dt (use and debug
type analysis):

    int global0[1] = { 134515020 };
    char* global1 = "Other!\n";

    int main(int argc, char** argv, char** envp)
    {
    int local1; // m[r28{0} - 8]
    int local3; // r29
    int local4; // r28
        if ((unsigned)(argc - 2) > 5) {
            local1 = "Other!\n";
        } else {
            switch(argc) {
            case 2:
                local1 = "Two!\n";
                break;
            case 3:
                local1 = "Three!\n";
                break;
            case 4:
                local1 = "Four!\n";
                break;
            case 5:
                local1 = "Five!\n";
                break;
            case 6:
                local1 = "Six!\n";
                break;
            case 7:
                local1 = "Seven!\n";
                break;
            }
        }
        printf(local1, local3, *(int*)local4, argc, argv);
        return 0;/* local4 + 4, 0*/
    }

This compiles and runs correctly. It would be nice to convert the if
statement near the start into a \"default\" case. Again, there are too
many locals; this should be fixed soon.

------------------------------------------------------------------------

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.DecompilationBoomerang moved from
Transform.DeCompilationBoomerang on 03 Feb 2003 - 06:50 by
[MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Transform/DecompilationBoomerang?newweb=Transform&newtopic=DeCompilationBoomerang&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
