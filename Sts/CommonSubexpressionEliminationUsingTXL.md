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
    Page](http://www.program-transformation.org/edit/Sts/CommonSubexpressionEliminationUsingTXL?t=1536827755)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/CommonSubexpressionEliminationUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/CommonSubexpressionEliminationUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/CommonSubexpressionEliminationUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/CommonSubexpressionEliminationUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/CommonSubexpressionEliminationUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/CommonSubexpressionEliminationUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/CommonSubexpressionEliminationUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Sts/CommonSubexpressionEliminationUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
Common Subexpression Elimination Using TXL {#common-subexpression-elimination-using-txl .twikiTopicTitle}
==========================================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#3.2,
Common subexpression elimination.

Thie simple example demonstrates the basics of common subexpression
elimination at the statement level using TXL. In a realistic application
for optimizing numerical programs, this would be combined with constant
folding and code motion transformations to yield a higher quality
result.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 19 Oct 2007

*File \"TILcommonsubexp.Txl\"*

    % TXL transformation to recognize and optimize common subexpressions
    % Jim Cordy, March 2007

    % This program finds subexpressions that are used two or more times without
    % intervening changes to the variables used in it, and introduces a new
    % temporary variable to optimize it to a single computation.

    % Based on the TIL base grammar
    include "TIL.Grm"

    % Preserve comments, we're probably going to maintain the result
    include "TILCommentOverrides.Grm"

    % Override grammar to abstract compound statements
    redefine statement
            [compound_statement]
        |   ...
    end redefine

    define compound_statement
            [if_statement]
        |   [while_statement]
        |   [for_statement]
    end define

    % Allow statements to be attributed so we don't mistake one we've
    % generated for one we need to process

    redefine statement 
            ...
        |   [statement] [attr 'NEW]
    end redefine

    % Main function

    function main
        replace [program]
            P [program]
        by
            P [optimizeSubexpressions]
    end function

    rule optimizeSubexpressions
        replace [statement*]
            S1 [statement]
            SS [statement*]

        % Don't process statements we generated
        deconstruct not * [attr 'NEW] S1
            'NEW

        % What we're looking for is an expression ...
        deconstruct * [expression] S1
            E [expression]

        % ... that is nontrivial ...
        deconstruct * [op]  E
            _ [op]

        % ... and repeated 
        deconstruct * [expression] SS
            E

        % See if we can abstract it (checks if variables assigned between)
        where
            SS [?replaceExpnCopies S1 E 'T]

        % If so, generate a new temporary variable name ...
        construct T [id]
            _ [unquote "temp"] [!]

        % ... declare it, assign it the common expression,
        % and replace instances of the expression with it
        construct NewS [statement*]
            'var T; 'NEW
            T := E; 'NEW
            S1 [replaceExpn E T]
            SS [replaceExpnCopies S1 E T]
        by
            NewS 
    end rule

    % Recursively replace copies of a given expression with a given temporary variable id,
    % provided the variables used in the expression are not assigned in between

    function replaceExpnCopies S1 [statement] E [expression] T [id]
        construct Eids [id*]
            _ [^ E]

        % If the previous statement did not assign any of the variables in the expression
        where not
            S1 [assigns each Eids]

        % Then we can continue to substitute the temporary variable for the expression
        % in the next statement ...
        replace [statement*]
            S [statement]
            SS [statement*]

        % ... as long as it isn't a compound statement that internally assigs one of 
        % the variables in the expression 
        where not all
            S [assignsOne Eids]
              [isCompoundStatement]
        by
            S [replaceExpn E T]
            SS [replaceExpnCopies S E T]
    end function

    % Condition function checking to see if a statement assigns a variable

    function assignsOne Eids [id*]
        match [statement]
            S [statement]
        where 
            S [assigns each Eids]
    end function

    function assigns Id [id]
        match * [statement]
            Id := _ [expression] ;
    end function

    function isCompoundStatement
        match [statement]
            _ [compound_statement]
    end function

    rule replaceExpn E [expression] T [id]
        replace [expression]
            E
        by
            T
    end rule

*Example run:* \"commonsubexpeg.til\" is a meaningless little program
with lots of common subexpressions, both optimizable and not.

    <linux> cat commonsubexpeg.til 
    // Silly TIL example with lots of common subexpressions
    var a;
    var b;
    var c;
    a := 1;
    b := a + 1;
    var i;
    i := 7;
    c := a + 1;
    i := i - c;
    c := b + i;
    for i := 1 to 10 do
        a := b + i;
        if b + i != 10 then
            c := b;
        else
            c := b + i;
        end
        b := b + i;
    end 
    while b != 10 do
        a := b + i;
        if b + i != 10 then
            a := c;
        else
            c := b + i;
        end
        b := b + i;
    end
    write (i - c);

    <linux> txl commonsubexpeg.til TILcommonsubexp.Txl 
    TXL v10.5 (22.9.07) (c)1988-2007 Queen's University at Kingston
    Compiling TILcommonsubexp.Txl ... 
    Parsing commonsubexpeg.til ...
    Transforming ...

    // Silly TIL example with lots of common subexpressions
    var a;
    var b;
    var c;
    a := 1;
    var temp1;
    temp1 := a + 1;
    b := temp1;
    var i;
    i := 7;
    c := temp1;
    i := i - c;
    c := b + i;
    for i := 1 to 10 do
        var temp2;
        temp2 := b + i;
        a := temp2;
        if temp2 != 10 then
            c := b;
        else
            c := temp2;
        end
        b := temp2;
    end
    while b != 10 do
        var temp3;
        temp3 := b + i;
        a := temp3;
        if temp3 != 10 then
            a := c;
        else
            c := temp3;
        end
        b := temp3;
    end
    write (i - c);

    <linux> 

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 19 Oct 2007\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
