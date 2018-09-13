::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![gpce-logo.jpg](../pub/GPCE11/WebLeftBar/gpce-logo.jpg){width="100"
height="120"}

**[GPCE Home](http://program-transformation.org/Gpce)**\
**[GPCE\'11 Home](WebHome){.twikiLink}**\
[Keynotes](KeynoteSpeakers){.twikiLink}\
[Schedule](ConferenceProgram){.twikiLink}\
[Accepted Papers](AcceptedPapers){.twikiLink}\
[Tech Talks](TechTalks){.twikiLink}\
[Poster](Poster){.twikiLink}\
[Banner](Banner){.twikiLink}\
[Organization](ConferenceOrganization){.twikiLink}\
[Dates](ImportantDates){.twikiLink}\
[Venue](ConferenceVenue){.twikiLink}\
[Registration](ConferenceRegistration){.twikiLink}\

**Calls for**\
[Papers](CallForPapers){.twikiLink}\
[Tech Talks](CallForTechTalks){.twikiLink}\
[Workshops](Workshops){.twikiLink}

**[Electronic\
Submission](http://www.easychair.org/conferences/?conf=gpce11)**\
(Submission deadline has passed)\
\
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/GPCE11/EfficientExtractionAndAnalysisOfPreprocessorBasedVariability?t=1536828818)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE11/EfficientExtractionAndAnalysisOfPreprocessorBasedVariability)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE11/EfficientExtractionAndAnalysisOfPreprocessorBasedVariability)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE11/EfficientExtractionAndAnalysisOfPreprocessorBasedVariability?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE11/EfficientExtractionAndAnalysisOfPreprocessorBasedVariability?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/GPCE11/EfficientExtractionAndAnalysisOfPreprocessorBasedVariability?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE11/EfficientExtractionAndAnalysisOfPreprocessorBasedVariability)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE11/EfficientExtractionAndAnalysisOfPreprocessorBasedVariability?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/GPCE11/EfficientExtractionAndAnalysisOfPreprocessorBasedVariability?template=oopsmore&param1=1.1&param2=1.1)
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
Efficient Extraction and Analysis of Preprocessor-Based Variability {#efficient-extraction-and-analysis-of-preprocessor-based-variability .twikiTopicTitle}
===================================================================

::: {.twikiWebTitle}
Julio Sincero, Reinhard Tartler
:::

**Abstract**: The CPP is the dominant tool of choice for the
implementation of variability in large-scale configurable software.
Linux, probably the most-configurable piece of software ever, employs
more than 10,000 preprocessor variables for this purpose. However, this
de-facto variability tends to be \`\`hidden in the code\'\'; which on
the long term leads to varibility defects, such as dead code or
inconsistencies with respect to the intended (modelled) variability of
the software. This calls for tool support for the efficient extraction
of (and reasoning over) CPP-based variability.

We suggest a novel approach to extract CPP-based variability. Our tool
transforms CPP-based variability in O(n) complexity into a propositional
formula that \`\`mimics\'\' all valid effects of conditional compilation
and can be queried with standard SAT or BDD packages.

Our evaluation results demonstrate the scaleability and practicability
of the approach. A dead-block-analysis on the complete Linux source tree
takes less than 15 minutes; we thereby have revealed 4 defects, 2 of
which meanwhile have been confirmed as new (and long-lasting) bugs.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
