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
    Page](http://www.program-transformation.org/edit/Transform/DccDecompilerTests?t=1536826453)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DccDecompilerTests)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DccDecompilerTests)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DccDecompilerTests?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DccDecompilerTests?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/DccDecompilerTests?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DccDecompilerTests?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DccDecompilerTests?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DccDecompilerTests)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DccDecompilerTests?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/DccDecompilerTests?template=oopsmore&param1=1.2&param2=1.2)
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
Dcc Decompiler Tests {#dcc-decompiler-tests .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

::: {.twikiToc}
-   [Strlen](DccDecompilerTests#Strlen)
-   [Fibo](DccDecompilerTests#Fibo)
-   [Matrix Multiplication](DccDecompilerTests#Matrix_Multiplication)
-   [Dhampstone benchmark](DccDecompilerTests#Dhampstone_benchmark)
:::

The tests performed here are downloaded from the file
[test.zip](http://www.itee.uq.edu.au/~cristina/dcc/distribution/test.zip),
part of the dcc distribution. It should be remembered that these tests
were therefore chosen to suit the dcc decompiler.

### []{#Strlen} Strlen

The original C source for this program is as follows:

    main()
    { char *s = "test";
        strlen(s);
    }
    strlen(char *s)
    { int n = 0;
        while (*s++)
            n++;
        return (n);
    }

This disassembled as follows:

                    proc_1  PROC  NEAR
    000 000305 55                  PUSH           bp
    001 000306 8BEC                MOV            bp, sp
    002 000308 56                  PUSH           si
    003 000309 33F6                XOR            si, si

    005 00030E 8B5E04         L1:  MOV            bx, [bp+4]
    006 000311 FF4604              INC   word ptr [bp+4]
    007 000314 803F00              CMP   byte ptr [bx], 0
    008 000317 75F4                JNE            L2
    009 000319 8BC6                MOV            ax, si
    011 00031D 5E                  POP            si
    012 00031E 5D                  POP            bp
    013 00031F C3                  RET

    014 00030D 46             L2:  INC            si
    015                            JMP            L1                 ;Synthetic inst
                    proc_1  ENDP

                    main  PROC  NEAR
    000 0002FA 56                  PUSH           si
    001 0002FB BE9401              MOV            si, 194h
    002 0002FE 56                  PUSH           si
    003 0002FF E80300              CALL  near ptr proc_1
    004 000302 59                  POP            cx
    005 000303 5E                  POP            si
    006 000304 C3                  RET

                    main  ENDP

The decompiled output:

    /*
     * Input file   : test\strlen.exe
     * File type    : EXE
     */

    #include "dcc.h"


    void proc_1 (int arg0)
    /* Takes 2 bytes of parameters.
     * High-level language prologue code.
     * C calling convention.
     */
    {
    int loc1;

        loc1 = 0;
        arg0 = (arg0 + 1);

        while ((*arg0 != 0)) {
            loc1 = (loc1 + 1);
            arg0 = (arg0 + 1);
        }   /* end of while */
    }

    void main ()
    /* Takes no parameters.
     */
    {
    int loc1;

        loc1 = 404;
        proc_1 (loc1);
    }

Here, arg0 is typed as an int, when in fact it is a char\*. The program
would actually compile, if one cast was added. This is the price of not
having type inference; the program does not compile (the semantics are
ambiguous).

Unfortunately, there is an increment of `arg0` outside the loop, which
makes the program logic incorrect. dcc would have recovered the return
type of `strlen` (`proc1`), if the return value was used.

### []{#Fibo} Fibo

The original C source code is:

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

The disassembly for the fib function is

                    proc_1  PROC  NEAR
    000 00035B 55                  PUSH           bp
    001 00035C 8BEC                MOV            bp, sp
    002 00035E 56                  PUSH           si
    003 00035F 8B7604              MOV            si, [bp+4]
    004 000362 83FE02              CMP            si, 2
    005 000365 7E1C                JLE            L1
    006 000367 8BC6                MOV            ax, si
    007 000369 48                  DEC            ax
    008 00036A 50                  PUSH           ax
    009 00036B E8EDFF              CALL  near ptr proc_1
    010 00036E 59                  POP            cx
    011 00036F 50                  PUSH           ax
    012 000370 8BC6                MOV            ax, si
    013 000372 05FEFF              ADD            ax, 0FFFEh
    014 000375 50                  PUSH           ax
    015 000376 E8E2FF              CALL  near ptr proc_1
    016 000379 59                  POP            cx
    017 00037A 8BD0                MOV            dx, ax
    018 00037C 58                  POP            ax
    019 00037D 03C2                ADD            ax, dx

    021 000388 5E             L2:  POP            si
    022 000389 5D                  POP            bp
    023 00038A C3                  RET

    024 000383 B80100         L1:  MOV            ax, 1
    025 000386 EB00                JMP            L2

                    proc_1  ENDP

Note that a branch before L2 has been eliminated, and the addresses are
a little out of order. The decompiled output is as follows:

    /*
     * Input file   : fibos.exe
     * File type    : COM
     */

    #include "dcc.h"


    int proc_1 (int arg0)
    /* Takes 2 bytes of parameters.
     * High-level language prologue code.
     * C calling convention.
     */
    {
    int loc1;
    int loc2; /* ax */

        loc1 = arg0;

        if (loc1 > 2) {
            loc2 = (proc_1 ((loc1 - 1)) + proc_1 ((loc1 + 0xFFFE)));
        }
        else {
            loc2 = 1;
        }
        return (loc2);
    }

    void main ()
    /* Takes no parameters.
     * High-level language prologue code.
     */
    {
    int loc1;
    int loc2;
    int loc3;
    int loc4;

        printf ("Input number of iterations: ");
        scanf ("%d", &loc1);
        loc3 = 1;
        while ((loc3 <= loc1)) {
            printf ("Input number: ");
            scanf ("%d", &loc2);
            loc4 = proc_1 (loc2);
            printf ("fibonacci(%d) = %u\n", loc2, loc4);
            loc3 = (loc3 + 1);
        }
        exit (0);
    }

dcc has recovered the parameters (both formal and actual), and the
return type. Library function names have been recovered. In fact, this
output compiles, and runs correctly (or it would on a system with 16 bit
integers; replacing the 0xFFFE with -2 corrects the problem).

### []{#Matrix_Multiplication} Matrix Multiplication

The original source is:

    #define n 5
    #define m 4

    static void multMatrix (int a[n][m], int b[m][n], int c[n][n])
    { int i,j,k;

            for (i=0; i<n; i++)
                for (j=0; j<m; j++)
                    for (k=0; k<m; k++)
                        c[i][j] = a[i][k] * b[k][j] + c[i][j];
    }

    main()
    { int a[n][m], b[n][m], c[n][m];

            multMatrix (a,b,c);
    }

The disassembly for the matrixMult procedure only is rather large:

                    proc_1  PROC  NEAR
    000 0002FA 55                  PUSH           bp
    001 0002FB 8BEC                MOV            bp, sp
    002 0002FD 83EC02              SUB            sp, 2
    003 000300 56                  PUSH           si
    004 000301 57                  PUSH           di
    005 000302 33F6                XOR            si, si

    007 000378 83FE05         L1:  CMP            si, 5
    008 00037B 7C89                JL             L2
    009 00037D 5F                  POP            di
    010 00037E 5E                  POP            si
    011 00037F 8BE5                MOV            sp, bp
    012 000381 5D                  POP            bp
    013 000382 C3                  RET

    014 000306 33FF           L2:  XOR            di, di

    016 000372 83FF04         L3:  CMP            di, 4
    017 000375 7C93                JL             L4
    018 000377 46                  INC            si
    019                            JMP            L1                 ;Synthetic inst
    020 00030A C746FE0000     L4:  MOV   word ptr [bp-2], 0

    022 00036B 837EFE04       L5:  CMP   word ptr [bp-2], 4
    023 00036F 7CA0                JL             L6
    024 000371 47                  INC            di
    025                            JMP            L3                 ;Synthetic inst
    026 000311 8BDE           L6:  MOV            bx, si
    027 000313 D1E3                SHL            bx, 1
    028 000315 D1E3                SHL            bx, 1
    029 000317 D1E3                SHL            bx, 1
    030 000319 035E04              ADD            bx, [bp+4]
    031 00031C 8B46FE              MOV            ax, [bp-2]
    032 00031F D1E0                SHL            ax, 1
    033 000321 03D8                ADD            bx, ax
    034 000323 8B07                MOV            ax, [bx]
    035 000325 50                  PUSH           ax
    036 000326 8B46FE              MOV            ax, [bp-2]
    037 000329 BA0A00              MOV            dx, 0Ah
    038 00032C F7E2                MUL            dx
    039 00032E 8BD8                MOV            bx, ax
    040 000330 035E06              ADD            bx, [bp+6]
    041 000333 8BC7                MOV            ax, di
    042 000335 D1E0                SHL            ax, 1
    043 000337 03D8                ADD            bx, ax
    044 000339 58                  POP            ax
    045 00033A F727                MUL   word ptr [bx]
    046 00033C 50                  PUSH           ax
    047 00033D 8BC6                MOV            ax, si
    048 00033F BA0A00              MOV            dx, 0Ah
    049 000342 F7E2                MUL            dx
    050 000344 8BD8                MOV            bx, ax
    051 000346 035E08              ADD            bx, [bp+8]
    052 000349 8BC7                MOV            ax, di
    053 00034B D1E0                SHL            ax, 1
    054 00034D 03D8                ADD            bx, ax
    055 00034F 58                  POP            ax
    056 000350 0307                ADD            ax, [bx]
    057 000352 50                  PUSH           ax
    058 000353 8BC6                MOV            ax, si
    059 000355 BA0A00              MOV            dx, 0Ah
    060 000358 F7E2                MUL            dx
    061 00035A 8BD8                MOV            bx, ax
    062 00035C 035E08              ADD            bx, [bp+8]
    063 00035F 8BC7                MOV            ax, di
    064 000361 D1E0                SHL            ax, 1
    065 000363 03D8                ADD            bx, ax
    066 000365 58                  POP            ax
    067 000366 8907                MOV            [bx], ax
    068 000368 FF46FE              INC   word ptr [bp-2]
    069                            JMP            L5                 ;Synthetic inst

The decompiled output for the multMatrix procedure only:

    /*
     * Input file   : test\matrixmu.exe
     * File type    : EXE
     */

    #include "dcc.h"


    void proc_1 (int arg0, int arg1, int arg2)
    /* Takes 6 bytes of parameters.
     * High-level language prologue code.
     * C calling convention.
     */
    {
    int loc1;
    int loc2;
    int loc3;

        loc2 = 0;
        while ((loc2 < 5)) {
            loc3 = 0;
            while ((loc3 < 4)) {
                loc1 = 0;
                while ((loc1 < 4)) {
                    *((((loc2 * 10) + arg2) + (loc3 << 1))) =
                          ((*((((loc2 << 3) + arg0) + (loc1 << 1))) *
                            *((((loc1 * 10) + arg1) + (loc3 << 1)))) +
                            *((((loc2 * 10) + arg2) + (loc3 << 1))));
                    loc1 = (loc1 + 1);
                }
                loc3 = (loc3 + 1);
            }
            loc2 = (loc2 + 1);
        }
    }

As Cristina states in her thesis, this example shows that forward
substitution is able to find array expressions. The conversion to array
format was not done, although an algorithm to achieve this was
suggested. Again, the above will not compile, because the size of the
items pointed to by the indirection operators (stars) is not given. It
is desirable that expressions such as the above are converted to array
format, because the assumption in the above code (that sizeof(int) == 2)
is unlikely to be true for modern compilers.

The for loops are here converted to functionally equivalent while loops.
The number of formal parameters is correctly found.

### []{#Dhampstone_benchmark} Dhampstone benchmark

The only source file contained in the above test.zip file was `dhamp.c`
, another benchmark program. The main function is as follows:

    #define NUMTEST 6
    main()
    {
    char buf1[TINY], buf2[TINY];
    int i = 0;
    unsigned fib ();
    long square, sq ();
    double dmath, sroot (), dply ();

    printf("Start...%c\n\n",BELL);
    while (i < NUMTEST)
        {
        switch (i)
            {
            case (0):                                   /* Character test       */
                results.cresult = stest (buf1,buf2);
                printf ("\ncresult = %d\n",results.cresult);
                break;
            case (1):                                   /* Integer test         */
                results.iresult = intest ();
                printf ("\niresult = %d\n",results.iresult);
                break;
            case (2):                                   /* Unsigned test        */
                results.uresult = fib (FIB);
                printf ("\nuresult = %u\n",results.uresult);
                break;
            case (3):                                   /* Long test            */
                ...
            default:
                break;
            }
        ++i;
        }                                           /* End while i          */
    printf ("\n\n...End%c",BELL);
    }

The decompiled output for main is as follows:

    void main ()
    /* Takes no parameters.
     * High-level language prologue code.
     * Contains instructions not normally used by compilers.
     * Contains coprocessor instructions.
     */
    {
    int loc1;
    int loc2;
    ...
    int loc11;
    int loc12; /* ax */
    int loc13; /* bx */

        loc11 = 0;
        printf ("Start...%c\n\n", 7);
        while ((loc11 < 6)) {
            loc12 = loc11;
            if (loc12 <= 5) {
                loc13 = (loc12 << 1);
                var06278 = proc_1 (&loc2, &loc1, , );
                printf ("\ncresult = %d\n", var06278);
            }
            loc11 = (loc11 + 1);
        }
        printf ("\n\n...End%c", 7);
    }

Only the first branch of the switch statement is decompiled. This is a
result of ignoring the indirect branch, falling in to the code for the
first case, and not finding any control paths to the other cases. In her
thesis, Cristina suggests several idioms for detecting switch
statements, but none have been implemented in dcc. The variable loc12
could have been eliminated, merely replaced by loc11.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
