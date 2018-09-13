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
    Page](http://www.program-transformation.org/edit/Transform/AspectOrientedProgrammingReview?t=1536826428)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/AspectOrientedProgrammingReview)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/AspectOrientedProgrammingReview)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/AspectOrientedProgrammingReview?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/AspectOrientedProgrammingReview?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/AspectOrientedProgrammingReview?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/AspectOrientedProgrammingReview)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/AspectOrientedProgrammingReview?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/AspectOrientedProgrammingReview?template=oopsmore&param1=1.1&param2=1.1)
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
Aspect Oriented Programming Review {#aspect-oriented-programming-review .twikiTopicTitle}
==================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

**Aspect-Oriented Programming**

by
[GregorKiczales[^?^](http://www.program-transformation.org/edit/Transform/GregorKiczales?topicparent=Transform.AspectOrientedProgrammingReview)]{.twikiNewLink
style="background : #FFFFCE;"},
[JohnLamping[^?^](http://www.program-transformation.org/edit/Transform/JohnLamping?topicparent=Transform.AspectOrientedProgrammingReview)]{.twikiNewLink
style="background : #FFFFCE;"},
[AnuragMendhekar[^?^](http://www.program-transformation.org/edit/Transform/AnuragMendhekar?topicparent=Transform.AspectOrientedProgrammingReview)]{.twikiNewLink
style="background : #FFFFCE;"},
[ChrisMaeda[^?^](http://www.program-transformation.org/edit/Transform/ChrisMaeda?topicparent=Transform.AspectOrientedProgrammingReview)]{.twikiNewLink
style="background : #FFFFCE;"},
[ChristinaVideiraLopes[^?^](http://www.program-transformation.org/edit/Transform/ChristinaVideiraLopes?topicparent=Transform.AspectOrientedProgrammingReview)]{.twikiNewLink
style="background : #FFFFCE;"},
[JeanMarcLoingtie[^?^](http://www.program-transformation.org/edit/Transform/JeanMarcLoingtie?topicparent=Transform.AspectOrientedProgrammingReview)]{.twikiNewLink
style="background : #FFFFCE;"} and
[JohnIrwin[^?^](http://www.program-transformation.org/edit/Transform/JohnIrwin?topicparent=Transform.AspectOrientedProgrammingReview)]{.twikiNewLink
style="background : #FFFFCE;"}.

In *Proceedings of the European Conference on Object-Oriented
Programming ([ECOOP](ECOOP){.twikiLink}\'97)*.
[LectureNotesInComputerScience](LectureNotesInComputerScience){.twikiLink}
1241, Springer-Verlag, June 1997.

------------------------------------------------------------------------

**Summary**

\-- [MartijnSchrage](MartijnSchrage){.twikiLink}

Even though the object-oriented programming (OOP) model provides a good
fit for many real domain problems, some problems cannot be captured
effectively with either OOP or procedural approaches. System design
normally takes place by breaking up the system in increasingly smaller
units, until the behaviour of these units can be captured by actual
abstractions, or generalized procedures, in a programming language. The
abstractions are then combined again to form the system. However, some
kinds of behaviour do not follow this functional decomposition of the
system and are therefore difficult to implement elegantly using the
normal design process.

An example of this can be found in an image processing system that
consists of a number of filters. Primitive filters are implemented as
loops over the input images, and higher-level filters are implemented by
combining primitive filters. This leads to a transparent and easy to
maintain implementation, but repeated calls to primitive filters can
cause many intermediate images to be created that only exist briefly
before they are fed into other filters. Optimizing the code for this
problem requires fusing loops together and results in tangled code that
is difficult to read and to maintain. The problem is that the condition
on which loops can be fused is based on the data flow graph, instead of
on the functional decomposition graph, and that these two graphs compose
differently. The loop fusion property, which is an aspect, is said to
cross cut the functional decomposition of the system.

Properties may be split into two categories: aspects and components.
Components are properties that can be cleanly encapsulated by a
generalized procedure, whereas aspects cannot be cleanly encapsulated.
Examples of aspects are failure handling, performance, and memory access
patterns. Aspect-oriented programming (AOP) allows separate
specification of the components as well as of the aspects of the program
and combines these specifications automatically in a process called
aspect weaving. Important to the aspect weaving is the concept of join
points, which are the parts of the semantics of the component programs
that the aspect programs coordinate with. In the image processing
example, the join points are the data flows of the filter components.

The implementation of a system involves programming the components in a
component language and writing one or more aspect programs in one or
more aspect languages. Furthermore, the aspect weaver for the specific
combination of component and aspect languages has to be written, but it
might be reused for other applications using the same combination of
languages.

Using the aspect-oriented approach, the image filters of the example are
written in a special component language that makes the loop structure of
each filter explicit. An aspect program can examine the structure of the
data flow graphs of the filters and reduce them by fusing loops
together. The resulting program can then be compiled to an actual
implementation. All these steps take place in the aspect weaver.

The systems that have been re-implemented using AOP tended to be smaller
than their OOP counterparts, and perform about equally well. However, no
large experimental studies have been performed yet. An important area of
research is an assessment of the actual benefits of AOP. As a starting
point, current systems can be examined for presence of AOP elements in
their design. Other research areas include the development of a
collection of aspect and component languages for different applications,
the development of theoretical support and training methods for AOP, and
the integration of AOP with current approaches. The field of
aspect-oriented programming is related to reflection and metaobject
protocols, program transformation, and subjective programming.

------------------------------------------------------------------------

[CategoryReview](CategoryReview){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
