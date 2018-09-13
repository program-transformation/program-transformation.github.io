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
    Page](http://www.program-transformation.org/edit/Transform/DecompilerDesquirrTest?t=1536826464)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilerDesquirrTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilerDesquirrTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilerDesquirrTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilerDesquirrTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Transform/DecompilerDesquirrTest?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/DecompilerDesquirrTest?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/DecompilerDesquirrTest?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DecompilerDesquirrTest?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/DecompilerDesquirrTest?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DecompilerDesquirrTest?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilerDesquirrTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilerDesquirrTest?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilerDesquirrTest?template=oopsmore&param1=1.4&param2=1.4)
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
Decompiler Desquirr Test {#decompiler-desquirr-test .twikiTopicTitle}
========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

These Fibonacci (286) and Palindrome results are from David\'s masters
theses, Figure 5.2. The other tests are using the 20030507 binary of the
desquirr plugin, as downloaded from the
[Sourceforge](http://sourceforge.net/project/showfiles.php?group_id=53491)
page.

::: {.twikiToc}
-   [Fibonacci (286)](DecompilerDesquirrTest#Fibonacci_286)
-   [Fibonacci (ELF/386)](DecompilerDesquirrTest#Fibonacci_ELF_386)
-   [Palindrome test](DecompilerDesquirrTest#Palindrome_test)
-   [Switch\_gcc](DecompilerDesquirrTest#Switch_gcc)
-   [Switch\_cc](DecompilerDesquirrTest#Switch_cc)
-   [Sumarray-O4](DecompilerDesquirrTest#Sumarray_O4)
:::

[]{#Fibonacci_286}[]{#Fibonacci_286_} Fibonacci (286)
-----------------------------------------------------

David apparently used one of the [dcc](DccDecompiler){.twikiLink} test
programs. The original C source code is:

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

The decompiled output is as follows:

    sub 10291:
      _printf("Input number of iterations: ");
      ax = _scanf("%d", & var_2);
      si = 1;
      goto loc_102DD;

    loc 102AF:
      _printf("Input number: ");
      scanf("%d", & var_4);
      var_6 = sub_102EB(var_4);
      ax = _printf("fibonacci(%d) = %u\n", var_4, var_6);
      si = si + 1;

    loc 102DD:
      if (si <= var_2) goto loc_102AF;

      _exit(0);
      return ax;


    sub_102EB:
      if (arg 0 <= 2) goto loc_10313;

      dx = sub_102EB(arg_0 - 1);
      ax = sub_102EB(arg_0 + 0xfffe);
      ax = dx + ax;
      goto loc 10318;

      goto loc 10318;

    loc_10313:
      ax = 1;
      goto loc_10318;

    loc_10318:
      return ax;

Registers are visible; variables, procedures and parameters are not
declared. Control flow is limited to `if (...) goto` *label;* Actual
parameters are recovered well.

Note: I tried to reproduce these results with the original 80286
binaries, and get much worse results. Presumably, David compiled the
test program with a different compiler. It\'s impressive that Desquirr
can handle 80286 code at all, though perhaps IDA is handling most of the
286 uglinesses.

[]{#Fibonacci_ELF_386}[]{#Fibonacci_ELF_386_} Fibonacci (ELF/386)
-----------------------------------------------------------------

Original source code (slightly different to the above Fibonacci
program):

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

Decompiled output:

    main:
      _printf("Input number: ");
      _scanf("%d", & var_4);
      sp = sp + 12;
      if (bx <= 1) goto loc_8048814;

      fib(bx + -1);
      ax = fib(bx + -2) + si;
      goto loc_8048816;

    loc_8048814:
      ax = bx;

    loc_8048816:
      _printf("fibonacci(%d) = %d\n", var_4, ax);
      /* pop  */
      /* pop  */
      return 0;

    fib:
      if (bx <= 1) goto loc_80487C0;

      fib(bx + -1);
      ax = fib(bx + -2) + si;
      goto loc_80487C2;

    loc_80487C0:
      ax = bx;

    loc_80487C2:
      /* pop  */
      /* pop  */
      return ax;

Some code is missing, e.g. near the top of main, `bx = var4`. Parameters
and returns are missing from fib().

[]{#Palindrome_test} Palindrome test
------------------------------------

The original source code is:

    #include <stdio.h>
    #include <string.h>
    #include <malloc.h>

    void rev(char* source, char* destination)
    {
      char* tmp = destination + strlen(source);
      for (*tmp-- = 0; *source; *tmp-- = *source++)
        ;
    }

    int main(int argc, char**argv)
    {
      char* original = NULL;
      char* reverse = NULL;

      if (argc < 2)
      {
        original = "nitalarbralatin";

      }
      else
      {
        original = argv[1];
      }

      reverse = malloc(strlen(original)+1);

      rev(original, reverse);
      if (0 == strcmp(original, reverse))
      {
        printf("%s is a palindrome\n", original);
      }
      else
      {
        printf("Try again!\n");
      }

      free(reverse);

      return 0;
    }

The decompiled output is:

    sub_401150:
      bx = arg_0;
      ax = _strlen(bx) + arg_4;
      * ax = 0;
      ax = ax - 1;
      goto loc_40116E;

    loc_401167:
      dl = * bx;
      bx = bx + 1;
      ax = ax - 1;
      * (ax + 1) = dl;

    loc_40116E:
      if ((* bx) != 0) goto loc_401167;

      return ax;


    _main:
      if (argc >= 2) goto loc_401188;

      bx = "nitalarbralatin";
      goto loc_40118E;

    loc_401188:
      bx = * (argv + 4);

    loc_40118E:
      si = _malloc(_strlen(bx) + 1);
      sub_401150(bx, si);
      if (_strcmp(bx, si) != 0) goto loc_4011C7;

      _printf("%s is a palindrome\n", bx);
      goto loc_4011D2;

    loc_4011C7:
      _printf("Try again!\n");

    loc 4011D2:
      _free(si);
      return 0;

[]{#Switch_gcc} Switch\_gcc
---------------------------

This is the boomerang test from test/pentium/switch\_gcc. Original
source code is:

    int main(int argc)
    {
        switch(argc)
        {
            case 2: printf("Two!\n"); break;
            case 3: printf("Three!\n"); break;
            case 4: printf("Four!\n"); break;
            case 5: printf("Five!\n"); break;
            case 6: printf("Six!\n"); break;
            case 7: printf("Seven!\n"); break;
            default:printf("Other!\n"); break;
            }
        return 0;
    }

Decompiled output:

    main:
      switch (arg_0)

    off_8048934:

      case 0:
      goto loc_8048981;

      case 1:
      goto loc_8048981;

      case 2:
      goto loc_8048981;

      case 3:
      goto loc_8048981;

      case 4:
      goto loc_8048981;

      case 5:
      goto loc_8048981;

    loc_804897C:

    loc_8048981:
      _printf("Other!\n", "Seven!\n", "Six!\n", "Five!\n", "Four!\n", "Three!\n", "Two!\n");
      return 0;

Desquirr seems to have ignored the gotos, so that all the push
instructions appear to add parameters to the one call to printf. The
argument to the switch statement is wrong (should be arg0-2, or the
switch values should be increased by 2).

[]{#Switch_cc} Switch\_cc
-------------------------

This is the Boomerang test from test/pentium/switch\_cc. It comes from
the same source code as the above, but was compiled with a Sun compiler.
The compiler has one call to printf in each case of the switch
statement. Decompiled output:

    08048978 Error! Jump destination is not a Global!
    main:
      ax = ax + -2;
      if (ax <= 5) goto loc_8048978;

      return _printf("Other!\n") - ax;

    loc_8048914:
      return _printf("Two!\n") - ax;

    loc_8048928:
      return _printf("Three!\n") - ax;

    loc_804893C:
      return _printf("Four!\n") - ax;

    loc_8048950:
      return _printf("Five!\n") - ax;

    loc_8048964:
      return _printf("Six!\n") - ax;

    loc_8048978:
      goto off_80489E8 + (ax * 4);

    loc_804897F:
      return _printf("Seven!\n") - ax;

The switch table is in the .rodata section, not in the .text section as
with switch\_gcc. This seems to be unexpected. It also seems confused by
the `sub eax, eax` instructions used to return 0.

[]{#Sumarray_O4} Sumarray-O4
----------------------------

This is the Boomerang test test/pentium/sumarray-O4. As the name
suggests, this test is compiled with the gcc compiler using -O4
optimisation. (Output for the same program compiled with no optimisation
is ironically less readable, because local variables are emitted as
`* (& var_4)`, and has more errors.) The original source code:

    int a[10] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
    int main() {
        int sum = 0;
        int i;
        for (i=0; i < 10; i++) {
            sum += a[i];
        }
        printf("Sum is %d\n", sum);
        return 0;
    }

Decompiled output:

    main:
      sp = sp & -16;
      dx = 0;
      ax = 0;
      cx = a;

    loc_804833C:
      dx = dx + (* (cx + (ax * 4)));
      ax = ax + 1;
      if (ax <= 9) goto loc_804833C;

      _printf("Sum is %d\n", dx);
      return 0;

This is not too bad. The array is not declared, and the index operation
is as per the X86 instructions. The for loop is not recovered. Other
than that, it\'s fairly readable.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 20 Mar 2003,
updated 20 Jul 2005.\
[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.DecompilerDesquirrTest moved from
Transform.DecompilationDesquirr on 20 Mar 2003 - 03:05 by
[MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Transform/DecompilerDesquirrTest?newweb=Transform&newtopic=DecompilationDesquirr&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
