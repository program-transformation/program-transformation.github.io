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
    Page](http://www.program-transformation.org/edit/Transform/AnatomizerDecompilerTest?t=1536826296)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/AnatomizerDecompilerTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/AnatomizerDecompilerTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/AnatomizerDecompilerTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/AnatomizerDecompilerTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/AnatomizerDecompilerTest?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/AnatomizerDecompilerTest?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/AnatomizerDecompilerTest?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/AnatomizerDecompilerTest?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/AnatomizerDecompilerTest?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/AnatomizerDecompilerTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/AnatomizerDecompilerTest?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/AnatomizerDecompilerTest?template=oopsmore&param1=1.3&param2=1.3)
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
Anatomizer Decompiler Test {#anatomizer-decompiler-test .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

::: {.twikiToc}
-   [Hello\_release](AnatomizerDecompilerTest#Hello_release)
-   [switch\_gcc.exe](AnatomizerDecompilerTest#switch_gcc_exe)
-   [Wink.exe](AnatomizerDecompilerTest#Wink_exe)
-   [Anatomizer hello world
    example](AnatomizerDecompilerTest#Anatomizer_hello_world_example)
:::

[]{#Hello_release} Hello\_release
---------------------------------

From Boomerang\'s test/windows/hello\_release.exe (I had to force the
entry point):

Original source code:

    LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
    {
            int wmId, wmEvent;
            PAINTSTRUCT ps;
            HDC hdc;
            TCHAR szHello[MAX_LOADSTRING];
            LoadString(hInst, IDS_HELLO, szHello, MAX_LOADSTRING);

            switch (message)
            {
                    case WM_COMMAND:
                            wmId    = LOWORD(wParam);
                            wmEvent = HIWORD(wParam);
                            // Parse the menu selections:
                            switch (wmId)
                            {
                                    case IDM_ABOUT:
                                       DialogBox(hInst, (LPCTSTR)IDD_ABOUTBOX, hWnd, (DLGPROC)About);
                                       break;
                                    case IDM_EXIT:
                                       DestroyWindow(hWnd);
                                       break;
                                    default:
                                       return DefWindowProc(hWnd, message, wParam, lParam);
                            }
                            break;
                    case WM_PAINT:
                            hdc = BeginPaint(hWnd, &ps);
                            // TODO: Add any drawing code here...
                            RECT rt;
                            GetClientRect(hWnd, &rt);
                            DrawText(hdc, szHello, strlen(szHello), &rt, DT_CENTER);   # Note (1)
                            EndPaint(hWnd, &ps);
                            break;
                    case WM_DESTROY:
                            PostQuitMessage(0);
                            break;
                    default:
                            return DefWindowProc(hWnd, message, wParam, lParam);
       }
       return 0;
    }

Disassembly:

      4011b0:       8b 0d 58 55 40 00       mov    0x405558,%ecx
      4011b6:       81 ec b4 00 00 00       sub    $0xb4,%esp
      4011bc:       8d 44 24 50             lea    0x50(%esp),%eax
      4011c0:       6a 64                   push   $0x64
      4011c2:       50                      push   %eax
      4011c3:       6a 6a                   push   $0x6a
      4011c5:       51                      push   %ecx
      4011c6:       ff 15 d0 40 40 00       call   *0x4040d0
      4011cc:       8b 8c 24 bc 00 00 00    mov    0xbc(%esp),%ecx
      4011d3:       8b c1                   mov    %ecx,%eax
      4011d5:       83 e8 02                sub    $0x2,%eax
      4011d8:       0f 84 14 01 00 00       je     0x4012f2
      4011de:       83 e8 0d                sub    $0xd,%eax
      4011e1:       0f 84 ab 00 00 00       je     0x401292
      4011e7:       2d 02 01 00 00          sub    $0x102,%eax
      4011ec:       74 28                   je     0x401216
      4011ee:       8b 94 24 c4 00 00 00    mov    0xc4(%esp),%edx
      4011f5:       8b 84 24 c0 00 00 00    mov    0xc0(%esp),%eax
      4011fc:       52                      push   %edx
      4011fd:       50                      push   %eax
      4011fe:       51                      push   %ecx
      4011ff:       8b 8c 24 c4 00 00 00    mov    0xc4(%esp),%ecx
      401206:       51                      push   %ecx
      401207:       ff 15 98 40 40 00       call   *0x404098
      40120d:       81 c4 b4 00 00 00       add    $0xb4,%esp
      401213:       c2 10 00                ret    $0x10
      401216:       8b 8c 24 c0 00 00 00    mov    0xc0(%esp),%ecx
      40121d:       8b c1                   mov    %ecx,%eax
      40121f:       25 ff ff 00 00          and    $0xffff,%eax
      401224:       83 e8 68                sub    $0x68,%eax
      401227:       74 41                   je     0x40126a
      401229:       48                      dec    %eax
      40122a:       74 25                   je     0x401251
      40122c:       8b 94 24 c4 00 00 00    mov    0xc4(%esp),%edx
      401233:       8b 84 24 b8 00 00 00    mov    0xb8(%esp),%eax
      40123a:       52                      push   %edx
      40123b:       51                      push   %ecx
      40123c:       68 11 01 00 00          push   $0x111
      401241:       50                      push   %eax
      401242:       ff 15 98 40 40 00       call   *0x404098
      401248:       81 c4 b4 00 00 00       add    $0xb4,%esp
      40124e:       c2 10 00                ret    $0x10
      401251:       8b 8c 24 b8 00 00 00    mov    0xb8(%esp),%ecx
      401258:       51                      push   %ecx
      401259:       ff 15 9c 40 40 00       call   *0x40409c
      40125f:       33 c0                   xor    %eax,%eax
      401261:       81 c4 b4 00 00 00       add    $0xb4,%esp
      401267:       c2 10 00                ret    $0x10
      40126a:       8b 94 24 b8 00 00 00    mov    0xb8(%esp),%edx
      401271:       a1 58 55 40 00          mov    0x405558,%eax
      401276:       6a 00                   push   $0x0
      401278:       68 10 13 40 00          push   $0x401310
      40127d:       52                      push   %edx
      40127e:       6a 67                   push   $0x67
      401280:       50                      push   %eax
      401281:       ff 15 a0 40 40 00       call   *0x4040a0
      401287:       33 c0                   xor    %eax,%eax
      401289:       81 c4 b4 00 00 00       add    $0xb4,%esp
      40128f:       c2 10 00                ret    $0x10
      401292:       53                      push   %ebx
      401293:       56                      push   %esi
      401294:       8b b4 24 c0 00 00 00    mov    0xc0(%esp),%esi
      40129b:       8d 4c 24 18             lea    0x18(%esp),%ecx
      40129f:       57                      push   %edi
      4012a0:       51                      push   %ecx
      4012a1:       56                      push   %esi
      4012a2:       ff 15 a4 40 40 00       call   *0x4040a4
      4012a8:       8d 54 24 0c             lea    0xc(%esp),%edx
      4012ac:       8b d8                   mov    %eax,%ebx
      4012ae:       52                      push   %edx
      4012af:       56                      push   %esi
      4012b0:       ff 15 a8 40 40 00       call   *0x4040a8
      4012b6:       8d 44 24 0c             lea    0xc(%esp),%eax
      4012ba:       6a 01                   push   $0x1
      4012bc:       50                      push   %eax
      4012bd:       8d 7c 24 64             lea    0x64(%esp),%edi
      4012c1:       83 c9 ff                or     $0xffffffff,%ecx
      4012c4:       33 c0                   xor    %eax,%eax
      4012c6:       f2 ae                   repnz scas %es:(%edi),%al     # Note (1)
      4012c8:       f7 d1                   not    %ecx
      4012ca:       49                      dec    %ecx
      4012cb:       51                      push   %ecx
      4012cc:       8d 4c 24 68             lea    0x68(%esp),%ecx
      4012d0:       51                      push   %ecx
      4012d1:       53                      push   %ebx
      4012d2:       ff 15 ac 40 40 00       call   *0x4040ac
      4012d8:       8d 54 24 1c             lea    0x1c(%esp),%edx
      4012dc:       52                      push   %edx
      4012dd:       56                      push   %esi
      4012de:       ff 15 b0 40 40 00       call   *0x4040b0
      4012e4:       5f                      pop    %edi
      4012e5:       5e                      pop    %esi
      4012e6:       5b                      pop    %ebx
      4012e7:       33 c0                   xor    %eax,%eax
      4012e9:       81 c4 b4 00 00 00       add    $0xb4,%esp
      4012ef:       c2 10 00                ret    $0x10
      4012f2:       6a 00                   push   $0x0
      4012f4:       ff 15 b4 40 40 00       call   *0x4040b4
      4012fa:       33 c0                   xor    %eax,%eax
      4012fc:       81 c4 b4 00 00 00       add    $0xb4,%esp
      401302:       c2 10 00                ret    $0x10

Anatomizer\'s decompiled output:

    long Main(long arg1, void arg2, long arg3, long arg4)
    /* 004011B0 - 00401304
     * Size : 341 ( 0x00000155 )
     * Takes 16 Bytes parameters.
     * Pascal calling convention.
     * Have 180Byte(s) local variable(s).
     */
    {
        void loc1; /* ESP -180 */
        void loc2; /* ESP -164 */
        void loc3; /* ESP -100 */
        register long loc4; /* ECX */
        register long loc5; /* EAX */
        register long loc6; /* ESI */
        register long loc7; /* EBX */

        (void) LoadStringA(var00405558, 106, &loc3, 100);
        loc4 = arg2;
        loc5 = loc4;
        loc5 = loc5 - 2;

        if (loc5 != 0) {
            loc5 = loc5 - 13;

            if (loc5 != 0) {
                loc5 = loc5 - 258;

                if (loc5 != 0) {
                    loc5 = DefWindowProcA(arg1, loc4, arg3, arg4);
                    return (loc5);
                }
                loc4 = arg3;
                loc5 = loc4 & 0x0000FFFF;
                loc5 = loc5 - 104;

                if (loc5 != 0) {
                    loc5 = loc5 - 1;

                    if (loc5 != 0) {
                        loc5 = DefWindowProcA(arg1, 273, loc4, arg4);
                        return (loc5);
                    }
                    (void) DestroyWindow(arg1);
                    return (0);
                }
                else {
                    (void) DialogBoxParamA(var00405558, 103, arg1, &var00401310, 0);
                    return (0);
                }
            }
            else {
                loc6 = arg1;
                loc7 = BeginPaint(loc6, &loc2);
                (void) GetClientRect(loc6, &loc1);
                (void) DrawTextA(loc7, &loc3, strlen(&loc3), &loc1, 1);    # Note (1)
                (void) EndPaint(loc6, &loc2);
                return (0);
            }
        }
        else {
            (void) PostQuitMessage(0);
            return (0);
        }
    }

Note (1): The string scan instruction at 0x4012c6 is converted cleanly
into a strlen call (the third parameter to `DrawTextA`); this is quite
impressive.

[]{#switch_gcc_exe} switch\_gcc.exe
-----------------------------------

The following test is from Boomerang\'s test/windows/switch\_gcc.exe.

Original source code:

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

Disassembly:

      401080:       55                      push   %ebp
      401081:       31 c0                   xor    %eax,%eax
      401083:       89 e5                   mov    %esp,%ebp
      401085:       83 ec 08                sub    $0x8,%esp
      401088:       83 e4 f0                and    $0xfffffff0,%esp
      40108b:       89 5d fc                mov    %ebx,0xfffffffc(%ebp)
      40108e:       8b 5d 08                mov    0x8(%ebp),%ebx
      401091:       e8 aa 03 00 00          call   401440 <___chkstk>
      401096:       e8 35 04 00 00          call   4014d0 <___main>
      40109b:       83 fb 07                cmp    $0x7,%ebx
      40109e:       77 40                   ja     4010e0 <_main+0x60>
      4010a0:       ff 24 9d a8 10 40 00    jmp    *0x4010a8(,%ebx,4)
      4010a7:       90                      nop

      4010a8:       e0104000 e0104000 c8104000 e9104000 f2104000 fb104000 
      4010c0:       04114000 0d114000 

      4010c8:       c7 04 24 50 10 40 00    movl   $0x401050,(%esp)
      4010cf:       90                      nop
      4010d0:       e8 0b 04 00 00          call   4014e0 <_puts>
      4010d5:       8b 5d fc                mov    0xfffffffc(%ebp),%ebx
      4010d8:       31 c0                   xor    %eax,%eax
      4010da:       89 ec                   mov    %ebp,%esp
      4010dc:       5d                      pop    %ebp
      4010dd:       c3                      ret
      4010de:       89 f6                   mov    %esi,%esi
      4010e0:       c7 04 24 55 10 40 00    movl   $0x401055,(%esp)
      4010e7:       eb e7                   jmp    4010d0 <_main+0x50>
      4010e9:       c7 04 24 5c 10 40 00    movl   $0x40105c,(%esp)
      4010f0:       eb de                   jmp    4010d0 <_main+0x50>
      4010f2:       c7 04 24 63 10 40 00    movl   $0x401063,(%esp)
      4010f9:       eb d5                   jmp    4010d0 <_main+0x50>
      4010fb:       c7 04 24 69 10 40 00    movl   $0x401069,(%esp)
      401102:       eb cc                   jmp    4010d0 <_main+0x50>
      401104:       c7 04 24 6f 10 40 00    movl   $0x40106f,(%esp)
      40110b:       eb c3                   jmp    4010d0 <_main+0x50>
      40110d:       c7 04 24 74 10 40 00    movl   $0x401074,(%esp)
      401114:       eb ba                   jmp    4010d0 <_main+0x50>

Anatomizer Decompiler decompiled output (entry point forced):

    long Main()
    /* 00401080 - 00401115
     * Size : 150 ( 0x00000096 )
     * Takes no parameters.
     * Stack unresolve.
     * Have 8Byte(s) local variable(s).
     */
    {
        void loc1; /* ESP -12 */
        void loc2; /* ESP 0 */
        register long loc3; /* EBP */
        register long loc4; /* EBX */
        register long loc5; /* ESP */

        *(loc3 - 4) = loc4;
        loc4 = *(loc3 + 8);
        (void) proc_0002(0, loc5 & -16);
        (void) Red___main();

        if (loc4 <= 7) {

            switch (loc4) {
            case 0:
            case 1:
    L1:
                *loc5 = &var00401055;
                break;

            case 2:
                *loc5 = &var00401050;
                break;

            case 3:
                *loc5 = &var0040105C;
                break;

            case 4:
                *loc5 = &var00401063;
                break;

            case 5:
                *loc5 = &var00401069;
                break;

            case 6:
                *loc5 = &var0040106F;
                break;

            case 7:
                *loc5 = &var00401074;
                break;

            } /* end of switch */
        }
        else {
            goto L1;
        }
        (void) Red_puts();
        loc4 = *(loc3 - 4);
        return (0);
    }

Perhaps \"Stack Unresolve\" results from forcing the entry point. (This
is a CygWin executable; the only reference to this main function is a
move indirect on the stack pointer; it is not called directly). The
switch statement is handled reasonably well, apart from the default
statement. The parameter to `puts` is missing. No strings are resolved
as a result.

[]{#Wink_exe} Wink.exe
----------------------

From a 2MB open source executable:

      48d6e8:       56                      push   %esi
      48d6e9:       57                      push   %edi
      48d6ea:       8b f1                   mov    %ecx,%esi
      48d6ec:       33 ff                   xor    %edi,%edi
      48d6ee:       39 7e 04                cmp    %edi,0x4(%esi)
      48d6f1:       76 24                   jbe    0x48d717
      48d6f3:       8b 46 08                mov    0x8(%esi),%eax
      48d6f6:       8b 04 b8                mov    (%eax,%edi,4),%eax
      48d6f9:       83 e8 0c                sub    $0xc,%eax
      48d6fc:       8b 08                   mov    (%eax),%ecx
      48d6fe:       83 f9 ff                cmp    $0xffffffff,%ecx
      48d701:       74 0e                   je     0x48d711
      48d703:       49                      dec    %ecx
      48d704:       85 c9                   test   %ecx,%ecx
      48d706:       89 08                   mov    %ecx,(%eax)
      48d708:       75 07                   jne    0x48d711
      48d70a:       50                      push   %eax
      48d70b:       e8 fc f9 0e 00          call   0x57d10c
      48d710:       59                      pop    %ecx
      48d711:       47                      inc    %edi
      48d712:       3b 7e 04                cmp    0x4(%esi),%edi
      48d715:       72 dc                   jb     0x48d6f3
      48d717:       5f                      pop    %edi
      48d718:       5e                      pop    %esi
      48d719:       c3                      ret

    void proc_0019()
    /* 0048D6E8 - 0048D719
     * Size : 50 ( 0x00000032 )
     * Takes no parameters.
     * Call from proc_0020 ,proc_0022 ,proc_0021.
     */
    {
        register long loc1; /* ESI */
        register long loc2; /* ECX */
        register long loc3; /* EDI */
        register long loc4; /* EAX */

        loc1 = loc2;
        loc3 = 0;

        if (*(loc1 + 4) <= loc3) {
            return;
        }

        do {
            loc4 = *(*(loc1 + 8) + (loc3 * 4)) - 12;
            loc2 = *loc4;

            if (loc2 != -1) {
                loc2 = loc2 - 1;
                *loc4 = loc2;

                if (loc2 == 0) {
                    (void) proc_0046();
                }
            }
            loc3 = loc3 + 1;
        } while (loc3 < *(loc1 + 4));

        return;
    }

Note that no parameters were found, even though plainly ecx is used
before being defined. In the first conditional statement, the zero value
in edi is not propagated into the predicate. The while statement is
clearly using an array, which remains as a memory expression.

In other cases, it is obvious that no floating point instructions are
handled, and overlapped registers (e.g. bl and ebx) are treaded as
separate registers.

[]{#Anatomizer_hello_world_example} Anatomizer hello world example
------------------------------------------------------------------

The above example is similar to one I found on the Anatomizer web page;
both come from the MSVC C++ Wizard, and both implement the commonly used
\"hello world\" program.

-   [Original source
    code](http://jdi.at.infoseek.co.jp/japanese/samplecpp.txt) (with
    Japanese comments)
-   [Disassembled
    code](http://jdi.at.infoseek.co.jp/japanese/sampled.txt)
-   [Anatomizer
    output](http://jdi.at.infoseek.co.jp/japanese/samplec.txt)
    (unfortunately, WndProc is not visible, as the author did not force
    an entry point).
-   As above, [all on one
    page](http://jdi.at.infoseek.co.jp/japanese/examin.plg) (may require
    Internet Explorer to view as intended).

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 01 Aug 2005\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
