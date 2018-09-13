::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
**[SDF Home](http://www.syntax-definition.org)**

-   [About](SdfLanguage){.twikiLink}
-   [Documentation](SdfDocumentation){.twikiLink}
-   [Download](SdfSoftware){.twikiLink}
-   [Grammars](SdfGrammars){.twikiLink}
-   [Related Software](SdfRelatedSoftware){.twikiLink}

**Community**

-   [Contributors](SdfDevelopment){.twikiLink}
-   [Publications](SdfPublications){.twikiLink}
-   [Applications](SdfApplications){.twikiLink}
-   [Mailing Lists](MailingList){.twikiLink}
-   [License](BSDLicense){.twikiLink}

**Development**

-   [Tools](DevelopmentTools){.twikiLink}
-   [API](http://homepages.cwi.nl/~daybuild/daily-docs)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Sdf/SDFbyExample?t=1536826616)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sdf/SDFbyExample)
-   [Attach
    File](http://www.program-transformation.org/attach/Sdf/SDFbyExample)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sdf/SDFbyExample?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sdf/SDFbyExample?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Sdf/SDFbyExample?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Sdf/SDFbyExample?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Sdf/SDFbyExample?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Sdf/SDFbyExample?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Sdf/SDFbyExample?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Sdf/SDFbyExample?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sdf/SDFbyExample)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sdf/SDFbyExample?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Sdf/SDFbyExample?template=oopsmore&param1=1.5&param2=1.5)
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
SDFby Example {#sdfby-example .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Sdf
:::

SDF2 is a rich formalism for the definition of the syntax of all kinds
of computer languages. This page explores the possibilities of the
formalism by means of a number of fragments of syntax definitions from
the SDF2 [GrammarBase](GrammarBase){.twikiLink}. In particular, the
language is contrasted with traditional formalisms that use a separate
scanner to deal with lexical syntax.

(When editing this page, uncheck the
[ConvertSpacesToTabs[^?^](http://www.program-transformation.org/edit/Sdf/ConvertSpacesToTabs?topicparent=Sdf.SDFbyExample)]{.twikiNewLink
style="background : #FFFFCE;"} checkbox to avoid spoiling the layout of
the examples.)

**Context-free Syntax Definition**

expression grammar

**Disambiguating Expressions**

**Lexical Syntax Definition**

idenitifiers, layout

**Regular Expressions**

**Overloading Delimiters**

[BibTeX[^?^](http://www.program-transformation.org/edit/Sdf/BibTeX?topicparent=Sdf.SDFbyExample)]{.twikiNewLink
style="background : #FFFFCE;"} is a language for the describtion of
bibliographical information such as articles and books. For example, the
following entry describes a
[PhD[^?^](http://www.program-transformation.org/edit/Sdf/PhD?topicparent=Sdf.SDFbyExample)]{.twikiNewLink
style="background : #FFFFCE;"} thesis.

     @PhdThesis{Vis97.thesis,
       author = {Visser, Eelco},
       title  = {Syntax Definition for Language Prototyping},
       year   = {1997},
       month  = {September},
       school = {University of Amsterdam},
       URL    = { http://www.cs.uu.nl/~visser/thesis/ }
     }

In the syntax of
[BibTeX[^?^](http://www.program-transformation.org/edit/Sdf/BibTeX?topicparent=Sdf.SDFbyExample)]{.twikiNewLink
style="background : #FFFFCE;"} entries the symbol { has two meanings:
(1) indicating the start of the list of fields and (2) indicating the
start of a field body. The second kind of use requires a lexical
treatment since the body of a field consists of an arbitrary list of
characters until the closing } is found. In an approach where scanner
and parser are separated it is not possible for the scanner to know
which kind of { is encountered. Furthermore, a field body can contain
nested occurences of { and }, which should only occur in matching pairs.
In

Finally, the treatment of whitespace is different between entries,
between the fields of an entry and inside the body of a field.

      context-free syntax
        C {Entry C}* C                  -> Entries 
        "@" EName "{" Key "," 
                      {Field ","}* ","? 
                  "}"                   -> Entry 
        Name "=" Value                  -> Field
        "{" ValWords "}"                -> Value
        (ValWord | ("{" ValWords "}"))* -> ValWords
      lexical syntax
        ~[\{\}\ \t\n]+  -> ValWord
      lexical restrictions
        ValWord   -/- ~[\{\}\ \t\n]

The complete syntax definition for
[BibTeX[^?^](http://www.program-transformation.org/edit/Sdf/BibTeX?topicparent=Sdf.SDFbyExample)]{.twikiNewLink
style="background : #FFFFCE;"} (that also treats double quotes in field
bodies correctly) can be found at

<http://www.cwi.nl/~mdejonge/grammar-base/bibtex.0/index.html>

**Solving Lexical Ambiguities**

**Longest Match**

follow restrictions

**Reserved Words**

in a normal scanner generator like LEX

when combining languages we want to have separate sets of reserved
words;

a COBOL reserved word should not be used as a COBOL identifier, but
might be quite usable as a SQL identifier

**Ignoring Whitespace in Lexicals**

In Fortran whitespace inside lexicals is not significant. This can be
accomodated in Trash.SDFII by using context-free syntax to define
lexicals.

**Dividing a Syntax Definition into Modules**

reuse of pieces of syntax

renaming

**Combining Languages**

COBOL is a language for manipulating business information represented by
means of lists of records. COBOL programs are often mixed with fragments
from other languages. For example, SQL queries can be embedded to access
a database and CICS programs are used for process control. It is
desirable to describe the syntax of each of the language separately and
combine these descriptions as needed.

In a traditional syntax definition formalism this is not possible: (1)
The grammars restrictions such LL or LALR on which the context-free
syntax is based are not closed under composition. (2) the regular
grammars on which the definition of the lexical syntax are based are not
closed under composition either.

In practice, this translates to the following: A scanner does not
consider the context in determining the sort of a token. Therefore,
normal scanners cannot deal with

(LEX provides a workaround by means of *modes*.)

In Trash.SDFII the syntax of the composing languages can be described in
separate modules and combined at will. For example, consider the
following fragments from a syntax definition for COBOL. (Note that the
actual combined syntax definition for COBOL, CICS and SQL combined
consists of 1600 LOC divided into 38 modules.)

    Module ID defines the syntax of identifiers. The 

     module ID
       lexical syntax
         [0-9]* [A-Z]                                          -> Lex-Id
         [0-9]* [A-Z] [A-Za-z0-9\-]* [A-Za-z0-9]               -> Lex-Id
         [0-9]+ [\-] [0-9\-]* [A-Z] [A-Za-z0-9\-]* [A-Za-z0-9] -> Lex-Id
       context-free syntax
         Lex-Id -> Id 
       lexical restrictions
         Lex-Id -/- [A-Za-z0-9\-]

Module COBOL defines the syntax of COBOL programs. The actual syntax
definition for cobol consists of 36 modules. Here only the productions
relevant for the example are shown. Note that the syntax of Picture
overlaps with the syntax for Id. This overlap is disambiguated by
context.

     module COBOL
       imports ID %% ...
       lexical syntax
         [0-9XxAa\(\)pZzVvSszBCRD\/\,\$\+\-\*\:]+ -> Picture
       context-free syntax
         Ident-div Env-div Data-div Proc-div            -> Program
         "DATA" "DIVISION" "." File-sec Ws-sec Link-sec -> Data-div
         "FILE" "SECTION" "." File-desc*                -> File-sec
         "FD" Id Fd-item* "." Data-desc*                -> File-desc
         Dd-header Dd-body*                             -> Data-desc

Module SQL defines the syntax for SQL queries. Queries are embedded into
COBOL programs by means of the keywords EXEC SQL \... END-EXEC.

     module SQL
       lexical syntax
         [A-Z0-9\-\_\.\:]+ -> Sql-id
       context-free syntax
         "SELECT" Distinct Select-list From-into Where Order-by -> Select
         Select                                                 -> Sql-item
         "EXEC" "SQL" Sql-item+ "END-EXEC" "."                  -> Data-desc
         "EXEC" "SQL" Sql-item+ "END-EXEC"                      -> Stat

Module CICS defines the syntax of CICS commands and their embedding in
COBOL programs. Note that a command can have a reference to an A-exp,
which is a COBOL expression.

     module CICS
       imports PROGRAM
       lexical syntax
         [A-Z]+ -> Cics-kw
       context-free syntax
         Stat* "EXEC" "CICS" Cics-command Cics-opt* "." -> Sentence
         "EXEC" "CICS" Cics-command Cics-opt* "END-EXEC" -> Stat
                
         Cics-kw                  -> Cics-opt
         Cics-kw "(" Cics-arg ")" -> Cics-opt
         A-exp                    -> Cics-arg
         Str                      -> Cics-arg
         "ADDRESS" "OF" A-exp     -> Cics-arg
         "LENGTH" "OF" A-exp      -> Cics-arg
         "ABEND"                  -> Cics-command
         %% etc.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Sdf.SDFbyExample moved from Tools.SDFbyExample on 09 Feb 2004 - 14:41
by [MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Sdf/SDFbyExample?newweb=Tools&newtopic=SDFbyExample&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
