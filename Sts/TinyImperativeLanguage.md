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
    Page](http://www.program-transformation.org/edit/Sts/TinyImperativeLanguage?t=1536827762)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/TinyImperativeLanguage)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/TinyImperativeLanguage)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/TinyImperativeLanguage?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/TinyImperativeLanguage?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Sts/TinyImperativeLanguage?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Sts/TinyImperativeLanguage?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Sts/TinyImperativeLanguage?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Sts/TinyImperativeLanguage?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Sts/TinyImperativeLanguage?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sts/TinyImperativeLanguage?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/TinyImperativeLanguage)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/TinyImperativeLanguage?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Sts/TinyImperativeLanguage?template=oopsmore&param1=1.4&param2=1.4)
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
Tiny Imperative Language {#tiny-imperative-language .twikiTopicTitle}
========================

::: {.twikiWebTitle}
Software Transformation Systems
:::

This is a proposal for a Tiny Imperative Language for setting tiny
benchmarks of source transformation systems such as the [TIL
Chairmarks](TILChairmarks){.twikiLink}.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} &
[JamesCordy](../Main/JamesCordy){.twikiLink}

Added \"primary -\> string\", to allow for transformations involving
addition of meaningful output statements.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 29 Apr 2005

In the draft Stratego manual Eelco has proposed that the commenting
convention of TIL be the C++ // to end of line comments. This seems a
good idea and I suggest we adopt it.

Eelco has also proposed that the \"write\" statement does not output a
full line, rather outputs only what is given. Newlines must then be
explicitly output using an escaped newline \"\\n\". This is a good idea
also but not yet agreed. It also opens the larger question of \"what\'s
in a string?\" We need some lexical specs here.

The draft Stratego manual also adds \"begin-end\" statements, which TIL
so far does not have, and seems to assume that begin-end implies scopes,
which at present it appears TIL also does not have. Both of these are
the subject of [TIL Chairmarks](TILChairmarks){.twikiLink}. Possibly the
core language should have begin-end, but if so we are committed to
nested scope rules I think. Not clear this keeps us \"tiny\".

Finally, I infer from the desugaring example in the draft Stratego
manual that it is proposed that \"for\" statements be changed to require
their control variable to be declared. This is the subject of one of the
[TIL Chairmarks](TILChairmarks){.twikiLink} transformations. Possibly we
should make this change to the core language.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 30 Aug 2005

    % Grammar for Tiny Imperative Language (TIL)

    program -> statement*

    statement ->  declaration
               |  assignment_statement
               |  if_statement
               |  while_statement
               |  for_statement
               |  read_statement
               |  write_statement

    % Untyped variables
    declaration -> "var" identifier ";"

    assignment_statement -> identifier ":=" expression ";"

    if_statement -> "if" expression "then" 
                        statement* 
                    "end"
                 |  "if" expression "then" 
                        statement* 
                    "else" 
                        statement* 
                    "end"

    % While loop 
    while_statement -> "while" expression "do"
                          statement* 
                       "end"

    % Declaring for
    for_statement -> "for"  identifier ":=" expression "to" expression do
                         statement*
                     "end"

    read_statement -> "read" identifier ";"

    write_statement -> "write" expression ";"

    % Simple 
    expression -> primary
               |  expression op expression

    primary -> identifier
            |  integer
            |  string
            |  "(" expression ")"

    op -> "=" | "!="        % lowest priority       
       |  "+" | "-"
       |  "*" | "/"         % highest priority

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
