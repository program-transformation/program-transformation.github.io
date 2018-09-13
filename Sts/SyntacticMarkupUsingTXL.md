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
    Page](http://www.program-transformation.org/edit/Sts/SyntacticMarkupUsingTXL?t=1536827753)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/SyntacticMarkupUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/SyntacticMarkupUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/SyntacticMarkupUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/SyntacticMarkupUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Sts/SyntacticMarkupUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/SyntacticMarkupUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/SyntacticMarkupUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Sts/SyntacticMarkupUsingTXL?template=oopsmore&param1=1.1&param2=1.1)
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
Syntactic Markup Using TXL {#syntactic-markup-using-txl .twikiTopicTitle}
==========================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#4.7:
Syntactic markup - Marking up program statements or expressions with
some structural property.

This example demonstrates the use of agile parsing to mark up statements
with a specified structural property, in this case embedded output. This
is a specialization of the generalized markup technique described in the
IWPC 2003 paper, \"Generalized Selective XML Markup of Source Code using
Agile Parsing\".

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 06 Jan 2008

*File \"TILmarkup.Txl\"*

    % TXL transformation to mark up statements of a TIL program with some syntactic property 
    % Jim Cordy, January 2008

    % This program marks up with XML tags all statements in a TIL program
    % matching some property specified using a syntactic pattern.

    % Based on the TIL base grammar
    include "TIL.Grm"

    % Preserve commenting, since we may want to display or maintain the result
    include "TILCommentOverrides.Grm"


    % Grammar overrides to allow for XML tags on TIL statements.
    % The same paradigm can be used for any other nonterminal type.

    redefine statement
            ...
        |   [marked_statement]
    end redefine

    define marked_statement
            [xml_tag]         [NL][IN]    % [NL] etc specify pretty tag printing
                [statement]   [EX]
            [xml_endtag]      [NL]
    end redefine


    % Simple grammar for basic XML markup tags.
    % [SPOFF] and [SPON] ("spacing off" and "spacing on") allow for local precise 
    % control of TXL output spacing, in this case no spacing % between < and >.

    define xml_tag
            '< [SPOFF] [id] '> [SPON]
    end define

    define xml_endtag
            '< [SPOFF] '/ [id] '> [SPON]
    end define


    % Our main function just gathers the steps of the transformation -
    % in this case only one rule so far

    function main
        replace [program]
            P [program]
        % We need a dummy statement to seed the markup
        construct NullStmt [statement]
            '// dummy 
        by
            P [markupMatchingStatements NullStmt]
    end function

    % Condition function to specifiy the property we're interested in
    % For this simple example, it's just statements with embedded output statements

    function matchesMarkupCriterion
        % We're interested in statements
        match [statement]
            Stmt [statement]
        % That are not themselves output statements
        deconstruct not Stmt
            _ [write_statement]
        % But have embedded output
        deconstruct * Stmt
            _ [write_statement]
    end function

    % Generic markup rule for statements matching the criterion -
    % uses the general paradigm from the IWPC 2003 paper
    % "Generalized Selective XML Markup of Source Code using Agile Parsing"
    %
    % The $ means a one-pass traversal of the code, the "skipping" prevents
    % the traversal from reconsidering the same statement after markup.
    % The recursive call forces markup of cadidate statements at all levels,
    % and the "deconstruct not" ensures we don't recursively re-mark the same statement

    rule markupMatchingStatements ThisStmt [statement]
        % Don't mark already marked statements
        skipping [marked_statement]

        % Make a one pass traversal over the statements of the program
        replace $ [statement]
            Stmt [statement]

        % Don't recursively re-mark the same statement 
        deconstruct not Stmt
            ThisStmt

        % Make sure it has the property we're interested in ...
        where 
            Stmt [matchesMarkupCriterion]

        % ... and if so, mark it
        by
            <matches>
                Stmt [markupMatchingStatements Stmt] 
            </matches>
    end rule

*Example run:*

\"factors.til\" is one of the TIL example programs.

    <linux> cat factors.til
    // Factor an input number
    var n;
    write "Input n please";
    read n;
    write "The factors of n are";
    var f;
    f := 2;
    while n != 1 do
        while (n / f) * f = n do
            write f;
            n := n / f;
        end
        f := f + 1;
    end

    <linux> txl factors.til TILmarkup.Txl
    TXL v10.5 (11.12.07) (c)1988-2007 Queen's University at Kingston
    Compiling TILmarkup.Txl ... 
    Parsing factors.til ...
    Transforming ...

    // Factor an input number
    var n;
    write "Input n please";
    read n;
    write "The factors of n are";
    var f;
    f := 2;
    <matches>
        while n != 1 do
            <matches>
                while (n / f) * f = n do
                    write f;
                    n := n / f;
                end
            </matches>
            f := f + 1;
        end
    </matches>

    <linux> 

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 06 Jan 2008\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
