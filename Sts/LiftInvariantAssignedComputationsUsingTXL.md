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
    Page](http://www.program-transformation.org/edit/Sts/LiftInvariantAssignedComputationsUsingTXL?t=1536827757)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/LiftInvariantAssignedComputationsUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/LiftInvariantAssignedComputationsUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/LiftInvariantAssignedComputationsUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/LiftInvariantAssignedComputationsUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/LiftInvariantAssignedComputationsUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/LiftInvariantAssignedComputationsUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/LiftInvariantAssignedComputationsUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Sts/LiftInvariantAssignedComputationsUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
Lift Invariant Assigned Computations Using TXL {#lift-invariant-assigned-computations-using-txl .twikiTopicTitle}
==============================================

::: {.twikiWebTitle}
Software Transformation Systems
:::

A more sophisticated TXL solution to [TIL
Chairmarks](TILChairmarks){.twikiLink} \#3.1, Move all invariant
assigned computations outside of while loops.

This is a more sophisticated version of [Lift Invariant Assignments
Using TXL](LiftInvariantAssignmentsUsingTXL){.twikiLink}, which uses
renaming of masking assignments in a loop to expose more opportunities
to move assigned computations out of the loop. See the original for the
basics of code motion in TXL, and this one for the renaming aspect.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 04 Nov 2005

*File \"TILcodemotion2.Txl\"*

    % Lift independent assigned computations outside of TIL while loops
    % J.R. Cordy, November 2005

    % This more sophisitcated TXL program will optimize a TIL program by moving all 
    % assigned computations not dependent on computation inside while loops to the outside.
    % The process works in two steps: 
    %   (1) Renaming of masking assignments (subsequent assignments to a variable), 
    %       which exposes hidden opportunities for code motion, and 
    %   (2) Lifting of independent assignments, exactly as in the simpler assignment
    %       only case in TILcodemotion.Txl
    % Finally, declarations are synthesized and inserted for any new variables introduced 
    % by the renaming.

    % Based on the TIL grammar
    include "TIL.Grm"

    % Two main parts - the actual renaming and lifting, then the introduction of missing 
    % declarations for any introduced renamed variables
    function main
        replace [program]
            P [program]
        by
            P [renameAndLift]
              [declareNewVariables]
    end function


    % Main rule: Rename masking assignments and lift them outside loops until no more can be 
    % renamed and no more can belifted
    rule renameAndLift
        replace [program]
            P [program]

        % We continue as long as a match for either transform can be found - the form [?rule] 
        %   in TXL means test if a pattern match for the rule can be found
        % In TXL, the composition of two conditionals is "or", so this guard tests whether
        %   either rule can find a match
        where
            P [?renameMaskingAssignments]
              [?liftLoopAssignments]

        % If so, apply the rules and continue until the condition above fails 
        by
            P [renameMaskingAssignments]
              [liftLoopAssignments]
    end rule


    % Ruleset 1: Rename any masking assignments (i.e., re-assignments to the same variable)
    % This exposes hidden opportunities to move assigned computations out of the loop
    rule renameMaskingAssignments
        % Find every while loop
        replace [statement*]
            while Expn [expression] do
                Body [statement*]
            'end
            Rest [statement*]

        % Keep renaming until there are no more to rename
        where
            Body [?renameAssignment Body]
        by
            while Expn do
                Body [renameAssignment Body]
            'end 
            Rest
    end rule

    % Rename repeated assignments
    rule renameAssignment Body [statement*]
        % Find an assignment
        replace [statement*]
            X [id] := E [expression];
            Rest [statement*]

        % Construct the context it appears in
        construct PreContext [statement*]
            Body [deleteAssignmentAndRest X]

        % Rename any subsequent assignment to X, if possible
        where
            Rest [?renameAssignmentsTo X PreContext]
        by
            X := E;
            Rest [renameAssignmentsTo X PreContext]
    end rule

    % Rename any subsequent assignment to X, if possible
    rule renameAssignmentsTo X [id] PreContext [statement*]
        % Find a subsequent assignment to X
        replace [statement*]
            X := E [expression];
            Rest [statement*]

        % It only makes sense to rename it if its effect doesn't wrap around ...
        where not 
            PreContext [refers X]

        % ... and it is not an iteration 
        where not
            E [refers X]

        % ... and it is not assigned again
        where not
            Rest [assigns X]

        % If all that is ok, then rename it
        construct NewX [id]
            X [!]
        by  
            NewX := E;
            Rest [$ X NewX]      % [$ X NewX] means substitute NewX for X everywhere in Rest
    end rule


    % Ruleset 2: Lift all independent assignments out of loops
    % This is exactly the same ruleset as in TILcodemotion.Txl - we could use a TXL "include"
    % statement to reuse the original
    rule liftLoopAssignments
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

    % Delete everything in a scope from the assignment to X on -
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


    % Ruleset 3: Declare any renaming variables we introduced
    rule declareNewVariables
        replace [program]
            P [program]
        % Continue until we can't find any more
        where
            P [?declareNewVariable P]
        by
            P [declareNewVariable P]
    end rule

    function declareNewVariable P [program]
        replace * [statement*]
            X [id] := E [expression];
            MoreStatements [statement*]
        deconstruct not * [declaration] P
            'var X;
        by
            'var X;
            X := E;
            MoreStatements 
    end function

*Example run:* \"lift2.til\" is a meaningless little program intended to
demonstrate the difference between the simple assignment code motion
solution of [Lift Invariant Assignments using
TXL](LiftInvariantAssignmentsUsingTXL){.twikiLink} and the more
sophisticated one above. We first run the simple solution, and no
opportunities for code motion are found. Then we run the solution above,
which renames masking assignments to expose two computations that can be
moved out of the loop.

    <linux> cat lift2.til
    var a; var b; var c; 
    var x; var y; var z;
    while 1 do
        x := a + b;
        y := x;
        a := y + 3;
        x := b + c;
        y := x - 2;
        z := x + a * y;
    end
    <linux> txl lift2.til TILcodemotion.Txl
    TXL v10.4a (15.6.05) (c)1988-2005 Queen's University at Kingston
    Compiling TILcodemotion.Txl ... 
    Parsing lift2.til ...
    Transforming ...
    var a;
    var b;
    var c;
    var x;
    var y;
    var z;
    while 1 do
        x := a + b;
        y := x;
        a := y + 3;
        x := b + c;
        y := x - 2;
        z := x + a * y;
    end
    <linux> txl lift2.til TILcodemotion2.Txl
    TXL v10.4a (15.6.05) (c)1988-2005 Queen's University at Kingston
    Compiling TILcodemotion2.Txl ... 
    Parsing lift2.til ...
    Transforming ...
    var a;
    var b;
    var c;
    var x;
    var y;
    var z;
    var x4;
    x4 := b + c;
    var y2;
    y2 := x4 - 2;
    while 1 do
        x := a + b;
        y := x;
        a := y + 3;
        z := x4 + a * y2;
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
