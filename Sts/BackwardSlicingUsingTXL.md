::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[Home](WebHome){.twikiLink}**\
[STS\'08](STS08){.twikiLink}\
[STS\'06](http://www.program-transformation.org/Sts/STS06){.twikiLink}\
[STS\'04](STS04){.twikiLink}\
[StsBench](StsBench){.twikiLink}\
\
**[News](WebNews){.twikiLink}**\
[Recent Changes](WebChanges){.twikiLink}\
[Mailinglist](MailingList){.twikiLink}\
\
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
    Page](http://www.program-transformation.org/edit/Sts/BackwardSlicingUsingTXL?t=1536827756)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/BackwardSlicingUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/BackwardSlicingUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/BackwardSlicingUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/BackwardSlicingUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Sts/BackwardSlicingUsingTXL?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Sts/BackwardSlicingUsingTXL?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Sts/BackwardSlicingUsingTXL?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sts/BackwardSlicingUsingTXL?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Sts/BackwardSlicingUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/BackwardSlicingUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/BackwardSlicingUsingTXL?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Sts/BackwardSlicingUsingTXL?template=oopsmore&param1=1.3&param2=1.3)
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
Backward Slicing Using TXL {#backward-slicing-using-txl .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#4.5:
Static slicing. This example implements backward static slicing using
cascaded markup to a fixed point.

**Notes:** In an implementation for a real scoped language, a unique
renaming transformation would normally be done before slicing in order
to remove ambiguities of reference. Alias resolution may or may not be
necessary depending on the language. Inter-procedural slicing is added
in the usual way, by marking the formal parameters corresponding to any
argument variable of the slice passed by reference to the procedure.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 02 Mar 2007

*File \"TILbackslice.Txl\"*

    % Backward static slicing of Tiny Imperative Language programs
    % Jim Cordy, February 2007

    % Given a TIL program with a single statement marked up using the
    % XML markup <mark> </mark>, backward slices the program from that
    % statement and its referenced variables.

    % Works by inducing markup of unmarked statements from already marked-up
    % statements beginning with the original marked statement until a fixed 
    % point is reached, then removing all remaining unmarked statements.
    % No dependency graph is required.

    % Begin with the TIL base grammar
    include "TIL.Grm"

    % Add allowance for XML markup of TIL statements
    redefine statement
            ...
        |   [marked_statement]
    end redefine

    define marked_statement
                [xmltag] [statement] [xmlend]
    end define

    define xmltag
            < [SPOFF] [id] > [SPON]
    end define

    define xmlend
            < [SPOFF] / [id] > [SPON]
    end define

    % Conflate while and for statements into one form to optimize
    % handling of both forms in one rule
    redefine statement
            [loop_statement]
        |   ...
    end redefine

    define loop_statement
            [loop_head]                [NL][IN]
                [statement*]           [EX]
            'end                       [NL]
    end define

    define loop_head
            while [expression] do
        |   for [id] := [expression] to [expression] do
    end define


    % The main function gathers the steps of the transformation:
    % induce markup to a fixed point, remove unmarked statements,
    % remove declarations for variables not used in the slice,
    % and strip the markups to yield the sliced program

    function main
        replace [program]
            P [program]
        by
            P [propogateMarkupToFixedPoint]
              [removeUnmarkedStatements]
              [removeRedundantDeclarations]
              [stripMarkup]
    end function

    % Back propogate markup of statements beginning with the initially
    % marked statement of interest.  Continue until a fixed point, 
    % when no new markups are induced

    rule propogateMarkupToFixedPoint
        replace [program]
            P [program]

        construct NP [program]
            P [backPropogateAssignments]
              [backPropogateReads]
              [whilePropogateControlVariables]
              [loopPropogateMarkup]
              [loopPropogateMarkupIn]
              [ifPropogateMarkupIn]
              [compoundPropogateMarkupOut]

        % We're at a fixed point when P = NP   :-)
        deconstruct not NP
            P
        by
            NP 
    end rule

    % Rule to back-propogate markup of assignments.
    % A previous assignment is in the slice if its assigned 
    % variable is used in a following marked statement

    rule backPropogateAssignments
        skipping [marked_statement]
        replace [statement*]
            X [id] := E [expression] ; 
            More [statement*]
        where 
            More [hasMarkedUse X]
        by
            <mark> X := E; </mark>
            More 
    end rule

    % Similar rule for back-propogating markup of read statements

    rule backPropogateReads
        skipping [marked_statement]
        replace [statement*]
            read X [id] ; 
            More [statement*]
        where 
            More [hasMarkedUse X]
        by
            <mark> read X; </mark>
            More 
    end rule

    function hasMarkedUse X [id]
        match * [marked_statement]
            M [marked_statement]
        deconstruct * [expression] M
            E [expression]
        deconstruct * [id] E
            X
    end function

    % Assignments to variables inside a while loop containing statements
    % of a slice are also in the slice if the while condition uses them

    rule whilePropogateControlVariables
        replace $ [statement]
            while E [expression] do
                S [statement*]
            'end
        deconstruct * [statement] S
            _ [marked_statement]
        by
            while E do
                S [markAssignmentsTo E]
                  [markReadsOf E]
            'end
    end rule

    rule markAssignmentsTo Exp [expression]
        skipping [marked_statement]
        replace $ [statement]
            X [id] := E [expression] ;
        deconstruct * [id] Exp
            X
        by
            <mark> X := E; </mark>
    end rule

    rule markReadsOf Exp [expression]
        skipping [marked_statement]
        replace $ [statement]
            read X [id] ;
        deconstruct * [id] Exp
            X
        by
            <mark> read X; </mark>
    end rule

    % Rule for propagating dependencies around loops.
    % An assignment inside a loop is in the slice if its assigned variable
    % is used in a marked statement anywhere inside the loop

    rule loopPropogateMarkup
        replace $ [statement]
            Head [loop_head]
                S [statement*]
            'end
        construct MarkedS [marked_statement*]
            _ [^ S]
        construct MarkedE [expression*]
            _ [^ MarkedS]
        by
            Head
                S [markAssignmentsTo each MarkedE]
                  [markReadsOf each MarkedE]
            'end
    end rule

    % Rule for propagating dependencies into loops.
    % An assignment inside the loop is in the slice if its assigned variable 
    % is used in a marked statement anywhere following the loop

    rule loopPropogateMarkupIn
        replace $ [statement*]
            Head [loop_head]
                S [statement*]
            'end
            MoreS [statement*]
        construct MarkedMoreS [marked_statement*]
            _ [^ MoreS]
        construct MarkedMoreE [expression*]
            _ [^ MarkedMoreS]
        by
            Head
                S [markAssignmentsTo each MarkedMoreE]
                  [markReadsOf each MarkedMoreE]
            'end
            MoreS
    end rule

    % Rule for propagating dependencies into if statements.
    % An assignment inside the then or else part of the if is in the slice 
    % if its assigned variable is used in a marked statement anywhere 
    % following the if

    rule ifPropogateMarkupIn
        replace $ [statement*]
            if E [expression] then
                ST [statement*]
            ElseSE [opt else_statement]
            'end
            MoreS [statement*]
        construct MarkedMoreS [marked_statement*]
            _ [^ MoreS]
        construct MarkedMoreE [expression*]
            _ [^ MarkedMoreS]
        by
            if E then
                ST [markAssignmentsTo each MarkedMoreE]
            ElseSE [markAssignmentsTo each MarkedMoreE]
            'end
            MoreS
    end rule

    % Rule for propagating dependencies out.
    % A compound statement of any kind is in the loop if it contains
    % a marked statement

    rule compoundPropogateMarkupOut
        replace $ [statement*]
            CS [statement]
            More [statement*]
        deconstruct not CS
            _ [marked_statement]
        deconstruct * [statement] CS
            _ [marked_statement]
        by
            <mark> CS </mark>
            More
    end rule

    % Rule to remove all unmarked statements after the fixed point
    % is reached, yielding only the slice

    rule removeUnmarkedStatements
        replace [statement*]
            S [statement]
            More [statement*]
        deconstruct not S
            _ [marked_statement]
        deconstruct not S
            _ [declaration]
        by
            More
    end rule

    % Rule to remove declarations not needed in the slice

    rule removeRedundantDeclarations
        replace [statement*]
            var X [id] ;
            More [statement*]
        deconstruct not * [id] More
            X
        by
            More
    end rule

    % Rule to strip all markup when we're done

    rule stripMarkup
        replace [statement]
            < _ [id] > S [statement] </ _ [id] >
        by
            S
    end rule

*Example run 1:*

    <linux> cat sliceg1.til
    var n;
    read n;
    var fac;
    fac := 1;
    var sum;
    sum := 0;
    var i;
    i := 1;
    while i != n+1 do
        fac := fac * i;
        sum := sum + i;
        i := i + 1;
    end
    <foo>write fac;</foo>
    write sum;

    <linux> txl sliceg1.til TILbackslice.Txl
    TXL v10.4d (4.2.07) (c)1988-2007 Queen's University at Kingston
    Compiling TILbackslice.Txl ... 
    Parsing sliceg1.til ...
    Transforming ...
    var n;
    read n;
    var fac;
    fac := 1;
    var i;
    i := 1;
    while i != n + 1 do
        fac := fac * i;
        i := i + 1;
    end
    write fac;

    <linux>

*Example run 2:*

    <linux> cat sliceg2.til 
    var x;
    x := 0;
    var t;
    t := 0;
    for i := 1 to 10 do
        if x = 1 then
            t := t * i;
        else
            t := t + i;
        end
        x := 1;
    end
    <mark>write x;</mark>

    <linux> txl sliceg2.til TILbackslice.Txl
    TXL v10.4d (4.2.07) (c)1988-2007 Queen's University at Kingston
    Compiling TILbackslice.Txl ... 
    Parsing sliceg2.til ...
    Transforming ...
    var x;
    x := 0;
    for i := 1 to 10 do
        x := 1;
    end
    write x;

    <linux> 

*Example run 3:*

    <linux> cat sliceg6.til
    var lines;
    lines := 0;    
    var chars;    
    var n;    
    read n;
    var eof_flag;
    read eof_flag;
    chars := n;   
    while eof_flag do
        lines := lines + 1;     
        read n;
        read eof_flag;
        chars := chars + n;   
    end
    <mark>write (lines);</mark>
    write (chars);

    <linux> txl sliceg6.til TILbackslice.Txl
    TXL v10.4d (4.2.07) (c)1988-2007 Queen's University at Kingston
    Compiling TILbackslice.Txl ... 
    Parsing sliceg6.til ...
    Transforming ...
    var lines;
    lines := 0;
    var eof_flag;
    read eof_flag;
    while eof_flag do
        lines := lines + 1;
        read eof_flag;
    end
    write (lines);

    <linux>

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 02 Mar 2007\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Sts.BackwardSlicingUsingTXL moved from Sts.TILBackwardSlicingUsingTXL
on 03 Mar 2007 - 20:41 by [JamesCordy](../Main/JamesCordy){.twikiLink}*
- [put it
back](http://www.program-transformation.org/rename/Sts/BackwardSlicingUsingTXL?newweb=Sts&newtopic=TILBackwardSlicingUsingTXL&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
