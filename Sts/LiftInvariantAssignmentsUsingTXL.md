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
    Page](http://www.program-transformation.org/edit/Sts/LiftInvariantAssignmentsUsingTXL?t=1536827757)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/LiftInvariantAssignmentsUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/LiftInvariantAssignmentsUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/LiftInvariantAssignmentsUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/LiftInvariantAssignmentsUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Sts/LiftInvariantAssignmentsUsingTXL?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sts/LiftInvariantAssignmentsUsingTXL?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Sts/LiftInvariantAssignmentsUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/LiftInvariantAssignmentsUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/LiftInvariantAssignmentsUsingTXL?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Sts/LiftInvariantAssignmentsUsingTXL?template=oopsmore&param1=1.2&param2=1.2)
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
Lift Invariant Assignments Using TXL {#lift-invariant-assignments-using-txl .twikiTopicTitle}
====================================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#3.1, Move
all invariant assignments outside of while loops.

This is a simple demonstration of the basics of data flow checking and
code motion using TXL. For TIL this is not very challenging. In real
languages and applications, more sophisticated data flow and alias
analysis across procedures is needed. In TXL this more sophisticated
analysis is done using source code markup to localize dependency
information before actual code movement.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 03 Nov 2005

*File \"TILcodemotion.Txl\"*

    % Lift independent assignments outside of TIL while loops
    % J.R. Cordy, November 2005

    % This TXL program will optimize a TIL program by moving all assignments 
    % not dependent on computation inside while loops to the outside.  
    % For loops can be done similarly, but are not handled by this program.

    % Based on the TIL grammar
    include "TIL.Grm"

    % Lift all independent assignments out of loops
    rule main
        % Find every loop
        replace [statement*]
            while Expn [expression] do
                Body [statement*]
            'end 
            Rest [statement*]

        % Construct a list of all the top-level assignments in it
        construct AllAssignments [statement*]
            Body [deleteNonAssignments]

        % Construct a copy of the loop to work on
        construct LiftedLoop [statement*]
            while Expn do
                Body 
            'end 

        % Only proceed if there are assignments left that can be lifted out
        % The [?loopLift] form tests if the pattern of the [loopLift] rule can be matched -
        % "each AllAssignments" tests this for any of the top-level internal assignments
        where
            LiftedLoop [?loopLift Body each AllAssignments]

        % If the above guard succeeds, some can be moved out, so go ahead and move them,
        % replacing the original loop with the result
        by
            LiftedLoop [loopLift Body each AllAssignments]
            [. Rest]
    end rule

    % Attempt to lift a given assignment outside the loop
    function loopLift Body [statement*] Assignment [statement]
        deconstruct Assignment
            X [id] := E [expression];

        % Extract a list of all the identifiers used in the expression
        construct IdsInExpression [id*]
            _ [^ E]

        % Replace the loop and its contents
        replace [statement*]
            Loop [statement*]

        % We can only lift the assignment out if all the identifiers in its
        % expression are not assigned in the loop ...
        where not
            Loop [assigns each IdsInExpression]

        % ... and X itself is assigned only once
        deconstruct * Body
            X := _ [expression];
            Rest [statement*]
        where not
            Rest [assigns X]

        % ... and the the effect of it does not wrap around the loop
        construct PreContext [statement*]
            Body [deleteAssignmentAndRest X]
        where not 
            PreContext [refers X]

        % Now lift out the assignment
        by
            Assignment
            Loop [deleteAssignment Assignment]
    end function


    % Utility rules used above

    % Delete a given assignment statement from a scope
    function deleteAssignment Assignment [statement]
        replace * [statement*]
            Assignment
            Rest [statement*]
        by
            Rest
    end function

    % Delete all non-assignment statements in a scope - 
    % given a scope, yields the assignments only
    rule deleteNonAssignments
        replace [statement*]
            S [statement]
            Rest [statement*]
        deconstruct not S
            _ [assignment_statement]
        by
            Rest
    end rule

    % Delete everything in a scope from the first assignment to X on -
    % given a scope and X, yields the context of the first assignment to X
    function deleteAssignmentAndRest X [id]
        replace * [statement*]
            X := E [expression];
            Rest [statement*]
        by
            % nada
    end function

    % Condition - given a scope, does the scope assign to the identifier?
    function assigns Id [id]
        match * [assignment_statement]
            Id := Expn [expression];
    end function

    % Condition - given a scope, does the scope refer to the identifier?
    function refers Id [id]
        match * [id]
            Id
    end function

*Example run:* \"lift.til\" is a meaningless little program with lots of
data dependencies, lots of opportunities for code motion, and all global
declarations for demonstration purposes only.

    <linux> cat lift.til
    var x; var y; var z; var a; var b; var c;
    var d; var e; var j; var k; var m; var n; var r;
    y := 1;
    z := 2;
    while 1 do
        x := y + z;
        a := 3;
        z := 5;
        j := 0;
        while j != 100 do
            r := 99;
            d := 7;
            k := a + z;
            b := j * z;
            d := (y + z) * d;
            e := (x + z) * r;
            j := j + 1;
        end 
        c := a + y;
        m := y * b;
        n := r * y;
    end 

    <linux> txl lift.til TILcodemotion.Txl
    TXL v10.4a (15.6.05) (c)1988-2005 Queen's University at Kingston
    Compiling TILcodemotion.Txl ... 
    Parsing lift.til ...
    Transforming ...
    var x;
    var y;
    var z;
    var a;
    var b;
    var c;
    var d;
    var e;
    var j;
    var k;
    var m;
    var n;
    var r;
    y := 1;
    z := 2;
    a := 3;
    c := a + y;
    r := 99;
    n := r * y;
    while 1 do
        x := y + z;
        z := 5;
        j := 0;
        k := a + z;
        e := (x + z) * r;
        while j != 100 do
            d := 7;
            b := j * z;
            d := (y + z) * d;
            j := j + 1;
        end
        m := y * b;
    end
    <linux> 

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
