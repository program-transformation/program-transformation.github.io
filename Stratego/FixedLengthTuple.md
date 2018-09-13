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
    Page](http://www.program-transformation.org/edit/Stratego/FixedLengthTuple?t=1536825582)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/FixedLengthTuple)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/FixedLengthTuple)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/FixedLengthTuple?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/FixedLengthTuple?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    9](http://www.program-transformation.org/view/Stratego/FixedLengthTuple?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Stratego/FixedLengthTuple?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Stratego/FixedLengthTuple?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Stratego/FixedLengthTuple?rev1=1.8&rev2=1.7)
-   [Rev
    7](http://www.program-transformation.org/view/Stratego/FixedLengthTuple?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/FixedLengthTuple?rev1=1.7&rev2=1.6)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/FixedLengthTuple)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/FixedLengthTuple?template=oopsmore&param1=1.9&param2=1.9)
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
    \...](http://www.program-transformation.org/oops/Stratego/FixedLengthTuple?template=oopsmore&param1=1.9&param2=1.9)
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
Fixed Length Tuple {#fixed-length-tuple .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

A tuple is a term of the form `(t1,...,tn)`.

In pre- [StrategoRelease07](StrategoRelease07){.twikiLink} versions of
Stratego this was syntactic sugar for `TCons(t1,...,TCons(tn,TNil))`.
The idea behind this representation is the ability to define generic
operations on tuples (as heterogenous lists). A typing scheme for such
tuples was based on the stratified type system of
[MultiLevelSpecifications](../Transform/MultiLevelSpecifications){.twikiLink}.
However, a type system for Stratego based on these ideas never
developed. Furthermore, the binary representation for tuples is hard to
read in printed ATerms and is rather expensive since it requires
multiple operations for matching and allocation.

Another reason for this represention was that the
[ATermLibrary](../Tools/ATermLibrary){.twikiLink} did not support tuple
syntax, i.e., applications without a constructor. Based on the
observation that a tuple really is an application of the constructor
with the empty name, [HaycoDeJong](../Transform/HaycoDeJong){.twikiLink}
extended the [ATermLibrary](../Tools/ATermLibrary){.twikiLink} such that
`(t1,...,tn)` is now a proper ATerm.

Fixed length tuples are supported starting with
[StrategoRelease07](StrategoRelease07){.twikiLink}.

With the introduction of fixed length tuples the
[PairConstructor](PairConstructor){.twikiLink} becomes obsolete.

**Migration**

The change in representation affects existing specifiations. Here are
several scenarios and actions to be taken to migrate to the new
situation.

-   No Tuples: No need to do anything

<!-- -->

-   Tuples in specification: If tuples are used only internally then it
    suffices to recompile the specification. Already compiled C code
    should still work.

<!-- -->

-   Tuples in external data: If tuples are used externally (written to
    file), it will be necessary to recompile the specification and
    regenerate all data files.

<!-- -->

-   Tuples manipulated through `TCons` and `TNil`: Rewrite the parts of
    the specification using these constructors. See module `tuple.r` for
    some techniques to replace the generic operations.

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 06 Jan 2002

------------------------------------------------------------------------

Implement tuples by means of \"\" constructor instead of TCons/TNil (and
use (,,\_) notation)

\-- [EelcoVisser](EelcoVisser){.twikiLink} - 27 Oct 2001

The [ATermLibrary](../Tools/ATermLibrary){.twikiLink} has been modified
to support tuple syntax thanks to
[HaycoDeJong](../Transform/HaycoDeJong){.twikiLink}. Now it is a matter
of changing the representation of tuples in the compiler. The change is
rather easy, but the problem is that it will break existing code
depending on the `TCons/TNil` representation. This requires an impact
analysis. I expect there is little use.

This feature will be introduced in
[StrategoRelease07](StrategoRelease07){.twikiLink}

\-- [EelcoVisser](../Main/EelcoVisser){.twikiLink} - 22 Nov 2001\

------------------------------------------------------------------------

[CategoryDone[^?^](http://www.program-transformation.org/edit/Stratego/CategoryDone?topicparent=Stratego.FixedLengthTuple)]{.twikiNewLink
style="background : #FFFFCE;"} \|
[LanguageExtensions](LanguageExtensions){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Stratego.FixedLengthTuple moved from Stratego.FixedLengthTuples on 06
Jan 2002 - 17:21 by [EelcoVisser](../Main/EelcoVisser){.twikiLink}* -
[put it
back](http://www.program-transformation.org/rename/Stratego/FixedLengthTuple?newweb=Stratego&newtopic=FixedLengthTuples&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
