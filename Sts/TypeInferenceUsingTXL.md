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
    Page](http://www.program-transformation.org/edit/Sts/TypeInferenceUsingTXL?t=1536827756)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sts/TypeInferenceUsingTXL)
-   [Attach
    File](http://www.program-transformation.org/attach/Sts/TypeInferenceUsingTXL)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sts/TypeInferenceUsingTXL?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sts/TypeInferenceUsingTXL?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Sts/TypeInferenceUsingTXL?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Sts/TypeInferenceUsingTXL?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Sts/TypeInferenceUsingTXL?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sts/TypeInferenceUsingTXL)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sts/TypeInferenceUsingTXL?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Sts/TypeInferenceUsingTXL?template=oopsmore&param1=1.2&param2=1.2)
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
Type Inference Using TXL {#type-inference-using-txl .twikiTopicTitle}
========================

::: {.twikiWebTitle}
Software Transformation Systems
:::

TXL solution to [TIL Chairmarks](TILChairmarks){.twikiLink} \#4.4: Type
inference. This example implements type inference for untyped variables
in a TIL program and flags all type conflicts and ambiguous types as
errors.

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 03 Mar 2007

*File \"TILtypeinf.Txl\"*

    % TXL transformation to infer types for TIL variables and expressions
    % Jim Cordy, March 2007

    % This program annotates all expressions and variables in a TIL program
    % with their inferred type, adds inferred types to variable declarations 
    % and flags all type conflicts as errors.

    % Based on the TIL base grammar
    include "TIL.Grm"

    % Preserve comments, we're probably going to maintain the result
    include "TILCommentOverrides.Grm"


    % Grammar overrides to allow for type specs on TIL variable declarations.
    % The input TIL program may have either typed or untyped declarations.
    % This transformation will infer the types of all untyped variables.

    redefine declaration
       'var [primary] [opt colon_type_spec] ';   [NL]
    end redefine

    define colon_type_spec
       ': [type_spec]
    end define

    define type_spec
       'int | 'string | 'UNKNOWN
    end define


    % Grammar overrides to allow for type attributes on primary expressions.
    % The TXL form [attr X] means that the [X] is an attribute - that is, 
    % it cannot appear in input and is not printed in output.

    redefine primary 
       [subprimary] [attr type_attr]
    end redefine

    define subprimary
       [id] | [literal] | '( [expression] ') 
    end define

    define type_attr
       '{ [opt type_spec] '}
    end define


    % Grammar overrides to conflate all [id] references to the more 
    % general [primary], to make attribution rules simpler.

    redefine assignment_statement
       [primary] ':= [expression] ';   [NL]
    end redefine

    redefine for_statement
        'for [primary] := [expression] 'to [expression] 'do   [IN][NL]
           [statement*]                                 [EX]
        'end                                             [NL]
    end redefine

    redefine read_statement
       'read [primary] ';   [NL]
    end redefine


    % Our main function carries out the typing process in several steps:

    %    1. introduce complete parenthesization (to allow for detailed 
    %        attribution),
    %    2. enter default empty type attributes for everything,
    %    3. attribute literal expressions,
    %    4. infer attributes from context until a fixed point is reached,
    %    5. set type attribute of uninferred items to UNKNOWN,
    %    6. add declaration types from variables' inferred type attribute,
    %    7. report errors (i.e., any statement with an UNKNOWN in it),
    %    8. undo complete parenthesization.

    function main
        replace [program]
            P [program]
        by
            P [bracketExpressions]
              [enterDefaultAttributes]
              [attributeStringConstants]
              [attributeIntConstants]
              [attributeProgramToFixedPoint]
              [completeWithUnknown]
              [typeDeclarations]
              [reportErrors]
              [unbracketExpressions]
    end function

    % Rules to introduce and undo complete parenthesization to allow 
    % for detailed unambiguous type attribution

    rule bracketExpressions
        skipping [expression]
        replace [expression]
            E1 [expression] Op [op] E2 [expression]
        by
           '( E1 Op E2 ')
    end rule

    rule unbracketExpressions
        skipping [expression]
        replace [expression]
            '( E1 [expression] Op [op] E2 [expression] ') 
                {Type [type_spec]}
        by
            E1 Op E2
    end rule

    % Rule to add empty type attributes to every primary expression 
    % and variable

    rule enterDefaultAttributes
        replace [attr type_attr]
        by
            { }
    end rule
               

    % The meat of the type inference algorithm..  
    % Infer types of empty type attributes from the types in the  
    % context in which they are used.  Continue until a fixed point 
    % is reached, that is, until no more attributes can be inferred.

    rule attributeProgramToFixedPoint
        replace [program]
            P [program]
        construct NP [program]
            P [attributeAssignments]
              [attributeOperations]
              [attributeForIds]
              [attributeDeclarations]
        deconstruct not NP
             P
        by
             NP
    end rule

    rule attributeStringConstants
        replace [primary]
            S [stringlit] { }
        by
            S {string}
    end rule

    rule attributeIntConstants
        replace [primary]
            I [integernumber] { }
        by
            I {int}
    end rule

    rule attributeAssignments
        replace [assignment_statement]
            X [id] { } := SP [subprimary] {Type [type_spec]};
        by
            X {Type} := SP {Type};
    end rule

    rule attributeOperations
        replace [primary]
            ( P1 [subprimary] {Type [type_spec]} 
                Op [op] P2 [subprimary] {Type} ) { }
        by
            ( P1 {Type} Op P2 {Type} ) {Type}
    end rule

    rule attributeForIds
        replace [for_statement]
           'for Id [id] { } := P1 [subprimary] {Type [type_spec]} 
                   'to P2 [subprimary] {Type} 'do
                S [statement*]
           'end
        by
           'for Id {Type} := P1 {Type} 'to P2 {Type} 'do
                 S 
           'end
    end rule

    rule attributeDeclarations
        replace [statement*]
           'var Id [id] { } ;
            S [statement*]
        deconstruct * [primary] S
            Id {Type [type_spec]}
        by
           'var Id {Type};
            S [attributeReferences Id Type]
    end rule

    rule attributeReferences Id [id] Type [type_spec]
        replace [primary]
            Id { }
        by
            Id {Type}
    end rule


    % Once a fixed point has been reached, any remaining empty type 
    % attributes do not have enough context information to infer a type, 
    % or have conflicting context information for the type.  
    % Set all such remaining empty type attributes to UNKNOWN.

    rule completeWithUnknown
        replace [attr type_attr]
           { }
        by
           {UNKNOWN}
    end rule


    % Rule to add an explicit type to every untyped variable 
    % declaration.  The appropriate type is set from the variable's 
    % inferred type attribute.

    rule typeDeclarations
        replace [declaration]
            'var Id [id] {Type [type_spec]} ;
        by
            'var Id {Type} : Type;
    end rule


    % Report all type errors.  Any statement containing an UNKNOWN 
    % attribute has either a type conflict or not enough information 
    % to infer a type. 

    rule reportErrors
        replace $ [statement]
           S [statement]
        skipping [statement*]
        deconstruct * [type_spec] S
            'UNKNOWN

        % Issue an error message to the standard error stream.
        % The [pragma "-attr"] function turns on attribute printing so 
        % that the inferred type attributes of everything in the statement 
        % are printed in the message.
        % [stripBody] makes sure that if the error is in the header of an if, 
        % while or for statement we don't print the whole body in the message.

        construct Message [statement]
            S [pragma "-attr"] 
              [message "*** ERROR: Unable to resolve types in:"]
              [stripBody]
              [putp "%"]
              [pragma "-noattr"]
        by 
             S
    end rule

    function stripBody
        replace * [repeat statement]
           _ [repeat statement]
        by
            % nothing
    end function

