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
    Page](http://www.program-transformation.org/edit/Sdf/SdfToTable?t=1536826212)
-   [Rename
    Page](http://www.program-transformation.org/rename/Sdf/SdfToTable)
-   [Attach
    File](http://www.program-transformation.org/attach/Sdf/SdfToTable)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Sdf/SdfToTable?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Sdf/SdfToTable?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Sdf/SdfToTable?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Sdf/SdfToTable?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Sdf/SdfToTable?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Sdf/SdfToTable?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Sdf/SdfToTable?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Sdf/SdfToTable?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Sdf/SdfToTable)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Sdf/SdfToTable?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Sdf/SdfToTable?template=oopsmore&param1=1.6&param2=1.6)
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
Sdf To Table {#sdf-to-table .twikiTopicTitle}
============

::: {.twikiWebTitle}
Sdf
:::

[]{#Name} Name
--------------

sdf2table

[]{#Synopsis} Synopsis
----------------------

sdf2table \[-m ma\[-s\] \[-i sdf-definition\] \[-o parse-table\]

[]{#Description} Description
----------------------------

The utility sdf2table generates a parse table from an SDF syntax
definition.

The syntax definition is required to be in the SDF2 format.

[]{#Options} Options
--------------------

input and output
:::
:::
:::
:::

-i

*file*

input from *file* (default: all file arguments)

-o

*file*

output to *file* (default: *inputfile*.tbl)

-m

*name*

parse table is generated for module *name* (default: Main)

output format

-b

 

write output in Binary [AsFix](../Tools/AsFix){.twikiLink} (BAF) format

-t

 

write output in plain text format

control operation

-n

 

only normalization of grammar

-s

 

check sdf definition and show warnings on stderr

runtime information

-l

 

display statistic information

-v

 

verbose mode

meta information

-h

 

display help information (usage)

-V

 

reveal program version (i.e. 1.13)

[]{#See_also} See also
----------------------

-   [SGLR](SGLR){.twikiLink}

\
[]{#TopicEnd}

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Sdf.SdfToTable moved from Sdf.Sdf2TablePGEN on 17 Feb 2004 - 11:33 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Sdf/SdfToTable?newweb=Sdf&newtopic=Sdf2TablePGEN&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
