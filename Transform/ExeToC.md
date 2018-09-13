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
    Page](http://www.program-transformation.org/edit/Transform/ExeToC?t=1536826477)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/ExeToC)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/ExeToC)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/ExeToC?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/ExeToC?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/ExeToC?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/ExeToC)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/ExeToC?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/ExeToC?template=oopsmore&param1=1.1&param2=1.1)
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
Exe To C {#exe-to-c .twikiTopicTitle}
========

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

<http://sourceforge.net/projects/exetoc>

This is a decompiler for Win32 executable files, hosted on Windows. For
a first release, it\'s quite good. It seems to have reasonable dataflow
analysis, removal of unused statements, it recognises commonly used
Windows functions and seems to get the parameters right, and emits most
high level C statements such as if/switch/do/while. Here is a simple
example from his own test program:

    sub_401000  proc

         401000 PUSH   +04
         401002 PUSH   +03
         401004 PUSH   00408040
         401009 CALL   printf
         40100e ADD    ESP,+0C
         401011 RET
    sub_401000  endp

which after a few clicks transforms into:

    DWORD sub_401000 ()
    {
        return printf ("hello %d and %d",3,4 );
    }

It won\'t load certain Windows/PE programs, and occasionally fails, but
it usually displays a message box before editing. Plus, of course, you
can fix it yourself since source code is available.

After 100 steps, main transforms into:

    DWORD main (bit32 a_4, bit32 a_10 )
    {
        bit32 ESI ;
        bit32 EDI ;
        bit32 EBX ;
        bit32 EBP ;
        HINSTANCE ESI_1 ;
        HACCEL ESI_2 ;
        bit32 EAX_5 ;
        tagMSG  v_1c ;

        sub_401020 () = sub_401020 ();
        Sleep (sub_401020 ());
        ESI_1 = a_4;
        LoadStringA (ESI_1,(UINT)0x67,"",(int)100 );
        LoadStringA (ESI_1,(UINT)0x6d,"",(int)100 );
        sub_401100 ();
        EAX_5  = sub_401190 ();
        if (EAX_5  == 0 )
        {
            return EAX_5;
        }
        ESI_2  = LoadAcceleratorsA (ESI_1,(LPCSTR)0x6d );
        if (GetMessageA (&v_1c.hwnd,(HWND)NULL,(UINT)0,(UINT)0 ) != 0 )
        {
            do
            {
                if (TranslateAcceleratorA (v_1c.hwnd,ESI_2,&v_1c.hwnd ) == 0 )
                {
                    TranslateMessage (&v_1c.hwnd );
                    DispatchMessageA (&v_1c.hwnd );
                }
            }
            while (GetMessageA (&v_1c.hwnd,(HWND)NULL,(UINT)0,(UINT)0 ) != 0 );
        }
        return v_1c.wParam;
    }

As you can see, variables are declared, there is type analysis,
structures appear to be handled, parameters and returns are mostly
handled. I analysed sub\_401100, and it takes one parameter and returns
a value (but the return value is not used). When I returned to main,
however, I could not get it to recognise this. Even when I analyse
sub\_401100 first, it doesn\'t seem to use the information is has about
the child procedure.

All in all, an excellent first release.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 04 Aug 2005\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
