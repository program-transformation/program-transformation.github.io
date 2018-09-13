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
    Page](http://www.program-transformation.org/edit/Sts/ConsistentlyRenamedClonesUsingTXL?t=1536827755)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/ConsistentlyRenamedClonesUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/ConsistentlyRenamedClonesUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/ConsistentlyRenamedClonesUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/ConsistentlyRenamedClonesUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/ConsistentlyRenamedClonesUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/ConsistentlyRenamedClonesUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/ConsistentlyRenamedClonesUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Sts/ConsistentlyRenamedClonesUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
Consistently Renamed Clones Using TXL {#consistently-renamed-clones-using-txl .twikiTopicTitle}
=====================================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#4.6: Clone
detection with consistent renaming. This example implements clone
detection for clones of structured statements (if, while, for) with
consistent renaming in a TIL program and outputs both a table of clone
classes and the program with clones marked up using XML tags indicating
the clone class of each instance.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 16 Oct 2007

*File \"TILclonesrenamed.Txl\"*

    % Clone detection on Tiny Imperative Language programs
    % Jim Cordy, October 2007

    % Given a TIL program, this program finds structured statement
    % clones that differ only by consistent renaming, and marks them
    % up in the source with their clone class.  The clone classes
    % themselves are output on the standard error stream as well.

    % Usage:  txl program.til TILclonesrenamed.Txl > program.clones 2> program.cloneclasses

    % Begin with the TIL base grammar
    include "TIL.Grm"

    % Overrides to conflate all structured statements into one nonterminal type.
    % Putting [structured_statement] before existing statement forms makes
    % it the preferred parse for the statements it matches.

    redefine statement
            [structured_statement] 
        |   ...
    end redefine

    define structured_statement
            [if_statement]
        |   [for_statement]
        |   [while_statement]
    end define

    % Overrides to allow XML markup of TIL statements.

    redefine statement
            ...
        |   [marked_statement]
    end redefine

    define marked_statement
            [xmltag]        [NL][IN] 
                [statement] [EX] 
            [xmlend]        [NL]
    end define

    % [SPOFF] and [SPON] temporarily disable default spacing in tags

    define xmltag
            < [SPOFF] [id] [SP] [id] = [number] > [SPON]
    end define

    define xmlend
            < [SPOFF] / [id] > [SPON]
    end define


    % Main program

    function main
        replace [program]
            P [program]

        % First make a table of all structured statements that are
        % repeated but for consistent renaming
        construct StructuredClones [repeat structured_statement]
            _ [findStructuredStatementClones P]

        % Now mark up all consistently renamed instances of each of them in the program
        % CloneNumber keeps track of the index of each one in the table as we step 
        % through it using 'each'
        export CloneNumber [number] 0
        by
            P [markCloneInstances each StructuredClones]
    end function

    % We make a table of the cloned structured statements by first making a table
    % of all structured statements in the program, then looking for repeats

    function findStructuredStatementClones P [program] 
        % Use the extract [^] function to make a table of all structured statements in the program
        % and normalize them to standard renaming 
        construct StructuredStatements [repeat structured_statement]
                _ [^ P] [renameStructuredStatement]

        % Now add each one that is repeated to the table of clones 
        construct StructuredClones [repeat structured_statement]
            _ [addIfClone StructuredStatements each StructuredStatements]

        % Output the table to the standard error stream as a clone class table
        construct CloneTable [repeat statement]
            _ [addCloneClass 0 StructuredClones]
              [print]

        % Pass the table back to the main function
        replace [repeat structured_statement]
            % empty to begin with
        by
            StructuredClones
    end function

    function addIfClone StructuredStatements [repeat structured_statement] 
                        Stmt [structured_statement]
        % A structured statement is cloned if it appears twice in the table of all statements
        deconstruct * StructuredStatements
            Stmt
            Rest [repeat structured_statement]
        deconstruct * [structured_statement] Rest
            Stmt

        % If it does appear (at least) twice, add it to the table of clones 
        replace [repeat structured_statement]
            StructuredClones [repeat structured_statement]
        % Make sure it's not already in the table
        deconstruct not * [structured_statement] StructuredClones
            Stmt
        by
            StructuredClones [. Stmt]
    end function

    % Create a readable version of the clone class table for output

    function addCloneClass NM1 [number] Clones [repeat structured_statement]
        % Index of the class in the table of clones
        construct N [number]
            NM1 [+ 1]

        % Get the next clone
        deconstruct Clones
            Clone [structured_statement]
            Rest [repeat structured_statement]

        % Mark up the clone as a numbered clone class
        replace [repeat statement]
            Stmts [repeat statement]
        construct NewStmt [statement]
            <clone_class class=N> 
                Clone 
            </clone_class>
        % And add it to the table to output
        by
            Stmts [. NewStmt] 
                  [addCloneClass N Rest]
    end function

    % Once we have the table of all clones, we mark up each instance of each of them
    % in the program with its clone class, that is, the index of it in the clone table

    rule markCloneInstances StructuredClone [structured_statement]
        % Keep track of the index of this clone in the table
        import CloneNumber [number]
        export CloneNumber 
            CloneNumber [+ 1]

        % Mark up all instances of it in the program
        % 'skipping' avoids marking any instance twice
        skipping [marked_statement]
        replace [statement]
            Stmt [structured_statement]

        % Normalize to standard renaming for comparison
        construct RenamedStmt [structured_statement]
            Stmt [renameStructuredStatement]

        % If the renamed structured statement is an instance of the clone class ...
        deconstruct RenamedStmt
            StructuredClone
        % ... then mark it as such
        by
            <clone class=CloneNumber> Stmt </clone>
    end rule

    % Rule to normalize structured statements by consistent renaming of identifiers
    % to normal form (x1, x2, x3, ...)

    rule renameStructuredStatement
        % For each outer structured statement in the scope
        skipping [structured_statement]
        replace $ [structured_statement]
            Stmt [structured_statement]

        % Make a list of all of the unique identifiers in the statement
        construct Ids [repeat id]
            _ [^ Stmt] [removeDuplicateIds]

        % Make normalized new names of the form xN for each of them
        construct GenIds [repeat id]
            Ids [genIds 0]

        % Consistently replace each instance of each one by its normalized form
        by
            Stmt [$ each Ids GenIds]
    end rule

    % Utility rule - remove duplicate ids from a list

    rule removeDuplicateIds
        replace [repeat id]
            Id [id] Rest [repeat id]
        deconstruct * [id] Rest
            Id
        by
            Rest
    end rule

    % Utility rule - make a normalized id of the form xN for each unique id in a list

    function genIds NM1 [number]
        % For each id in the list
        replace [repeat id]
            _ [id] 
            Rest [repeat id] 

        % Generate the next xN id
        construct N [number]
            NM1 [+ 1]
        construct GenId [id]
            _ [+ 'x] [+ N]

        % Replace the id with the generated one
        % and recursively do the next one
        by
            GenId 
            Rest [genIds N]
    end function

*Example run 1 (with exact clones):*

    <linux> cat cloneseg1.til
    // Silly meaningless example with lots of exact clones
    var n;
    write "Input n please";
    read n;
    var f;
    f := 2;
    while n != 1 do
        while (n / f) * f = n do
            write f;
            n := n / f;
        end
        if n = 3 then
            n := 2;
        end
        f := f + 1;
    end
    while (n / f) * f = n do
        write f;
        if n = 3 then
            n := 2;
        end
        n := n / f;
    end
    while n != 1 do
        while (n / f) * f = n do
            write f;
            n := n / f;
            if n = 3 then
                n := 2;
            end
        end
        f := f + 1;
        while (n / f) * f = n do
            write f;
            n := n / f;
        end
    end

    <linux> txl cloneseg1.til TILclonesrenamed.Txl
    TXL v10.5 (22.9.07) (c)1988-2007 Queen's University at Kingston
    Compiling TILclonesrenamed.Txl ... 
    Parsing cloneseg1.til ...
    Transforming ...

    <clone_class class=1>
        while (x1 / x2) * x2 = x1 do
            write x2;
            x1 := x1 / x2;
        end
    </clone_class>
    <clone_class class=2>
        if x1 = 3 then
            x1 := 2;
        end
    </clone_class>

    var n;
    write "Input n please";
    read n;
    var f;
    f := 2;
    while n != 1 do
        <clone class=1>
            while (n / f) * f = n do
                write f;
                n := n / f;
            end
        </clone>
        <clone class=2>
            if n = 3 then
                n := 2;
            end
        </clone>
        f := f + 1;
    end
    while (n / f) * f = n do
        write f;
        <clone class=2>
            if n = 3 then
                n := 2;
            end
        </clone>
        n := n / f;
    end
    while n != 1 do
        while (n / f) * f = n do
            write f;
            n := n / f;
            <clone class=2>
                if n = 3 then
                    n := 2;
                end
            </clone>
        end
        f := f + 1;
        <clone class=1>
            while (n / f) * f = n do
                write f;
                n := n / f;
            end
        </clone>
    end
    <linux> 

*Example run 2 (with renamed clones):*

    <linux> cat cloneseg2.til
    // Silly meaningless example with lots of renamed clones
    var n;
    write "Input n please";
    read n;
    var f;
    var g;
    f := 2;
    g := 7;
    while n != 1 do
        while (n / f) * f = n do
            write f;
            n := n / f;
        end
        if f = 3 then
            f := 2;
        end
        f := f + 1;
    end
    while (n / f) * f = n do
        write f;
        if n = 3 then
            n := 2;
        end
        n := n / f;
    end
    while n != 1 do
        while (n / f) * f = n do
            write f;
            n := n / f;
            if g = 3 then
                g := 2;
            end
        end
        f := f + 1;
        while (g / f) * f = g do
            write f;
            g := g / f;
        end
    end

    <linux> txl cloneseg2.til TILclonesrenamed.Txl
    TXL v10.5 (22.9.07) (c)1988-2007 Queen's University at Kingston
    Compiling TILclonesrenamed.Txl ... 
    Parsing cloneseg2.til ...
    Transforming ...

    <clone_class class=1>
        while (x1 / x2) * x2 = x1 do
            write x2;
            x1 := x1 / x2;
        end
    </clone_class>
    <clone_class class=2>
        if x1 = 3 then
            x1 := 2;
        end
    </clone_class>

    var n;
    write "Input n please";
    read n;
    var f;
    var g;
    f := 2;
    g := 7;
    while n != 1 do
        <clone class=1>
            while (n / f) * f = n do
                write f;
                n := n / f;
            end
        </clone>
        <clone class=2>
            if f = 3 then
                f := 2;
            end
        </clone>
        f := f + 1;
    end
    while (n / f) * f = n do
        write f;
        <clone class=2>
            if n = 3 then
                n := 2;
            end
        </clone>
        n := n / f;
    end
    while n != 1 do
        while (n / f) * f = n do
            write f;
            n := n / f;
            <clone class=2>
                if g = 3 then
                    g := 2;
                end
            </clone>
        end
        f := f + 1;
        <clone class=1>
            while (g / f) * f = g do
                write f;
                g := g / f;
            end
        </clone>
    end
    <linux> 

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 16 Oct 2007\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
