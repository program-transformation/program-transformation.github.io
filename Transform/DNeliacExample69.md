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
    Page](http://www.program-transformation.org/edit/Transform/DNeliacExample69?t=1536826448)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DNeliacExample69)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DNeliacExample69)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DNeliacExample69?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DNeliacExample69?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/DNeliacExample69?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DNeliacExample69)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DNeliacExample69?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/DNeliacExample69?template=oopsmore&param1=1.1&param2=1.1)
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
DNeliac Example 69 {#dneliac-example-69 .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

*This page represents examples 69, 70, and 71 of Halstead\'s
\"Machine-Independent Computer Programming\".* *Comments in italics, as
well as the disassembly and Algol hand translation, have been added by*
[MikeVanEmmerik](MikeVanEmmerik){.twikiLink}.

      EXAMPLE 69.
      Address        ff  jkb  yyyyy           Address   ff  jkb  yyyyy
      10100          00  000  00000           10142     07  000  00036
      10101          00  000  00000           10143     03  000  00036
      10102          00  000  00000           10144     23  030  10106
      10103          00  000  00000           10145     14  030  10107
      10104          00  000  00000           10146     61  010  10131
      10105          00  000  00000           10147     10  030  10103
      10106          00  000  00000           10150     26  030  10100
      10107          00  000  00000           10151     22  030  10106
      10110          00  000  00000           10152     14  030  10107
      10111          00  000  00000           10153     10  030  10100
      10112          00  000  00000           10154     27  630  10103
      10113          00  000  00000           I0155     65  000  10113
      10114          10  030  10103           10156     11  030  10100
      10115          35  030  10100           10157     10  030  10106
      10116          61  010  10113           10160     27  000  00001
      10117          00  000  00000           10161     04  430  10103
      10120          10  000  00005           10162     61  000  10165
      10121          26  030  10100           10163     65  000  10117
      10122          27  730  10106           10164     61  000  10166
      10123          61  000  10126           10165     65  000  10131
      10124          65  000  10113           10166     61  000  10167
      10125          61  000  10130           10167     12  100  00000
      10126          10  030  10103           10170     10  000  00170
      10127          34  030  10100           10171     40  031  10103
      10130          61  010  10117           10172     07  000  00073
      10131          00  000  00000           10173     41  031  10100
      10132          10  030  10106           10174     07  000  00072
      10133          26  030  10103           10175     14  031  10107
      10134          07  000  00036           10176     71  100  00003
      10135          03  000  00036           10177     61  000  10170
      10136          23  030  10106           10200     10  030  10103
      10137          26  030  10107           10201     14  030  10106
      10140          22  030  10100           10202     61  400  10000
      10141          26  030  10103

*The above is obviously quite hard to read. Here is my attempt at
disassembling it:*

    10100 AB:     .word   0,0,0
    10103 AA:     .word   0,0,0
    10106 AC:     .word   0
    10107 AD:     .word   0,0,0
    10112         .word   0
    10113 SUB_B:  .word   0            ; Space for return address
    10114         ld      q,AA
    10115         sub_st  q,AB         ; Subtract and store
    10116         jmp     *SUBC        ; Jump indirect on return address
    10117 SUB_A:  .word   0
    10120         ld      q,#5
    10121         add     q,AB
    10122         sub     <,q,AC       ; Subtract and skip next instruction
                                       ; if result < 0
    10123         jmp     ENT_D
    10124         call    SUB_B
    10125         jmp     SUB_A        ; Call SUB_A then return
    10126 ENT_D:  ld      q,AA
    10127         add_st  q,AB         ; Add and store
    10130 ENT_C:  jmp     *SUB_A       ; return from SUB_A
    10131 SUB_C:  .word   0
    10132         ld      q,AC
    10133         add     q,AA
    ; Note: registers on the Univac M460 are 30 bits
    10134         shl     aq,#30       ; shift left the a and q registers
    10135         shr     aq,#30       ; shift right aq
    10136         div     AC
    10137         add     q,AD
    10140         mul     AB
    10141         add     q,AA
    10142         shl     aq,#30
    10143         shr     aq,#30
    10144         div     AC
    10145         st      q,AD
    10146         jmp     *SUBC         ; return

    10147 START:  ld      q,AA          ; note no return address storage
    10150         add     q,AB
    10151         mul     AC
    10152         st      q,AD
    10153         ld      q,AB
    10154         sub     >=,q,AA       ; subtract, skip if result >= 0
    10155         call    SUB_B
    10156         ld      a,AB
    10157         ld      q,AC
    10160         sub     q,#1
    10161         cmp     aq,AA         ; skip if a < OP <= q
    10162         jmp     ENT_E
    10163         call    SUB_A
    10164         jmp     ENT_A
    10165 ENT_E:  call    SUB_C
    10166 ENT_A:  jmp     ENT_B
    10167 ENT_B:  ld      b,#0           ; don't know why j=1
    10170 @1:     ld      q,#120
    10171         ld      aq,AA(b)       ; "enter logical product"
    10172         shl     aq,#59
    10173         add     aq,AB(b)
    10174         shl     aq,#58
    10175         st      q,AD(b)
    10176         cmp     =,b,#2         ; compare b with 2 and skip if equal?
    10177         jmp     @1
    10200         ld      q,AA
    10201         st      q,AC
    10202         halt

The program of Example 69 was then accepted by the Decompiler of
Appendix D, which found all of the absolute addresses used as nouns or
verbs, and assigned arbitrary names to them. The program logic itself
was then decoded into the equivalent Neliac statements, as shown in
Example 70.

![ex70\_1.jpg](../pub/Transform/DNeliacExample69/ex70_1.jpg){width="565"
height="816"}

*Again, I find the above difficult to read. Here is my translation to
Algol,* *which Neliac is supposed to be a dialect of, using the
procedure of Halstead\'s* *book, page 22:*

    Comments This is MikeVanEmmerik's hand translation to Algol of Example 70
    in "Machine-Independent Computer Programming".

    integer procedure START();
    integer A STORE, Q STORE, AA(3), AB(3), AC, AD(4);
    begin
        AD := (AA + AB) * AC;
        if AB - AA >= 0 ;
        else SUB B();
        A STORE := AB;
        Q STORE := AC-1;
        if Q STORE >= AA and if A STORE < AA;
        else goto ENT_E;
        SUB A();
        goto ENT_A;
    ENT E:
        SUB C();
    ENT A:
        goto ENT B;
    ENT B:
        i := 0;
        for i := i step 1 until 2 do
            begin AD[i] := AA[i](3..6) + AB[i](2..5) end
        AC := AA;
    end..

    integer procedure SUB C();
    begin
        AD := (((AC + AA)/AC+AD)*AB+AA)/AC;
    end

    integer procedure SUB B();
    begin
        AB := AB - AA;
    end

    integer procedure SUB A();
    begin
        if 5 + AB - AC < 0;
        else goto ENT D;
        SUB B();
        goto ENT_C;
    ENT D:
        AB := AB + AA;
    ENT C:
    end

*As you can see, there are no parameters to worry about (most code seems
to use global variables).* *The semantics of the skip instructions are
obvious, with the blank **if** clause always followed by an **else**
clause.* *I don\'t know the semantics for bit selection in Algol, if it
has any.* *No attempt has been made to structure the gotos in the
program.* *However, a for loop has been recovered, complete with indexes
and bit ranges.*

In addition to producing the Neliac version solely from the
machine-coded version of the program, the decompiler also pro- duced a
listing of the various names which it assigned, as shown in Example 71.

      EXAMPLE 71.
      SUB A 0 10117
        ENT A 0 10166
        ENT B 0 10167
        SUB B 0 10113
        ENT C 0 10130
        ENT D 0 10126
        ENT E 0 10165
        SUB C 0 10131
        START 0 10147
      AA 3 10103
      AB 3 10100
      AC 3 10106
      AD 3 10107

where an initial zero denotes a verb and a 3 indicates a noun.

It may be noted that in a case of this kind there is no inherent meaning
in the names assigned to nouns or verbs, except perhaps to the first and
last of the verbs. If the original documentation has been adequate, so
that the comments accompanying the original program has been
sufficiently informative to allow a person to provide meaningful names
for given addresses, the decompiler will accept and use them.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
