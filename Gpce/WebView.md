::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
![gpce-logo.jpg](../pub/Gpce/WebLeftBar/gpce-logo.jpg){width="100"
height="120"}

**[Home](WebHome){.twikiLink}**\
[GPCE\'04](../Gpce04/WebHome){.twikiLink}\
[GPCE\'05](../Gpce05/WebHome){.twikiLink}\
[GPCE\'06](../GPCE06/WebHome){.twikiLink}\
[GPCE\'07](../GPCE07/WebHome){.twikiLink}\
[GPCE\'08](../GPCE08/WebHome){.twikiLink}\
[GPCE\'09](../GPCE09/WebHome){.twikiLink}\
[GPCE\'10](../GPCE10/WebHome){.twikiLink}\
[GPCE\'11](../GPCE11/WebHome){.twikiLink}\
[GPCE\'12](../GPCE12/WebHome){.twikiLink}\
[GPCE\'13](../GPCE13/WebHome){.twikiLink}\
[GPCE\'14](../GPCE14/WebHome){.twikiLink}\
[GPCE\'15](http://conf.researchr.org/home/gpce2015)\
\
[Gpce Bylaws](GpceBylaws){.twikiLink}\
[Steering Committee](SteeringCommittee){.twikiLink}\
\
[GPCE Organizers](../Gpceorg/WebHome){.twikiLink}
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Gpce/WebView?t=1536828019)
-   [Rename
    Page](http://www.program-transformation.org/rename/Gpce/WebView)
-   [Attach
    File](http://www.program-transformation.org/attach/Gpce/WebView)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Gpce/WebView?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Gpce/WebView?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/Gpce/WebView?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Gpce/WebView?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Gpce/WebView?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Gpce/WebView?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Gpce/WebView?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Gpce/WebView)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Gpce/WebView?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/Gpce/WebView?template=oopsmore&param1=1.3&param2=1.3)
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
WebView {#webview .twikiTopicTitle}
=======

::: {.twikiWebTitle}
Generative Programming: Concepts and Experience
:::

Welcome to the [Rice PLT](http://www.cs.rice.edu/CS/PLT/) project on

[]{#Resource_Aware_Programming_RAP}[]{#Resource_Aware_Programming_RAP_} Resource Aware Programming (RAP)
========================================================================================================

Languages for embedded software

/pub/Gpce/WebView/emsp.gif

[]{#Introduction} Introduction
------------------------------

[This research group explores the impact of state-of-the-art programming
languages techniques such as multi-stage programming in embedded
systems. Multi-stage languages already provide significant safety
guarantees. For example, a program generator written in such a language
not only is type-safe in the traditional sense, but we are guaranteed
that any generated program will also be type safe. This provides a
noteworthy degree of assurance about the quality of the generated code.
But like most traditional high-level programming techniques, multi-stage
programming was designed to satisfy functional requirements rather than
operational ones, and existing multi-stage languages do not provide any
guarantees about the behavior of programs in the presence of bounded
resources. The challenge in this setting is ensuring that the generated
programs are suitable for execution on an embedded platform. ]{lang="EN"
style="font-family:Arial;"}

[Our current focus is on ways to address this problem by strengthening
\`\`traditional\'\' multi-stage type systems using (mainly) foundational
techniques from type theory and functional reactive programming (FRP) to
create a paradigm of resource-aware multi-stage programming. Linear and
alias types (in conjunction with dependent typing) will be used to
ensure space-boundedness, new typing techniques are used to ensure
time-boundedness, and signals and behaviors from FRP allow for a natural
style of reactive
programming.]{style="font-family:Arial;"}[]{style="font-family:Arial"}

[]{#Publications} Publications
------------------------------

-   Functional Programming for Real Applications, Invited Paper
    ([ES'01](http://www.cs.rice.edu/~taha/publications/conference/es01.pdf))

### []{#Resource_Aware_Programming_span}[]{#Resource_Aware_Programming_span_} [Resource Aware Programming]{style="font-family:Arial"}

-   Event-driven FRP
    ([PADL'02](http://www.cs.rice.edu/~taha/publications/conference/padl02.pdf))

<!-- -->

-   Real-Time FRP
    ([ICFP'01](http://www.cs.rice.edu/~taha/publications/conference/icfp01b.pdf))

[These papers are also available in dvi and ps
[formats](http://www.cs.rice.edu/~taha/publications.html).]{style="font-family:Arial"}

[]{#Related_Systems_span}[]{#Related_Systems_span_} [Related Systems]{style="font-family:Arial"}
------------------------------------------------------------------------------------------------

-   [MetaOCaml](http://www.metaocaml.org):A compiled, multi-stage OCaml

[]{#Openings_span}[]{#Openings_span_} [Openings]{style="font-family:Arial"}
---------------------------------------------------------------------------

-   [Postdoctoral Research
    Scientist](http://www.cs.rice.edu/~taha/RAP/openings.txt)

[]{#Team_Members_span}[]{#Team_Members_span_} [Team Members]{style="font-family:Arial"}
---------------------------------------------------------------------------------------

-   [Walid Taha](http://www.cs.rice.edu/~taha/)
-   [Stephan Ellner](http://www.owlnet.rice.edu/~besan/)

[]{#Acknowledgments_span}[]{#Acknowledgments_span_} [Acknowledgments]{style="font-family:Arial"}
------------------------------------------------------------------------------------------------

Supported by NSF ITR [\"A Framework for Rapid Development of Reliable
Robotics
Software\"](https://www.fastlane.nsf.gov/servlet/showaward?award=0205542)
:::

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
