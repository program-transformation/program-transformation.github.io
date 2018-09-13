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
    Page](http://www.program-transformation.org/edit/Transform/DNeliacExample72?t=1536826448)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DNeliacExample72)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DNeliacExample72)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DNeliacExample72?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DNeliacExample72?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/DNeliacExample72?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DNeliacExample72?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DNeliacExample72?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DNeliacExample72)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DNeliacExample72?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/DNeliacExample72?template=oopsmore&param1=1.2&param2=1.2)
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
DNeliac Example 72 {#dneliac-example-72 .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

*This page represents examples 72, 73, and 74 of Halstead\'s
\"Machine-Independent Computer Programming\".* *Comments in italics, as
well as the disassembly and Algol hand translation, have been added by*
[MikeVanEmmerik](MikeVanEmmerik){.twikiLink}.

      EXAMPLE 72.
      Address         ff  jkb  yyyyy              Ad.dress    ff   jkb   yyyyy
      00522           00  000  00000              00565       12   130   00130
      00523           65  000  00352              00566       10   030   00132
      00524           65  000  00211              00567       14   031   00000
      00525           16  030  00130              00570       61   000   00526
      00526           16  030  00131              00571       65   000   00346
      00527           16  030  00132              00572       12   500   00007
      00530           12  300  00000              00573       10   030   00130
      00531           10  030  00130              00574       27   515   00133
      00532           27  500  00051              00575       61   000   00541
      00533           61  000  00571              00576       72   500   00573
      00534           10  030  00130              00577       11   530   00130
      00535           27  500  00045              00600       61   000   00571
      00536           61  000  00571              00601       10   030   00130
      00537           65  000  00346              0060?       27   500   00004
      00540           61  000  00526              00603       61   000   00571
      00541           10  003  00000              00604       10   030   00130
      00542           27  700  00005              00605       27   500   00057
      00543           61  000  00553              00606       61   000   00571
      00544           10  030  00131              00607       10   030   00130
      00545           05  000  00003              00610       27   500   00047
      00546           14  030  00467              00611       61   000   00571
      00547           10  005  00000              00612       10   030   00130
      00550           26  030  00467              00613       27   500   00077
      00551           14  030  00131              00614       61   000   00571
      00552           61  000  00561              00615       10   030   00130
      00553           10  030  00132              00616       27   400   00042
      00554           05  000  00003              00617       61   000   00526
      00555           14  030  00467              00620       65   000   00346
      00556           10  005  00000              00621       10   030   00130
      00557           26  030  00467              00622       27   400   00042
      00560           14  030  00132              00623       61   000   00526
      00561           12  303  00001              00624       65   000   00265
      00562           10  003  00000              00625       65   000   00363
      00563           27  400  00017              00626       61   010   00522
      00564           61  000  00571              00627       00   000   00000

*Again, here is [MikeVanEmmerik](MikeVanEmmerik){.twikiLink}\'s hand
disassembly of the above:*

    00522 START:  .word   0
    00523         call    SUB_A
    00524         call    SUB_B
    00525         st      b,AA
    00526 ENT_A:  st      b,AB
    00527         st      b,AC
    00530         ld      b,#0           ; Why is j=3?
    00531         ld      q,AA
    00532         sub     <>,q,#00051    ; Subtract and skip if result not equal to 0
    00533         jmp     ENT_B
    00534         ld      q,AA
    00535         sub     <>,q,#00045
    00536         jmp     ENT_B
    00537         call    SUB_C
    00540         jmp     ENT_A
    00541 ENT_D:  ld      q,#0           ; Why is b=3?
    00542         sub     <,q,#5         ; subtract and skip if result < 0
    00543         jmp     ENT_F
    00544         ld      q,AB
    00545         shl     q,3
    00546         st      q,AD
    00547         ld      q,0(b)
    00550         add     q,AD
    00551         st      q,AB
    00552         jmp     ENT_E
    00553 ENT_F:  ld      q,AC
    00554         shl     q,#3
    00555         st      q,AD
    00556         ld      q,0(b)
    00557         add     q,AD
    00560         st      q,AC
    00561 ENT_E:  add     b,#1
    00562         ld      q,#0
    00563         sub     <,q,#00017      ; subtract and skip if result < 0?
    00564         jmp     ENT_B
    00565         ld      =,b,AB          ; why is j=1?
    00566         ld      q,AC
    00567         st      q,0(b)
    00570         jmp     ENT_A
    00571 ENT_B:  call    SUB_C
    00572         ld      b,#7            ; why is j=5?
    00573         ld      q,AA
    00574         sub     <>,q,AE(b)      ; ?
    00575         jmp     ENT_D
    00576         jmp     ?
    00577         ld      <>,a,AA         ; load a and skip if non zero
    00600         jmp     ENT_B
    00601         ld      q,AA
    00602         sub     <>,q,#4         ; subtract immediate 4 and skip if non zero
    00603         jmp     ENT_B
    00604         ld      q,AA
    00605         sub     <>,q,#00057
    00606         jmp     ENT_B
    00607         ld      q,AA
    00610         sub     <>,q,#00047
    00611         jmp     ENT_B
    00612         ld      q,AA
    00613         sub     <>,q,#00077
    00614         jmp     ENT_B
    00615         ld      q,AA
    00616         sub     =,q,#00042
    00617         jmp     ENT_A
    00620         call    SUB_C
    00621         ld      q,AA
    00622         sub     =,q,#00042
    00623         jmp     ENT_A
    00624         call    SUB_D
    00625         call    SUB_E
    00626         jmp     *START
    00627         .word   0

![ex73\_1.jpg](../pub/Transform/DNeliacExample72/ex73_1.jpg){width="600"
height="1105"}

*Here is [MikeVanEmmerik](MikeVanEmmerik){.twikiLink}\'s hand
translation to Algol:*

    integer procedure START();
    begin
        SUB A();
        SUB B();
        aa := 0;
    ENT A:
        ab := 0;
        ac := 0;
        k := 0;
        if aa-058 <> 0 ;
        else goto ENT B;
        if aa-045 <> 0 ;
        else goto ENT B;
        SUB C();
        goto ENT A;
    ENT D:
        if k-5 < 0 ;
        else goto ENT F;
        ad := ab * 2**3;
        ab := m + ad;
        goto ENT E;
    ENT F:
        ad := ac * 2**3;
        ac := m + ad;
    ENT E:
        k := k+1;
        if k - 017 = 0 ;
        else goto ENT B;
        i := ab;
        [i] := ac;
        goto ENT A;
    ENT B:
        SUB C();
        m := 7;
        for m := m step 1 until 0 do
            begin
                if aa - ae[m](0..14) <> 0 ;
                else goto ENT D;
            end;
        if aa <> 0 ;
        else goto ENT_B;
        if aa-4 <> 0 ;
        else goto ENT_B;
        if aa-057 <> 0 ;
        else goto ENT_B;
        if aa-047 <> 0 ;
        else goto ENT_B;
        if aa-077 <> 0 ;
        else goto ENT_B;
        if aa-042 = 0 ;
        else goto ENT_A;
        SUB C();
        if aa-042 = 0 ;
        else goto ENT_A;
        SUB D();
        SUB E();
    end

    EXAMPLE 74.
    SUB A  0 352
    SUB B  0 211
    SUB C  0 346
    ENT A  0 526
    ENT B  0 571
    SUB D  0 265
    SUB E  0 363
    ENT C  0 522
    ENT D  0 541
    ENT E  0 561
    ENT F  0 553
    START  0 522
    AA    3 130
    AB    3 131
    AC    3 132
    AD    3 467
    AE    3 133

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
