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
    Page](http://www.program-transformation.org/edit/Sts/TILParserUsingTXL?t=1536827758)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/TILParserUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/TILParserUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/TILParserUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/TILParserUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Sts/TILParserUsingTXL?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Sts/TILParserUsingTXL?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Sts/TILParserUsingTXL?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sts/TILParserUsingTXL?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Sts/TILParserUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/TILParserUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/TILParserUsingTXL?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Sts/TILParserUsingTXL?template=oopsmore&param1=1.3&param2=1.3)
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
TILParser Using TXL {#tilparser-using-txl .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution for [TIL Chairmarks](TILChairmarks){.twikiLink} \#1: A
parser for the [Tiny Imperative
Language](TinyImperativeLanguage){.twikiLink} (TIL) implemented in TXL.

This is the entire solution, run using the command \"txl program.til
TILparser.Txl\" no other libraries, support modules or data files are
needed. See below for an example run.

This version accepts but does not preserve comments, which is the
default in TXL. For a pretty-printer for TIL see [TIL Pretty Printer
Using TXL](TILPrettyPrinterUsingTXL){.twikiLink}.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 17 Aug 2005 (revised
[JamesCordy](../Main/JamesCordy){.twikiLink} - 02 Nov 2005)

*File \"TILparser.Txl\"*

    % TXL parser / pretty-printer for Tiny Imperative Language
    % Jim Cordy, April 2005

    % All TXL parsers are automatically also pretty-printers if the
    % grammar includes the optional formatting cues, as in this case

    % Use the TIL grammar shown below
    include "TIL.Grm"

    % No need to do anything except recognize the input, since the grammar
    % includes the output formatting cues
    function main
       match [program]
          _ [program]
    end function

*File \"TIL.Grm\"*

    % TXL grammar for Tiny Imperative Language
    % Jim Cordy, April 2005

    % Note that all quoting, as in 'if, is not required,
    % rather an optional coding convention used by TXL programmers

    % Formatting cues, such as [NL] on the right, are optional output formatting
    % suggestions and have no input parse meaning

    % From the spec, it is not clear if TIL should be priority expression parsed or not,
    % so this grammar provides both, controlled by this switch
    % #define PRIORITY

    % Keywords of TIL, assuming TIL is a reserved-word language
    % If not, remove this section
    keys
        var if then else while do for read write
    end keys

    % Compound tokens to be recognized as a single lexical unit
    compounds
        :=  !=
    end compounds

    % Commenting convention for TIL, assuming it has one
    comments
        //
    end comments

    % Direct TXL encoding of the TIL specification grammar -
    % I don't think any explantions are needed from here on
    % [NL], [IN] and [EX] on the right are optional pretty-printing cues

    define program
        [statement*]
    end define

    define statement
            [declaration]
        |   [assignment_statement]
        |   [if_statement]
        |   [while_statement]
        |   [for_statement]
        |   [read_statement]
        |   [write_statement]
    end define

    % Untyped variables
    define declaration
        'var [id] ;                   [NL]
    end define

    define assignment_statement
        [id] := [expression] ;        [NL]
    end define

    define if_statement
        'if [expression] 'then        [IN][NL]
            [statement*]              [EX]
        [opt else_statement]
        'end                          [NL]
    end define

    define else_statement
        'else                        [IN][NL]
            [statement*]             [EX]
    end define

    % While loop 
    define while_statement
        'while [expression] 'do      [IN][NL]
            [statement*]             [EX]
        'end                         [NL]
    end define

    % Declaring for
    define for_statement
        'for [id] := [expression] 'to [expression] 'do      [IN][NL]
            [statement*]                                    [EX]
        'end                                                [NL]
    end define

    define read_statement
        'read [id] ;                 [NL]
    end define

    define write_statement
        'write [expression] ;        [NL]
    end define

    #if not PRIORITY then
    % Simple nonpriority expression grammar, as specified
    define expression
            [primary]
        |   [expression] [op] [expression]
    end define

    define op 
            = | !=       
        |   + | -
        |   * | /        
    end define

    #else PRIORITY
    % Alternative traditional priority expression grammar
    define expression
            [term]
        |   [expression] [eqop] [term]
    end define

    define eqop
            = | !=
    end define

    define term
            [factor]
        |   [term] [addop] [factor]
    end define

    define addop
            + | -
    end define

    define factor
            [primary]
        |   [factor] [mulop] [primary]
    end define

    define mulop
            * | /
    end define
    #end if PRIORITY

    define primary
            [id]
        |   [literal]
        |   ( [expression] )
    end define

    define literal
            [integernumber]
        |   [stringlit]
    end define

*Example run:*

(Note comments are accepted in input and removed in output; see [TIL
Pretty Printer Using TXL](TILPrettyPrinterUsingTXL){.twikiLink} for a
comment-preserving version.)

    <linux> cat factors.til
    // Factor an input number
    var n; write "Input n please"; read n;
    write 
    "The factors of n are"; var f; f := 2;
    while n != 1 do while (n / f) * f = n do
            // Got one - print it!
            write f; n := n / f;
    end
        f := f + 1;
            end
    <linux> txl factors.til TILparser.Txl
    TXL v10.4a (15.6.05) (c)1988-2005 Queen's University at Kingston
    Compiling TILparser.Txl ... 
    Parsing factors.til ...
    Transforming ...
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
    <linux> 

*Example run with XML parse tree output:*

    <linux> txl factors.til TILparser.Txl -xml
    TXL v10.4a (15.6.05) (c)1988-2005 Queen's University at Kingston
    Compiling TILparser.Txl ... 
    Parsing factors.til ...
    Transforming ...
    <program>
     <repeat_statement>
      <statement><declaration> var
        <id>n</id> ;
       </declaration>
      </statement>
      <statement><write_statement> write
        <expression>
         <primary><literal><stringlit>"Input n please"</stringlit></literal></primary>
        </expression> ;
       </write_statement>
      </statement>
      <statement><read_statement> read
        <id>n</id> ;
       </read_statement>
      </statement>
      <statement><write_statement> write
        <expression>
         <primary><literal><stringlit>"The factors of n are"</stringlit></literal></primary>
        </expression> ;
       </write_statement>
      </statement>
      <statement><declaration> var
        <id>f</id> ;
       </declaration>
      </statement>
      <statement><assignment_statement>
        <id>f</id> :=
        <expression>
         <primary><literal><integernumber>2</integernumber></literal></primary>
        </expression> ;
       </assignment_statement>
      </statement>
      <statement><while_statement> while
        <expression>
         <expression><primary><id>n</id></primary></expression>
         <op>!=</op>
         <expression>
          <primary><literal><integernumber>1</integernumber></literal></primary>
         </expression>
        </expression> do
        <repeat_statement>
         <statement><while_statement> while
           <expression>
            <expression>
             <expression><primary> (
               <expression>
                <expression><primary><id>n</id></primary></expression>
                <op>/</op>
                <expression><primary><id>f</id></primary></expression>
               </expression> )
              </primary>
             </expression>
             <op>*</op>
             <expression><primary><id>f</id></primary></expression>
            </expression>
            <op>=</op>
            <expression><primary><id>n</id></primary></expression>
           </expression> do
           <repeat_statement>
            <statement><write_statement> write
              <expression><primary><id>f</id></primary></expression> ;
             </write_statement>
            </statement>
            <statement><assignment_statement>
              <id>n</id> :=
              <expression>
               <expression><primary><id>n</id></primary></expression>
               <op>/</op>
               <expression><primary><id>f</id></primary></expression>
              </expression> ;
             </assignment_statement>
            </statement>
           </repeat_statement> end
          </while_statement>
         </statement>
         <statement><assignment_statement>
           <id>f</id> :=
           <expression>
            <expression><primary><id>f</id></primary></expression>
            <op>+</op>
            <expression>
             <primary><literal><integernumber>1</integernumber></literal></primary>
            </expression>
           </expression> ;
          </assignment_statement>
         </statement>
        </repeat_statement> end
       </while_statement>
      </statement>
     </repeat_statement>
    </program>
    <linux> 

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
