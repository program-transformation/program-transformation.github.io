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
    Page](http://www.program-transformation.org/edit/Transform/DecompilerE2cTest?t=1536826464)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilerE2cTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilerE2cTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilerE2cTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilerE2cTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Transform/DecompilerE2cTest?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/DecompilerE2cTest?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/DecompilerE2cTest?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/DecompilerE2cTest?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Transform/DecompilerE2cTest?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DecompilerE2cTest?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilerE2cTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilerE2cTest?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilerE2cTest?template=oopsmore&param1=1.5&param2=1.5)
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
Decompiler E2 c Test {#decompiler-e2-c-test .twikiTopicTitle}
====================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

[]{#Exe_2_C_DOS_286_Decompiler_Tests} Exe-2-C DOS/286 Decompiler Tests
======================================================================

This is the beta version of an experimental decompiler. The tests are
from
[test.zip](http://www.itee.uq.edu.au/~cristina/dcc/distribution/test.zip)
in the [dcc](http://www.itee.uq.edu.au/~cristina/dcc) distribution.

::: {.twikiToc}
-   [Exe-2-C DOS/286 Decompiler
    Tests](DecompilerE2cTest#Exe_2_C_DOS_286_Decompiler_Tests)
    -   [Strlen](DecompilerE2cTest#Strlen)
    -   [Fibo](DecompilerE2cTest#Fibo)
:::

[]{#Strlen} Strlen
------------------

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

This disassembled as follows (amongst much other code):

    proc_10         proc    near
                    push    SI                      
                    mov     SI,194h                 
                    push    SI                      
                    call    near ptr proc_11        
                    pop     CX                      
                    pop     SI                      
                    retn                            
    proc_10         endp

    proc_11         proc    near
                    push    BP                      
                    mov     BP,SP                   
                    push    SI                      
                    xor     SI,SI                   
                    jmp     short loc_12            
    loc_11:         ; N-Ref=1
                    inc     SI                      
    loc_12:         ; N-Ref=1
                    mov     BX,Word Ptr [BP+4]      
                    inc     Word Ptr [BP+4]         
                    cmp     Byte Ptr [BX],0         
                    jne     loc_11                  ; Jump if not equal ( != )
                    mov     AX,SI                   
                    jmp     short loc_13            
    loc_13:         ; N-Ref=1
                    pop     SI                      
                    pop     BP                      
                    retn                            
    proc_11         endp

The output was as follows:

    /****************************************************************************/
                    near proc_10()
    /****************************************************************************/
    {
    register char *reg1 ;

        push(0x194);
        proc_11();
        cx = pop();
    }
    /****************************************************************************/
                    near proc_11(int   arg0)
    /****************************************************************************/
    {
    register char *reg1 ;

        reg1 = 0;
        while(bx = arg0, ++arg0, *bx != 0)   
            ++reg1;
        ax = reg1;
    }

It analysed that proc\_11 takes an int argument (actually a char\*), but
it did not pass the actual argument (0x194, the pointer to the string).
It has guessed incorrectly that reg1 in proc11 is a char\*. It may have
been able to do better if main made use of the return value.

There is nothing to indicate the size of \*bx (in fact, 8 bits), so this
would never compile. The while loop does look good, though.

[]{#Fibo} Fibo
--------------

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

    proc_11         proc    near
                    push    BP                      
                    mov     BP,SP                   
                    push    SI                      
                    mov     SI,Word Ptr [BP+4]      
                    cmp     SI,+2                   
                    jle     loc_13                  ; Jump if not greater ( <= )
                    mov     AX,SI                   
                    dec     AX                      
                    push    AX                      
                    call    near ptr proc_11        
                    pop     CX                      
                    push    AX                      
                    mov     AX,SI                   
                    add     AX,0FFFEh               
                    push    AX                      
                    call    near ptr proc_11        
                    pop     CX                      
                    mov     DX,AX                   
                    pop     AX                      
                    add     AX,DX                   
                    jmp     short loc_14            

                    dw      5EBh
    loc_13:         ; N-Ref=1
                    mov     AX,1                    
                    jmp     short loc_14            
    loc_14:         ; N-Ref=2
                    pop     SI                      
                    pop     BP                      
                    retn                            
    proc_11         endp

It correctly did not attempt to disassemble the unreachable code before
loc\_13.

The decompiled output is as follows. Again, main is proc\_10; proc\_11
is fib:

    /****************************************************************************/
                    near proc_10()
    /****************************************************************************/
    {
    register char *reg1 ;
    register char *reg2 ;
    char  *loc0;
    char  *loc1;

            push(0x194);
            proc_41();
            cx = pop();
            ax = &loc0;
            push(ax);
            push(0x1B1)
            proc_55();
            cx = pop();
            cx = pop();
            DELETE: reg1 = 1;
            si = 1;  /*PCH : RM_Table_init*/
            while(reg1 <= loc0)   {
                    push(0x1B4);
                    proc_41();
                    cx = pop();
                    ax = &loc1;
                    push(ax);
                    push(0x1C3);
                    proc_55();
                    cx = pop();
                    cx = pop();
                    push(loc1);
                    proc_11();
                    cx = pop();
                    push(ax);
                    push(loc1);
                    push(0x1C6);
                    proc_41();
                    sp = sp + 6;
                    ++reg1;
            }
            ax = 0;
            push(ax);
            proc_13();
            cx = pop();
    }

    /****************************************************************************/
                    near proc_11(int   arg0)
    /****************************************************************************/
    {
    register char *reg1 ;

            reg1 = arg0;
            if(reg1 > 2)   {
                    ax = reg1;
                    --ax;
                    push(ax);
                    proc_11();
                    cx = pop();
                    push(ax);
                    ax = reg1;
                    ax = ax +  - 2;
                    push(ax);
                    proc_11();
                    cx = pop();
                    dx = ax;
                    ax = pop();
                    ax = ax + dx;
            }
            else   {
                    DELETE: ax = 1;
                    ax = 1;  /*PCH : RM_Table_init*/
                    return;
            }
    }

Here the \"instruction by instruction\" nature of the decompilation is
evident. Forward substitution (necessitating data flow analysis to
ensure safety) would merge the individual instruction results into more
readable and complex expressions. The condition codes (status flags)
have been successfully removed.

No attempt has been made to determine the return value of function fib
(here proc\_11). No attempt is made to recognise the library functions
`printf` and `scanf`. In proc\_10, the decompiler seems to forget
whether register `SI` is represented by variable `si` or variable
`reg1`.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Transform.DecompilerE2cTest moved from Transform.DecompilationE2cTest
on 20 Mar 2003 - 03:08 by
[MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Transform/DecompilerE2cTest?newweb=Transform&newtopic=DecompilationE2cTest&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
