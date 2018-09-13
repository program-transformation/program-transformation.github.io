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
    Page](http://www.program-transformation.org/edit/Transform/DecompilerAndromedaTest?t=1536826462)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilerAndromedaTest)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilerAndromedaTest)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilerAndromedaTest?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilerAndromedaTest?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/DecompilerAndromedaTest?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilerAndromedaTest)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilerAndromedaTest?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilerAndromedaTest?template=oopsmore&param1=1.1&param2=1.1)
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
Decompiler Andromeda Test {#decompiler-andromeda-test .twikiTopicTitle}
=========================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

The Andromeda Decompiler is not available to the public at present, so
the only example of its use is usually limited to the very impressive
demo program. I asked the author to compile the switch test program;
here is the result:

    void sub_401080(DWORD arg_4)
    {
       DWORD   var_c;
       sub_401440();
       __main();
       switch (arg_4)
       {
       case 7:
          var_c = "Seven!";
          goto loc_4010D0;
       case 6:
          var_c = "Six!";
          goto loc_4010D0;
       case 5:
          var_c = "Five!";
          goto loc_4010D0;
       case 4:
          var_c = "Four!";
          goto loc_4010D0;
       case 3:
          var_c = "Three!";
          goto loc_4010D0;
       case 2:
          var_c = "Two!";
    loc_4010D0:
          puts((void *)var_c);
          return;
       }
       var_c = "Other!";
       goto loc_4010D0;
    }//sub_401080(:[1])

This will compile with little effort, and looks like it will run
correctly. Obviously, the goto statements are unfortunate. However, this
is possibly because the author has not tested before on gcc-compiled
input programs.

I\'m not sure where the binary for this program came from; it is in a
file called `switch_gcc.dc`. To give some idea of the original binary,
this is the assembler view:

    sub_401080   proc near
      mov    [eax], ebp
      mov    eax, 0
      mov    ebp, esp
      sub    esp, 8
      and    esp, 0FFFFFFF0h
      mov    [eax-4], ebx
      mov    ebx, [eax+8]
      call   sub_401440
      call   __main
      cmp    ebx, 7
      ja     loc_4010E0
      T32 = ebx * 4, T32 = &off_4010A8 + T32, (*T32)
    loc_40110D:
      mov    dword ptr [eax], offset aSeven
      jmp    loc_4010D0

    loc_40110D4:
      mov    dword ptr [eax], offset aSix
      jmp    loc_4010D0
    ...
    loc_4010C8:
      mov    fdword ptr [eax], offset aTwo
    loc_4010D0:
      call   puts
      mov    ebx, [eax-4]
      mov    eax, 0
      mov    esp, ebp
      mov    ebp, [eax]
      ret

    loc_4010E0:
      mov    dword ptr [eax], offset aOther
      jmp    loc_4010D0
    sub_401080   endp

This assembler code is like nothing I\'ve seen; I suspect that esp is
being displayed as eax and possibly some instructions are displayed out
of sequence. This was from version 0.62; unfortunately the `.dc` file
won\'t read in later versions of the GUI.

It\'s a real shame that this decompiler doesn\'t seem to have progressed
since May 2005.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 24 Mar 2007\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
