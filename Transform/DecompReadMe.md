::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![](../pub/transformation.gif)

------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

**Surveys**\
[Transformation](ProgramTransformation){.twikiLink}\
[Reengineering](ReengineeringWiki){.twikiLink}\
[DSL](DomainSpecificLanguages){.twikiLink}\
[Domain Engineering](DomainEngineering){.twikiLink}\
[Decompilation](DeCompilation){.twikiLink}\
[Generative Progr.](GenerativeProgrammingWiki){.twikiLink}\
\
**[Collections](CategoryCollection){.twikiLink}**\
[Categories](CategoryCategory){.twikiLink}\
[Systems](TransformationSystems){.twikiLink}\
[Conferences](TransformationConferences){.twikiLink}\
[People](TransformationPeople){.twikiLink}\
[Companies](TransformationCompanies){.twikiLink}\
[Papers](CategoryPaper){.twikiLink}

------------------------------------------------------------------------

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
    Page](http://www.program-transformation.org/edit/Transform/DecompReadMe?t=1536826455)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompReadMe)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompReadMe)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompReadMe?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompReadMe?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Transform/DecompReadMe?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Transform/DecompReadMe?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Transform/DecompReadMe?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DecompReadMe?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DecompReadMe?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompReadMe)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompReadMe?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompReadMe?template=oopsmore&param1=1.3&param2=1.3)
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
Decomp Read Me {#decomp-read-me .twikiTopicTitle}
==============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

This is the `readme` file for the \"decomp\" decompiler by Jim Reuter.

------------------------------------------------------------------------

            This README file describes the decompiler that resides
            in this directory.


    WHAT IT IS:

    The decompiler does just what the name implies--it decompiles object
    files into C source files (almost).

    WHO WROTE IT:

            Jim Reuter
            reuter@cookie.dec.com
            ...!decwrl!cookie.dec.com!reuter
            COOKIE::REUTER

    WHY I WROTE IT:

    To decompile Peter Langston's EMPIRE game and other goodies into source
    form.  This was desired because I wanted to port the games to VMS and
    to fix some bugs in the games.

    HOW TO USE IT:

    In order to decompile object files, the files must contain certain information.
    Specifically, this decompiler only works with 4.X BSD "a.out" files
    that contain global symbol information AND relocation tables.
    It can't deal with stripped executable files or executable files
    that have no relocation table.  Any unlinked object file has the
    necessary information.

    The decompiler was motivated by a desire to get sources from some
    object files that had no sources available.  These files were
    compiled with the "cc -O" command.  No "-g" symbolic debugger
    information was available.  Therefore the decompiler was not
    designed to understand this information.  If you have files compiled
    with the "-g" switch, the decompiler won't use the extra information.

    The decompiler does not generate C source.  It generates something
    close to C source that needs some hand editing to become the
    real thing.  Writing a decompiler that does everything would be
    extremely difficult, requiring more time than the hand-editing
    needed to finish the job (at least in my case).

    The decompiler makes several passes over an object file.  The first
    pass (over the symbol table) finds function entry points.
    The next pass builds tables of parameters, local variables, register
    usage, and branch targets for each function.  The third pass breaks
    the machine instructions into basic blocks.  Two more passes mangle
    the directed graph of basic blocks into a form that represents the
    high-level language tree structure of the program.  The final pass
    prints formatted almost-C output.

    The decompiler control flow analysis knows how to make
    'if then else' statements, 'while ()' loops, 'do while ()' loops,
    and 'switch()' groups.  It knows when to generate 'break' and 'continue'
    statements.  It does not know about 'for ()' loops.  Any loops that
    do not map to a 'while()' or 'do while()' form get placed in a
    'while (1) { }' form with appropriate 'if' statements to break out
    of the loop.

    When code does not fit into any of the nicely structured forms, trusty
    old 'goto' statements and labels are used.  (Take that, N. Wirth.)

    Because of the amount of hand-munging needed to get real source code,
    some form of checking is useful.  Here's what I did when decompiling
    Empire:

      1) decompile an object file
      2) munge the decompiler output with "sed" scripts
      3) hand edit the sed output into compilable source code
      4) compile this source into object form
      5) decompile this new object file
      6) "diff" the decompiler output for my object file against the
         decompiler output of the original object file.  Look for major
         discrepencies.

    I obtained nearly error free decompilation using this method.

    WHAT IT DOES NOT DO:

    The decompiler accomplishes a lot with control flow analysis, but
    not everything.  In order to do a complete job of decompiling,
    data flow analysis must be used.  The thought of this level of
    complexity was too much for me.  Besides, the C compiler itself
    doesn't go to that much trouble.  So the decompiler doesn't do it.
    What does this mean?

    1) The decompiler doesn't know what a compound statement is.  So code
    that uses lots of scratch registers to compute compound statements
    will be decompiled into lots of simple statements that use lots
    of scratch variables.  The code is correct C, but not terribly
    intuitive.  Hand-editing is used to make improvements.

    2) The decompiler can't build argument lists for functions.
    It knows when an argument is being put on the stack, and it knows
    when a call occurs, but because of limitation (1), it can't put
    the two together.  Also, because of the lack of data flow analysis,
    it does not know when a function returns a value.  This means that
    it CANNOT GENERATE CORRECT FUNCTION CALLS or 'return' statements.
    Instead it generates a code that is obviously wrong, but visually
    very easy to see and edit into the correct form (assuming that you
    have a decent a screen editor.)  The decompiled code is of the form:

            @arg@ = foo;
            @arg@ = bar;
            @val@ = mumble( @2 args@ );

    The user is responsible for editing this into the form:

            floop = mumble( bar, foo );

    Return statements are decompiled into:

            return @value@;

    The user is responsible for determining whether register R0 contained
    a value that will be used by the caller.

    NOTE that the @arg@ statements appear in REVERSE ORDER from the
    parameter order in the function call.  Also note that the function
    call skeleton tells you the correct number of arguments.  USE THIS
    NUMBER!  Code can appear in the form:

            @arg@ = fee;
            @arg@ = fi + 1;
            @arg@ = fo;
            @val@ = fum( @2 args@ );
            @arg@ = r00l;
            @val@ = foo( @2 args@ );

    which translates to:

            foo( fum( fo, fi + 1 ), fee );

    BE SURE YOU UNDERSTAND THIS EXAMPLE before attempting to edit the
    decompiler output.  (Hint:  editing the file from the bottom up
    helps.)

    3) The decompiler can't distinguish between crappy user code and
    peephole optimizer munging.  Sometimes the peephole optimizer will
    smash two separate but similar pieces of code together.  For example,

            ...
            fprintf( stderr, "bye bye" );
            return;
            ...
            fprintf( stderr, "hi ma!" );
            return;

    may appear as

            ...
            @arg@ = D0456l;
    G0020:
            @arg@ = __iob->O025b;
            @val@ = fprintf( @2 args@ );
            return @value@;
            ...
            @arg@ = D0464l;
            goto G0020;

    See how the "fprintf( stderr, " and "return" portion of each sub-block
    was collapsed by the peephole optimizer?  Have fun with these.

    4) Integers used as unsigned types are difficult to detect.  Sometimes
    the decompiler will get it right.  The only real problem here is
    with unsigned comparisons.  To help detect problems, any unsigned
    comparisons will appear with the suffix 'u', such as in

            if ( blah < u bletch ) { ...

    This is not correct C code, but will force the user to recognize
    what is happening.  The user is responsible for checking the type
    declarations for correctness.

    5) Because VAX conditional branches use global condition codes,
    several branches can follow one conditional test.  The decompiler
    cannot repeat the source form of the test in each if statement
    because the source form may have side effects like "++" in it.
    The decompiler punts and uses the string "@prev@" to indicate that
    the if statement uses the same test as the conditional test that
    preceedes it.  The user must fix these cases.

    6) The format of Unix 4.2BSD object files, especially the values used
    in the symbol table, are poorly documented.  I determined most of
    the information used by the decompiler empirically.  No doubt, I
    missed a few cases.  Whenever the decompiler becomes confused by
    an addressing mode, global symbol information, relocation information,
    or whatever, it will print errors on stderr and will also embed
    the error messages at the proper place in the decompiled output.
    All embedded error messages contain the string "ERR".

    7) The decompiler understands VAX the indexed addressing modes,
    but cannot easily generate semantically correct source code.
    The user is responsible for examining anything that looks
    like an array reference to verify correctness.

    Note how the decompiler always uses syntatically incorrect strings
    when it can't do something.  The @blah@ form is used for things that
    are simply beyond the capabilities of the decompiler.  The "ERR"
    string is used when something unexpected occurs.  The ">=u" case
    is used to show unsigned comparisons.

    8) Some kinds of instructions are just plain difficult to turn
    directly into source code.  For example, bitfield insertion and
    extraction is not converted into source code.  Instead, the
    assembler instruction is dropped right into the decompiled code
    and the user is responsible for intuiting the data structure and
    editing the code accordingly.

    9) The structuring part of the decompiler knows about compound "if"
    statements and will try to generate these.  Normally this works
    quite well and results in very clean decompiled code.  Compound
    "if" detection fails when the "if" expression is complex enough
    to require temporary variables--the resulting code no longer
    contains adjacent tests.  Large, complex "if" statements that have
    this problem can turn into pretty messy decompiled code.

    10) The MOD (%) operator generates a small jumble of division,
    multiplication, and subtraction.  Learn to recognize this pattern
    and convert it into the simpler mod operator.

    Items (1) and (2) will cause the most trouble.  There are several other
    things you should know about the decompiler output format that will help
    you reconstruct the source program.

    a) The decompiler will always use the correct name for a symbol when
    the name appears in the global symbol table.  (Functions will always
    have the correct names.)

    When a name isn't available, the decompiler will generate one.  It
    uses a naming convention that avoids editing ambiguity problems.

    b) Labels are always of the form "Gnnnn", where 'n' is a decimal digit.
    There are ALWAYS four digits--leading zeros are used when needed.
    This makes editing much less painful (e.g. no confusion between
    "G12" and "G120".)

    c) Function arguments always appear as "Annnt", where 'n' is a decimal
    digit and 't' is a type suffix.  The 'nnn' is actually the decimal
    offset of the argument on the stack.  The type suffix indicates the data
    type of the symbol and is derived by analyzing how the code uses the
    data.  If a function uses the second argument as both an "int" and a
    "char", you will see two arguments:  A004c and A004l.  The user is
    responsible for recognizing these cases and fixing the code.  The type
    suffixes are:

            c:  char
            uc: unsigned char
            s:  short
            us: unsigned short
            l:  long (int on VAX)
            ul: unsigned long
            p:  pointer (the decompiler can't compute pointer type)
            f:  floating
            d:  double
            q:  quadword (if you get this from the 4.2 C compiler, good luck)
            ERR: something is terribly wrong--time to panic

    For the following items, assume 'n' is a decimal digit and 't' is a
    type suffix, as above.

    d) All 'static' types global to the object file appear as "Dnnnnt"
    (D stands for Data).  These variables are also declared at the
    end of the decompiled source file, with initializers.  In some cases,
    these variables represent program constants (these are marked with
    "/* const */") and the constant values can be edited back into the
    source code.  Note that CONSTANT DETECTION IS NOT RELIABLE.  If no
    code is found that writes the variable, it is assumed to be constant.
    Without data flow analysis, the decompiler can't find indirect
    references to the variable through pointers.  Treat "/* const */"
    as a hint, not a fact, and use your intuition to decide.
    Also, the initialized data declarations may contain holes, for the same
    reason that constant hints are not reliable (pointers).

    e) Local (stack) variables have the symbol format "Lnnnnt".  The
    digits 'nnnn' represent the decimal offset from the beginning of
    the stack frame.

    f) Register local variables have the symbol format "rnnt".  The 'nn'
    part is the actual register number.  Since the Unix C compiler likes
    to use register 0 as the return value from functions, and registers
    0 and 1 as the main scratch registers, you can use this information
    to intuit return values and pieces of compound statements.

    g) Pointer offsets (usually structure elements) have the symbol
    format "Onnnt".

    In all cases, the "nnn..." parts of all the above symbols are based
    on actual program structure.  For arguments ("Annnt") the number is
    the offset up the stack from the argument pointer.  For local variables
    ("Lnnnnt") the number is the offset down the stack from same.  For
    registers ("rnnt") the number is the register number.  For static data
    ("Dnnnnt") the number is based on the offset into the object file.  For
    offsets ("Onnnt") the number is the actual offset value.  All values are
    decimal.  The decompiler cannot detect implicit type casting.  In all
    cases, the user is responsible for recognizing cases where the same
    offset is used as different types.

    HACKER HINTS:

    A good hacker with lots of spare time might want to improve this
    program.  I suggest the following:

    1) Find and fix omissions in the many combinations of symbol
    and relocation types.  These are the things that generate the
    "ERR" messages.

    Any other improvements require some form of dataflow analysis.  If
    you are really dedicated and want to do this, I would strongly
    suggest doing the dataflow analysis after the basic block analysis
    (done by block()) and before any of the structuring (hier(), hll(),
    and format()).  This is because dataflow analysis could eliminate
    some of the problems encountered by the structuring.  The kinds
    of things that dataflow analysis could fix are:

    2) Get rid of temporary variables.  PCC only uses R0 and R1 as
    temporaries, so temporaries would be easy to detect.  Just be
    sure to generate source code that reflects the correct implicit
    and explicit operator precedence.  If done correctly, this would
    also fix up the compound "if" problem mentioned above.

    3) Assemble correct argument lists.  The hardest parts of this would
    be a) fixing peephole optimizer munging and b) understanding whether
    or not a function returns a value.

    These last two changes would dramatically reduce the amount of hand-
    editing needed.

    If anybody actually does improve this thing, I'd appreciate getting
    a copy of the changes.

            Jim Reuter

------------------------------------------------------------------------

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
