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
    Page](http://www.program-transformation.org/edit/Sts/StatementFoldingUsingTXL?t=1536827754)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/StatementFoldingUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/StatementFoldingUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/StatementFoldingUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/StatementFoldingUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/StatementFoldingUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/StatementFoldingUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/StatementFoldingUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Sts/StatementFoldingUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
Statement Folding Using TXL {#statement-folding-using-txl .twikiTopicTitle}
===========================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#3.5,
Statement folding, recognizing and optimizing compile-time known if
statements, and possibly while and for statements.

Thie simple example demonstrates statement folding of if and while
statements using TXL. Assumes that it is used with a constant folding
opimization to yield constant conditions.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 04 Jan 2008

*File \"TILstmtfold.Txl\"*

    % Statement folding using TIL
    % Jim Cordy, January 2008

    % Given a TIL program, look for opportunities to reduce code footprint
    % by optimizing out unreachable code based on statically known conditions.

    % Statement folders are a staple of embedded code versioning, used for code 
    % reduction in limited memory applications such as mobile devices.
    % It is also used in some languages as a surrogate for conditional compilation.

    % This program is normally combined with a constant folding opimizer that 
    % evaluates constant expressions to yield the statically known conditions.


    % Begin with the TIL base grammar, using precedence
    #define PRIORITY
    include "TIL.Grm"

    % Preserve comments in this transformation
    #pragma -comment

    redefine statement
            ...
        |   [comment] [NL]
    end redefine


    % Main function - applies folders for the various statements

    function main
        replace [program]
            P [program]
        by
            P [foldTrueIfStatements]
              [foldFalseIfStatements]
              [warnTrueWhileStatements]
              [foldFalseWhileStatements]
    end function


    % Folding rules for constant condition if statements

    rule foldTrueIfStatements
        % Find an if statement
        replace [repeat statement]
            'if Cond [expression] 'then
                TrueStatements [repeat statement]
                ElseClause [opt else_statement]
            'end
            Rest [repeat statement]

        % That has a constant true condition
        where
            Cond [isTrueEqual]
                 [isTrueNotEqual]

        % By the true part
        by
            '// Folded true if
            TrueStatements [. Rest] 
    end rule

    rule foldFalseIfStatements
        % Find an if statement
        replace [repeat statement]
            'if Cond [expression] 'then
                TrueStatements [repeat statement]
                ElseClause [opt else_statement]
            'end
            Rest [repeat statement]

        % That has a constant false condition
        where not
            Cond [isTrueEqual]
                 [isTrueNotEqual]

        % By the false part
        construct FalseStatements [repeat statement]
            _ [getElseStatements ElseClause]
        by
            '// Folded false if
            FalseStatements [. Rest] 
    end rule

    function getElseStatements ElseClause [opt else_statement]
        deconstruct ElseClause
            'else
                FalseStatements [repeat statement]
        replace [repeat statement]
            % default none
        by
            FalseStatements
    end function


    % Folding rules for constant condition while statements

    rule warnTrueWhileStatements
        % "replace $" indicates one-pass search, since we don't want to match 
        % the same while statement twice

        % Find a while statement 
        replace $ [repeat statement]
            'while Cond [expression] 'do
                TrueStatements [repeat statement]
            'end
            Rest [repeat statement]

        % That has a constant true condition
        where
            Cond [isTrueEqual]
                 [isTrueNotEqual]

        % Warn but leave alone
        by
            'while Cond 'do
                '// Warning: while condition always true
                TrueStatements 
            'end
            Rest
    end rule

    rule foldFalseWhileStatements
        % Find a while statement
        replace [repeat statement]
            'while Cond [expression] 'do
                TrueStatements [repeat statement]
            'end
            Rest [repeat statement]

        % That has a constant false condition
        where not
            Cond [isTrueEqual]
                 [isTrueNotEqual]

        % And delete it!
        by
            '// Folded false while 
            Rest
    end rule


    % Utility functions to detect true conditions - these can be as smart as we wish
    % (For now just simple ones)

    function isTrueEqual 
        match [expression]
            I [integernumber] '= J [integernumber]
        where 
            I [= J]
    end function

    function isTrueNotEqual 
        match [expression]
            I [integernumber] '!= J [integernumber]
        where not 
            I [= J]
    end function

*Example run:* \"foldstmt.til\" is a meaningless little program with
several opportunities for statement folding.

    <linux> cat foldstmt.til 
    // Toy TIL example with constant conditions
    var a; var b; var c; var i;
    a := 1;
    b := a + 1;
    i := 7;
    c := a + 1;
    for i := 1 to 10 do
        a := b + i;
        if 11 = 10 then
            c := b;
        else
            c := b + i;
            a := a + 1;
        end
        while (2 = 1) do
            b := b + i;
        end
    end 
    while 5 != 10 do
        a := b + i;
        if 1 = 1 then
            a := c;
        else
            c := b + i;
        end
        b := b + i;
        if 17 = 42 then
            c := b + b;
        end
    end
    write (i - c);

    <linux> txl foldstmt.til TILstmtfold.Txl 
    TXL v10.5 (11.12.07) (c)1988-2007 Queen's University at Kingston
    Compiling TILstmtfold.Txl ... 
    Parsing foldstmt.til ...
    Transforming ...

    // Toy TIL example with constant conditions
    var a;
    var b;
    var c;
    var i;
    a := 1;
    b := a + 1;
    i := 7;
    c := a + 1;
    for i := 1 to 10 do
        a := b + i;
        // Folded false if
        c := b + i;
        a := a + 1;
        // Folded false while 
    end
    while 5 != 10 do
        // Warning: while condition always true
        a := b + i;
        // Folded true if
        a := c;
        b := b + i;
        // Folded false if
    end
    write (i - c);

    <linux>

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 04 Jan 2008\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
