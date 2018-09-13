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
    Page](http://www.program-transformation.org/edit/Transform/UnivacM460?t=1536826588)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/UnivacM460)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/UnivacM460)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/UnivacM460?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/UnivacM460?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/UnivacM460?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/UnivacM460?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/UnivacM460?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/UnivacM460)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/UnivacM460?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/UnivacM460?template=oopsmore&param1=1.2&param2=1.2)
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
Univac M460 {#univac-m460 .twikiTopicTitle}
===========

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

250 *Machine-Independent Computer Programming*

    TABLE XIII
    MACHINE LANGUAGE INSTRUCTION REPERTOIRE OF THE
    UNIVAC M-46O COUNTESS COMPUTER

    FF   Function                            FF   Function
    00   Illegal                             40   Enter logical product
    01   Shift Q right                       41   Add logical product
    02   Shift A right                       42   Subtract logical product
    03   Shift AQ right                      43   Mask comparison
    04   Compare                             44   Replace logical product
    05   Shift Q left                        45   Replace add logical product
    06   Shift A left                        46   Replace subtract logical product
    07   Shift AQ left                       47   Store logical product
    10   Enter Q register                    50   Selective set
    11   Enter accumulator                   51   Selective complement
    12   Enter B register                    52   Selective clear
    13   Enter C register                    53   Substitute
    14   Store Q register                    54   Replace selective set
    15   Store accumulator                   55   Replace selective complement
    16   Store B register                    56   Replace selective clear
    17   Store C register                    57   Replace substitute
    20   Add                                 60   Arithmetic jump
    21   Subtract                            61   Manual jump
    22   Multiply                            62   Input jump
    23   Divide                              63   Output jump
    24   Add replace                         64   Arithmetic return jump
    25   Subtract replace                    65   Manual return jump
    26   Q add                               66   Input return jump
    27   Q subtract                          67   Output return jump
    30   Load A add Q                        70   Initiate repeat
    31   Load A subtract Q                   71   Index skip
    32   Add Q and store                     72   Index jump
    33   Subtract Q and store                73   Initiate input transfer
    34   Replace add Q                       74   Initiate output transfer
    35   Replace subtract Q                  75   Initiate input buffer
    36   Replace add one                     76   Initiate output buffer
    37   Replace subtract one                77   Illegal.

*Here are [MikeVanEmmerik](MikeVanEmmerik){.twikiLink}\'s **guesses**
for the j, k, and b fields:*

**j = branch condition**
:::
:::
:::
:::

0

never

1

?

2

 

3

 

4

equal to 0

5

not equal to 0

6

\>= 0

7

\< 0

**k = operand interpreter**

0

immediate yyyyy

1

indirect memory m\[m\[yyyyy\]\] ?

2

 

3

direct memory m\[yyyyy\]

4

 

5

 

6

 

7

 

**b = index designator**

0

no index

1

b

2

 

3

 

4

 

5

 

6

 

7

 

See also

-   <http://ed-thelen.org/comp-hist/UNIVAC-M-640.html>
-   <http://encyclopedia.thefreedictionary.com/Univac%20M-460>

[CategoryDecompilation](CategoryDecompilation){.twikiLink}\
[]{#TopicEnd}

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
