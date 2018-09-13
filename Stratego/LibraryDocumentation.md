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
    Page](http://www.program-transformation.org/edit/Stratego/LibraryDocumentation?t=1536825596)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/LibraryDocumentation)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/LibraryDocumentation)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/LibraryDocumentation?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/LibraryDocumentation?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    4](http://www.program-transformation.org/view/Stratego/LibraryDocumentation?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/LibraryDocumentation?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/LibraryDocumentation?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/LibraryDocumentation?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/Stratego/LibraryDocumentation?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Stratego/LibraryDocumentation?rev1=1.2&rev2=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/LibraryDocumentation)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/LibraryDocumentation?template=oopsmore&param1=1.4&param2=1.4)
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
    \...](http://www.program-transformation.org/oops/Stratego/LibraryDocumentation?template=oopsmore&param1=1.4&param2=1.4)
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
Library Documentation {#library-documentation .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

The documentation of [Stratego Standard
Library[^?^](http://www.program-transformation.org/edit/Stratego/StrategoStandardLibrary?topicparent=Stratego.LibraryDocumentation)]{.twikiNewLink
style="background : #FFFFCE;"} must be improved. You can help with this
in two ways:

-   If you have to you think longer than 10 seconds about what a
    strategy in the SSL actually does, **please** write your
    understanding down and send it to the stratego-dev mailing list. One
    of the maintainers will add your contribution to the sources.
    Preferable use an
    [xDoc](ExtendibleDocumentationGenerator){.twikiLink} documentation
    comment, but plain text descriptions are welcome as well.

<!-- -->

-   If you contribute a new strategy to the library you **must**
    document it if you want your contribution to be useful. Of course
    you should use an
    [xDoc](ExtendibleDocumentationGenerator){.twikiLink} documentation
    comment for this.

A documentation comment should consist of

-   One line description of what the strategy does.
-   Optional some paragraphs where you explain the strategy in more
    details. It is useful to include some example applications and the
    expected result of these applications.
-   Use \@param to describe the purpose of term and strategy arguments
-   Use \@type to specify the type of the strategy and its term and
    strategy arguments
-   Use \@since to specify from which release the strategy has been be
    available

e.g.

    /**
     * Generates lists of numbers.
     * 
     * The given end point is never part of the generated list; <range> 10 generates a list of 10 values, 
     * exactly the legal indices for items of a sequence of length 10. It is possible to let the range 
     * start at another number.
     *
     * <range> 10 => [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
     * <range> (5, 10)     => [5, 6, 7, 8, 9]
     *
     * The documentation of the range strategy is partly copied from the Python tutorial.
     *
     * @since 0.9.3
     * @type Int * Int -> [Int]
     */

For useful tips and conventions for writing descriptions in doc comments
see [xDoc style guide](XDocStyleGuide){.twikiLink}.

------------------------------------------------------------------------

[]{#Discussion} Discussion
--------------------------

This is an excellent idea. I have a few comments.

Including example applications is fine, but if they are just comments
they tend not to be maintained properly and may contain syntactic and
semantic errors. Would it be an idea to make the examples more formal,
i.e., with an official syntax, and derive unit tests from them?

Examples are fine for small strategies, but more complicated for more
complex strategies. An early version of the rename-vars module contained
a complete example application in comment. The problem of examples in
comments increases considerable for such large examples. It might be
useful to recognize examples that are provided in a separate module. For
instance, one can imagine having a subdirectory full of examples for
some module, as well as unit tests.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 03 Aug 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
