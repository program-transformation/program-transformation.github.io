::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
  ----------------------------------------------------------------------------------
  [![](../pub/Stratego/StrategoLogo/StrategoLogoTextlessWhite-100px.png)](WebHome)
  ----------------------------------------------------------------------------------

**[Home](WebHome){.twikiLink}**

-   [Documentation](StrategoDocumentation){.twikiLink}
-   [Language](StrategoLanguage){.twikiLink}
-   [Research Papers](StrategoPublications){.twikiLink}
-   [Applications](StrategoApplication){.twikiLink}

**[Download](StrategoDownload){.twikiLink}**

-   [Continuous build](ContinuousBuild){.twikiLink}
-   [Extensions](AdditionalPackageDownload){.twikiLink}

**[Support](StrategoSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Users Days](StrategoUsersDay){.twikiLink}
-   [Bug Reports](http://yellowgrass.org/project/StrategoXT)

**[Developers](StrategoDev){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/StrategoXT/strategoxt/trunk)
-   [Buildfarm
    results](http://hydra.nixos.org/jobset/strategoxt/strategoxt-release/all)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization?t=1536825429)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/TurningDynamicTypingIntoStaticTypingByProgramSpecialization?template=oopsmore&param1=1.4&param2=1.4)
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
K. Olmos and E. Visser. **Turning dynamic typing into static typing by
program specialization.** In D. Binkley and P. Tonella, editors, [Third
IEEE International Workshop on Source Code Analysis and Manipulation
(SCAM\'03)](http://www.brunel.ac.uk/~csstmmh2/scam2003/), Amsterdam, The
Netherlands, September 2003. IEEE Computer Society Press.
([pdf](http://www.cs.uu.nl/~visser/ftp/OV03.pdf))

### []{#Abstract} Abstract

Array processing languages such as APL, Matlab and Octave rely on
dynamic typechecking by the interpreter rather than static typechecking
and are designed for user convenience with a syntax close to
mathematical notation. Functions and operators are highly overloaded.
The price to be paid for this flexibility is computational performance,
since the run-time system is responsible for type checking, array shape
determination, function call dispatching, and handling possible run-time
errors. In order to produce effecient code, an Octave compiler should
address those issues at compile-time as much as possible. In particular,
static type and shape inferencing can improve the quality of the
generated code. In this paper we discuss how overloading in dynamically
typed Octave programs can be resolved by program specialization. We
discuss the typing issues in compilation of Octave programs and give an
overview of the implementation of the specializer in the transformation
language Stratego.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