*Example run:*

    <linux> cat typeinfeg.til
    var s;
    var i;
    var m;
    s := "foo";
    i := 2;
    s := s + "bar";
    i := i + 1;
    for i := 1 to 10 do
        s := (s + i) * 2;
    end
    m := m + m;
    var j;
    for j := 1 to m do
        i := m;
    end 

    <linux> txl typeinfeg.til TILtypeinf.Txl

    TXL v10.4d (4.2.07) (c)1988-2007 Queen's University at Kingston
    Compiling TILtypeinf.Txl ... 
    Parsing typeinfeg.til ...
    Transforming ...

    *** ERROR: Unable to resolve types in:
    var m {UNKNOWN} : UNKNOWN;

    *** ERROR: Unable to resolve types in:
    s {string} := ((s {string} + i {int}) {UNKNOWN} * 2 {int}) {UNKNOWN};

    *** ERROR: Unable to resolve types in:
    m {UNKNOWN} := (m {UNKNOWN} + m {UNKNOWN}) {UNKNOWN};

    *** ERROR: Unable to resolve types in:
    var j {UNKNOWN} : UNKNOWN;

    *** ERROR: Unable to resolve types in:
    for j {UNKNOWN} := 1 {int} to m {UNKNOWN} do
    end

    *** ERROR: Unable to resolve types in:
    i {int} := m {UNKNOWN};


    var s : string;
    var i : int;
    var m : UNKNOWN;
    s := "foo";
    i := 2;
    s := s + "bar";
    i := i + 1;
    for i := 1 to 10 do
        s := (s + i) * 2;
    end
    m := m + m;
    var j : UNKNOWN;
    for j := 1 to m do
        i := m;
    end

    <linux>

\-- [JamesCordy](../Main/JamesCordy){.twikiLink} - 03 Mar 2007\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
