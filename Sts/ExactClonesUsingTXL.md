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
    Page](http://www.program-transformation.org/edit/Sts/ExactClonesUsingTXL?t=1536827756)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/ExactClonesUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/ExactClonesUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/ExactClonesUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/ExactClonesUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/ExactClonesUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/ExactClonesUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/ExactClonesUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Sts/ExactClonesUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
Exact Clones Using TXL {#exact-clones-using-txl .twikiTopicTitle}
======================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#4.6: Clone
detection. This example implements clone detection for exact clones of
structured statements (if, while, for) in a TIL program and outputs the
program with clones marked up using XML tags indicating the clone class
of each instance.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 15 Oct 2007

*File \"TILclonesexact.Txl\"*

    % Clone detection on Tiny Imperative Language programs
    % Jim Cordy, October 2007

    % Given a TIL program, this program finds exact clones
    % of stuctured statements (if, while and for statements)
    % and outputs the program with exact clones marked up
    % to indicate their clone class.  

    % Usage:  txl program.til TILclonesexact.Txl > program.clones 

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
            [xmltag]         [NL][IN] 
                [statement]  [EX] 
            [xmlend]         [NL]
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

        % First make a table of all repeated structured statements
        construct StructuredClones [repeat structured_statement]
            _ [findStructuredStatementClones P]

        % Now mark up all instances of each of them in the program
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
        construct StructuredStatements [repeat structured_statement]
                _ [^ P]
        % Now add each one that is repeated to the table of clones 
        replace [repeat structured_statement]
            % empty to begin with
        by
            _ [addIfClone StructuredStatements each StructuredStatements]
    end function

    function addIfClone StructuredStatements [repeat structured_statement] Stmt [structured_statement]
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
            StructuredClone
        by
            <clone class=CloneNumber> StructuredClone </clone>
    end rule

*Example run:*

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

    <linux> txl cloneseg1.til TILclonesexact.Txl
    TXL v10.5 (22.9.07) (c)1988-2007 Queen's University at Kingston
    Compiling TILclonesexact.Txl ... 
    Parsing cloneseg1.til ...
    Transforming ...
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

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 15 Oct 2007\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
