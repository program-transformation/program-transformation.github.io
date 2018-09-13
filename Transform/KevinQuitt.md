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
    Page](http://www.program-transformation.org/edit/Transform/KevinQuitt?t=1536826510)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/KevinQuitt)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/KevinQuitt)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/KevinQuitt?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/KevinQuitt?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/KevinQuitt?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/KevinQuitt)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/KevinQuitt?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/KevinQuitt?template=oopsmore&param1=1.1&param2=1.1)
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
Kevin Quitt {#kevin-quitt .twikiTopicTitle}
===========

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

Kevin D. Quitt wrote the following, about his compiler specific
approach:

1.  The executable has to be examined to see if it\'s a compressed
    executable (like what PKLITE does) and if so, it has to be
    uncompressed. Or just exclude that type of executable, with
    information for the user. Check the copyright notice to verify the
    compiler and version are correct. A single- version decompiler could
    be expanded to multiple versions of the same compiler by using files
    containing the critical data for each\--but let\'s work on that
    later.
2.  Examine the executable for debugging information and retain this
    information, possibly in a temp file. This can help us detect
    libraries and recover variable and function names. Build a
    linked-list that keeps track of what regions of the program are
    known (fully or partially), and, therefore, which are not known.
    Each node should have the type of memory (code/data), name of the
    function/storage if available and type of code (library/user).
3.  Determine the starting point of the executable (past the C startup
    code), this gives us `int main( int argc, char *argv[]`\" \--we\'re
    on our way! More importantly, the startup code tells us where
    initialized variables are and the initial values for them. We don\'t
    know, at first, the size or types of these variables; examining the
    initializing data can help us find floats, doubles, character
    strings, and maybe int types. By looking for repeating patterns of
    type/size entries, we can (tentatively) identify arrays of standard
    types and of structures. We will differentiate between arrays and
    multiple scalar variables in a row by examining the code that
    addresses them.
4.  The next step is disassembly: follow the flow of main, noting the
    addresses of the functions called and the starting addresses of
    executed instructions. Areas of confusion (where a goto is aimed at
    the middle of an instruction) must be in-line assembly (and get
    marked as such) since we always follow program execution. A warning
    issued when this is seen is probably a good idea; we may be lost
    already. See if the functions called correspond to anything in the
    information list. Then, for repeat recursively for each routine
    called, checking the information list, and comparing the code to the
    library for that compiler. Any known library modules can be
    eliminated from further consideration, except when one library
    function calls another; then we can eliminate the called function(s)
    as well, etc. By knowing what the various INTs do, we can determine
    areas that are data. When this process is done (and it may take
    several passes), we have developed a tremendous information tree
    about the executable, and we can produce an intermediate
    assembly-language file that has the library stripped out (even if
    there was no debugging information), initialized static variables
    identified along with their initial values.
5.  Once we have the disassembled version, along with our information
    list, we can start the actual decompilation process. I would use a
    branching linked list; each node would indicate the name of the
    function (determined from debug information or synthesized), and a
    pointer to the code list for that function. The code list node
    contains the type of code contained (source, binary, or in-line
    assembly), a pointer to memory that contains the ASCII source, and a
    pointer to the un-disassembled binary. As code is disassembled, the
    code list entries split and merge; when the entire function is
    disassembled, there is a single code list entry. The binary is
    retained until the entire function has been disassembled.
6.  Concentrate on one function at a time, not following function calls.
    The entry code to the function tells us about the automatic
    variables, and examination of the code will reveal the size and
    probably the type as well. The same type of analysis as for the
    initialized variable area can be used to locate structs.
7.  The second pass for a function is to identify function calls and the
    code that passes parameters to the function. For those values passed
    that are not simple load/push operations, we create a new code node
    containing the code that generates the value that does get pushed.
    For functions whose parameter types are know, we can adjust our
    information about the variables involved (e.g., identifying a
    \"`FILE *`\" variable). This is a form of pattern matching, but
    should be done before that step to make it easier later.
8.  Pass three is template matching, for whatever templates have been
    determined for the compiler. As code segments are identified as to
    the source, a code node is created that adds the generating source
    code to the binary. Template matching must be done recursively to
    handle loops within loops, etc. The setup code for loops either
    identifies them as for, while, or do, or the loop type doesn\'t
    matter and we can choose arbitrarily. This will pick up switches,
    cases, ifs, and function calls turned into in-line code by
    \"\#pragma inline\" statements. When \#pragma controlled code is
    encountered, the appropriate \#pragma statement must be put in the
    source; the actual location depends on whether the \#pragma can be
    used is a local block of code, or only for the entire file (and is
    there a corresponding \#pragma that turns it off).
9.  Pass four looks for in-line code that has a direct source
    representation and adding the source to the code node. This is code
    that picks up one or more variables, does something to them, and
    puts one or more values back. Attention must be paid to the sources
    of register variables (from the automatic pool) so that source can
    correctly identify the original variable. The conditional in \"if\"
    statements can be determined at this point since we can now identify
    the (immediate) source of the comparison.
10. Anything left over at this point can probably be safely turned into
    in-line assembly code. In any case, that\'s the ultimate fall-back
    position.

Although he thinks that dcc will be better than exec-2-c, he doubts
whether their approach will lead to better results than his, both with
respect to reconstructing the original work-flow, and with respect to
reconstructing the data type information. He commented: *In theory,
theory is the same as practice\--in practice, it\'s not.*

Kevin worked on this in the past for his own, and is perfectly willing
to discuss the decompilation process with anybody and tell them his
ideas and suggestions for various techniques and processes. He has some
scattered programs that he used to test out individual ideas, but does
not have a set of files that he would call \`source for a decompiler\'.

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
