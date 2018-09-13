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
    Page](http://www.program-transformation.org/edit/Stratego/XDocStyleGuide?t=1536825545)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/XDocStyleGuide)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/XDocStyleGuide)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/XDocStyleGuide?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/XDocStyleGuide?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/XDocStyleGuide?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/XDocStyleGuide)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/XDocStyleGuide?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/XDocStyleGuide?template=oopsmore&param1=1.1&param2=1.1)
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
XDoc Style Guide {#xdoc-style-guide .twikiTopicTitle}
================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The [style guide for writing Javadoc
comments](http://java.sun.com/j2se/javadoc/writingdoccomments/index.html#styleguide)
is a useful starting point for a style guide for writing xDoc comments
for Stratego.

\[this guide should be rewritten to Stratego context ;) \--
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 04 Aug 2003\]

-   Okay to use phrases instead of complete sentences, in the interests
    of brevity. This holds especially in the initial summary and in
    \@param tag descriptions.
-   Use 3rd person (descriptive) not 2nd person (prescriptive). The
    description is in 3rd person declarative rather than 2nd person
    imperative.
    -   preferred: Gets the label.
    -   avoid: Get the label.
-   Strategy descriptions begin with a verb phrase. A strategy
    implements an operation, so it usually starts with a verb phrase:
    -   preferred: Gets the label of this button.
    -   avoid: This method gets the label of this button.
-   Class/interface/field descriptions can omit the subject and simply
    state the object. These API often describe things rather than
    actions or behaviors:
    -   preferred: A button label.
    -   avoid: This field is a button label.
-   Add description beyond the strategy or module name. The best names
    are \"self-documenting\", meaning they tell you basically what the
    module/strategy does. If the doc comment merely repeats the name in
    sentence form, it is not providing more information.

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
