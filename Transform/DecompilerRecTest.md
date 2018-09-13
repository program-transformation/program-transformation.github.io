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
    Page](http://www.program-transformation.org/edit/Transform/DecompilerRecTest?t=1536826467)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilerRecTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilerRecTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilerRecTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilerRecTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Transform/DecompilerRecTest?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Transform/DecompilerRecTest?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Transform/DecompilerRecTest?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/DecompilerRecTest?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/DecompilerRecTest?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/DecompilerRecTest?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilerRecTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilerRecTest?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilerRecTest?template=oopsmore&param1=1.7&param2=1.7)
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
Decompiler Rec Test {#decompiler-rec-test .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Reverse_Engineering_Compiler_REC} Reverse Engineering Compiler (REC) Tests
==============================================================================

Some simple tests were performed on REC 1.6 for Linux.

::: {.twikiToc}
-   [Reverse Engineering Compiler (REC)
    Tests](DecompilerRecTest#Reverse_Engineering_Compiler_REC)
    -   [Fibo/286](DecompilerRecTest#Fibo_286)
    -   [Fibo/Elf](DecompilerRecTest#Fibo_Elf)
    -   [Fibo/SPARC](DecompilerRecTest#Fibo_SPARC)
    -   [Switch/SPARC](DecompilerRecTest#Switch_SPARC)
    -   [Switch/X86](DecompilerRecTest#Switch_X86)
:::

[]{#Fibo_286} Fibo/286
----------------------

This test file is the same one used to test the 286 decompilers (dcc and
Exe-2-C). It\'s pretty impressive that REC can handle this old code at
all. Original C source:

    int main()
    { int i, numtimes, number;
      unsigned value, fib();

        printf("Input number of iterations: ");
        scanf ("%d", &numtimes);
        for (i = 1; i <= numtimes; i++)
        {
            printf ("Input number: ");
            scanf ("%d", &number);
            value = fib(number);
            printf("fibonacci(%d) = %u\n", number, value);
        }
        exit(0);
    }

    unsigned fib(x)                 /* compute fibonacci number recursively */
    int x;
    {
        if (x > 2)
            return (fib(x - 1) + fib(x - 2));
        else
            return (1);
    }

The disassembly for the `fib` function is

    /*      Procedure: 0x0000025B - 0x0000028A
     *      Argument size: 4
     *      Local size: 0
     *      Save regs size: 4
     */

    L0000025B(A4)
    /* unknown */ void  A4;
    {
        if(A4 <= 2) {
            ax = 1;
        } else {
            (save)L0000025B(A4 - 1);
            dx = L0000025B(A4 + 65534);
            (restore)ax;
            ax = ax + dx;
        }
    }

As with Exe-2-C, push and pop are explicit (as `save` and `restore`),
registers are still visible, and no attempt is made to join the
semantics of individual instructions. Parameter type and return values
are not present.

Here is the code for `main`:

    /*      Procedure: 0x000001FA - 0x0000025A
     *      Argument size: 0
     *      Local size: 4
     *      Save regs size: 8
     */

    L000001FA()
    {
            /* unknown */ void  si;
            /* unknown */ void  di;
            /* unknown */ void  Vfffffffc;
            /* unknown */ void  Vfffffffe;



        L00000E11(0x194);
        L0000169A(0x1b1, & Vfffffffc);
        for(si = 1; si <= Vfffffffc; si = si + 1) {
            L00000E11(0x1b4);
            L0000169A(0x1c3, & Vfffffffe);
            (save)L0000025B(Vfffffffe);
            L00000E11(0x1c6, Vfffffffe);
        }
        return(L000002C7(0));
    }

It has not recognised the library functions `printf`, `scanf`, and
`exit`. It has recovered the for loop. There is no `restore` to
correspond to the `save` (it has not realised that the save is actually
passing a second parameter to `printf`). String constants are not
recovered.

[]{#Fibo_Elf} Fibo/Elf
----------------------

Elf is a more modern binary file format, and it has some symbolic
information (even in binary files \"stripped\" of their symbol tables).
REC was able to find the name for functions `fib` and `main`, even when
the symbols were stripped. Strangely, however, it failed to recover the
string constants in the \_un\_stripped version. Here is the original C
source (`main` is a little different to the 286 Fibo program):

    #include 

    int fib (int x)
    {
            if (x > 1)
                    return (fib(x - 1) + fib(x - 2));
            else return (x);
    }

    int main (void)
    {       int number, value;

            printf ("Input number: ");
            scanf ("%d", &number);
            value = fib(number);
            printf("fibonacci(%d) = %d\n", number, value);
            return (0);
    }

Here is the decompilation for `fib`:

    /*      Procedure: 0x08048798 - 0x080487C8
     *      Argument size: 4
     *      Local size: 0
     *      Save regs size: 8
     */

    fib(A8)
    /* unknown */ void  A8;
    {
            /* unknown */ void  esi;
        if(A8 > 1) {
            (save)A8 - 1;
            esi = fib();
            eax = fib(A8 - 2) + esi;
        } else {
            eax = A8;
        }
    }

It correctly generated the actual parameter for the second (recursive)
call to `fib`, but in the first one it generated a `save` and no
parameter. It correctly deals with the return value from the recursive
calls to `fib`, but fails to emit a return statement. Again, the number
of parameters is right, but the type is wrong.

Here is REC\'s decompilation for `main` (stripped version):

    /*      Procedure: 0x080487CC - 0x0804882C
     *      Argument size: 0
     *      Local size: 4
     *      Save regs size: 8
     */

    main()
    {
            /* unknown */ void  ebx;
            /* unknown */ void  esi;
            /* unknown */ void  Vfffffffc;



        (save)"Input number: ";
        printf();
        (save) & Vfffffffc;
        (save)"%d";
        scanf();
        ebx = Vfffffffc;
        esp = esp + 12;
        if(ebx > 1) {
            esi = fib(ebx - 1);
            eax = fib(ebx - 2) + esi;
        } else {
            eax = ebx;
        }
        printf("fibonacci(%d) = %d\n", Vfffffffc, eax);
        esp = ebp - 12;
        return(0);
    }

Library function names are recovered (it\'s much easier with dynamic
linking). Here, the arguments to some of the library functions are
passed correctly to the library functions, and not to others. Note that
one level of `fib` has actually been inlined into `main` by the
compiler, and this time, it gets the parameters correct.

[]{#Fibo_SPARC} Fibo/SPARC
--------------------------

The same program as above but compiled for SPARC/Solaris (also using
gcc) was decompiled, using the SPARC/Solaris version of REC. The results
for fib are:

    /*      Procedure: 0x00010A9C - 0x00010ACF
     *      Argument size: -112
     *      Local size: 112
     *      Save regs size: 0
     */

    fib()
    {
        r16 = r24;
        if(r16 > 1) {
            r24 = fib(r16 + -1);
            r24 = r24 + fib(r16 + -2);
        }
        return(r24);
    }

It got the formal parameters right to the recursive calls correct, but
not the formal parameter. This time it does return a value.

This is the result for main:

    /*      Procedure: 0x00010AD0 - 0x00010B2F
     *      Argument size: -120
     *      Local size: 120
     *      Save regs size: 0
     */

    main()
    {
            /* unknown */ void  Vffffffec;
        printf("Input number: ");
        r9 = & Vffffffec;
        scanf("%d");
        r24 = Vffffffec;
        r10 = r24;
        if(r24 > 1) {
            r8 = r24 + -1;
            r16 = fib();
            r8 = r24 + -2;
            r10 = r16 + fib();
        }
        r9 = Vffffffec;
        printf("fibonacci(%d) = %d\n");
        return(r24);
    }

Here, it gets the first parameter to printf and scanf correct; the
second parameters are simply assigned to r9. This time, the actual
parameter to the calls to fib are missing.

[]{#Switch_SPARC} Switch/SPARC
------------------------------

This program tests the recognition of switch statements.

The original C source code is

    #include 
    int main(int argc)
    {
        switch(argc)
        {
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

A disassembly of the first part of main is as follows:

    main()
            1090c:  9d e3 bf a0        save         %sp, -96, %sp
            10910:  92 26 20 02        sub          %i0, 2, %o1
            10914:  11 00 00 42        sethi        %hi(_ex_text0), %o0
            10918:  90 02 20 f4        add          %o0, 0xf4, %o0
            1091c:  80 a2 60 05        cmp          %o1, 5
            10920:  18 80 00 23        bgu          0x109ac
            10924:  93 2a 60 02        sll          %o1, 2, %o1
            10928:  d2 02 40 08        ld           [%o1 + %o0], %o1
            1092c:  81 c2 40 08        jmp          %o1 + %o0
            10930:  01 00 00 00        nop          

The decompilation of the first part of main is as follows:

    /*      Procedure: 0x0001090C - 0x000109BF
     *      Argument size: -96
     *      Local size: 96
     *      Save regs size: 0
     */

    main()
    {
        r9 = 2 - r24;
        r8 = 0x108f4;
        r9 = r9 << 2;
        if(r9 <= 5) {
            r9 = *(r9 + 0x108f4);
            goto (r9 + 0x108f4);
            r8 = printf(0x10a38);
            }
            return(r24);
            r8 = printf("Three!\n");
            }
            return(r24);
            r8 = printf("Four!\n");
            ...

This shows that the SPARC semantics are quite immature compared to the
X86 semantics. For example, the first statement has the operands to the
subtract around the wrong way. Worse, the compare against 5 must happen
before the left shift by 2 (which multiplies the register by 4).
Finally, the indirect jump is left as goto (r9 + \...). Note that one of
the parameters to printf is not converted to a string, but the others
are.

I thought that the \"computed goto\" might be because the table above is
of offsets, not direct pointers to code. However, the same code compiled
with `gcc` (which *does* use straight pointers) is about the same:

        if(r9 <= 5) {
            goto ( *(0x10a7c + (r9 << 2)));

[]{#Switch_X86} Switch/X86
--------------------------

The same source code as the above was compiled (also with gcc) for
Pentium (Solaris/X86, though the compiler for Linux/X86 is very
similar). The beginning of main disassembles as follows:

main() 80488f0: 55 pushl %ebp 80488f1: 8b ec movl %esp,%ebp 80488f3: 8b
45 08 movl 8(%ebp),%eax 80488f6: 05 fe ff ff ff addl \$0xfffffffe,%eax
80488fb: 3d 05 00 00 00 cmpl \$0x5,%eax 8048900: 76 76 jbe 0x76
\<8048978\> 8048902: 68 a0 9b 04 08 pushl \$0x8049ba0 8048907: e8 c8 fe
ff ff call 0xfffffec8 \... 8048978: ff 24 85 e8 89 04 08 jmp
\*134515176(,%eax,4)

The decompiled output for the start of main is

    /* DEST BLOCK NOT FOUND: 08048978 -> 080487d4 */
    /*      Procedure: 0x080488F0 - 0x0804898F
     *      Argument size: 4
     *      Local size: 0
     *      Save regs size: 0
     */

    main(A8)
    /* unknown */ void  A8;
    {
        eax = A8 + -2;
        if(eax > 5) {
            printf(0x8049ba0);
            return(0);
            printf(0x8049b58);
            esp = ebp;
            return(0);
            printf(0x8049b64);
            esp = ebp;
            return(0);
            printf(0x8049b70);
            esp = ebp;
    ...
        }
        goto *(eax * 4 + 0x80489e8)[L08048914, L08048928, L0804893c, L08048950,
    L08048964, L0804897f, ]goto ( *(eax * 4 + 0x80489e8));

Again, the indirect jump becomes a sort of \"computed goto\", but this
time the possible destination labels are given. Unfortunately, the
labels are missing from the code, and it would have been nice to see an
actual switch statement.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.DecompilerRecTest moved from Transform.DecompilationRecTest
on 20 Mar 2003 - 03:06 by
[MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Transform/DecompilerRecTest?newweb=Transform&newtopic=DecompilationRecTest&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
