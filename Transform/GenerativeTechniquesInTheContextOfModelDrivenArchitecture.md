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
    Page](http://www.program-transformation.org/edit/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture?t=1536826491)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Transform/GenerativeTechniquesInTheContextOfModelDrivenArchitecture?template=oopsmore&param1=1.6&param2=1.6)
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
Generative Techniques In The Context Of Model Driven Architecture {#generative-techniques-in-the-context-of-model-driven-architecture .twikiTopicTitle}
=================================================================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

The first workshop on this topic was very successful, resulting in the
[GenerativeModelTransformer[^?^](http://www.program-transformation.org/edit/Transform/GenerativeModelTransformer?topicparent=Transform.GenerativeTechniquesInTheContextOfModelDrivenArchitecture)]{.twikiNewLink
style="background : #FFFFCE;"} project. A second workshop is scheduled
for 27 October at [OOPSLA](OOPSLA){.twikiLink} 2003,
<http://www.softmetaware.com/oopsla2003/mda-workshop.html>.

------------------------------------------------------------------------

This page started with the raw notes from the
[OOPSLA](OOPSLA){.twikiLink}\'2002 workshop on this topic, see
<http://www.softmetaware.com/oopsla2002/mda-workshop.html>. Please
refactor as appropriate and add depth to the discussion topics.

------------------------------------------------------------------------

[]{#Domain_Modeling_and_Transformati} Domain Modeling and Transformation Specification
--------------------------------------------------------------------------------------

-   Eric Engstrom
-   Jorn Bettin
-   Ghica Van Emde Boas
-   Dean Wampler
-   Wei Zhao
-   Krzystof Czarnecki

### []{#Topics} Topics

1.  Transformation languages
    1.  Visual/ Textual
    2.  Different types Tree re
    3.  Power
    4.  Usability
    5.  Scalability
        1.  How does visual scale
    6.  Composition
    7.  Modularization
    8.  Transformation complexity
        1.  Template language? (What role)
        2.  Linear / graph
        3.  Typed / untyped language (c++ templates vs Template Language
            TL)
    9.  Recording to transformation
2.  Domain modeling
    1.  Breadth of domain
    2.  Family modeling
    3.  Separation of concerns
    4.  Life cycle of the [MDA](MDA){.twikiLink} (business to design to
        develop)
    5.  Aspects
3.  Platform modeling
    1.  What is a PSM vs PIM.
    2.  Executable
    3.  Different layers of models w/wo different aspects
    4.  Domain Language and Transformation coupling
4.  Output Executable
    1.  Quality
    2.  Meet requirements
5.  Big picture of [MDA](MDA){.twikiLink}
    1.  Guidelines (given by [MDA](MDA){.twikiLink})
    2.  Development process (given by [MDA](MDA){.twikiLink})
    3.  Tools (needs to be developed)
    4.  Techniques (needs to be developed)
6.  Component Acquisition business

------------------------------------------------------------------------

[]{#Why_LEGO_Blocks_don_t_work} Why LEGO Blocks don\'t work
-----------------------------------------------------------

### []{#Topics} Topics

1.  Software components are not physical things
2.  Parameterization
3.  Components as parameters
4.  Components don't work because of lack of specification?
5.  Is Adaptability domain specific?
6.  Does static typing impede adaptability?
    -   Adaptability is moving components from one context to another
    -   A component reacts to context change and adapts itself
        (internal)
7.  Component should be black box?
8.  Layering
9.  Runtime vs. construction time adaptability
10. Type objects are a runtime construct versus simple classes generated
    at compile time
11. System functions, ui functions, etc [MDA](MDA){.twikiLink}....
12. Annotate models with extra information about mappings
13. Dead specification removal
14. No need for inheritance if code is synthesized...
15. Has-a is more reusable (pluggable)
16. Is inheritance generalization or specialization?
17. Difference in Context is the common culprit
18. We can't envision every possible variation up front
19. Wrapping, extending
20. Dynamic code loading, runtime reflection
21. Aspects!
22. What's a component in the context of [MDA](MDA){.twikiLink}
    -   well defined interface
    -   well specified interaction
    -   configuration port?
23. Reflection is not the bottleneck in most systems
24. In [MDA](MDA){.twikiLink}, a components is most probably OMG
    component specification!
25. Black boxes CAN be adaptive! It can have configuration parameters
    that completely change its behavior. State models inside components.
26. RT needs only and/or tree as hierarchical decomposition

OMG is Oh My God 

1.  Yoder: There is no generic domain independent adaptivity "language"
2.  Yunker: The more fine-grained the components the more intelligence
    is needed in the assembly process.
3.  Adaptability is a recursive problem
4.  We don't have tools that support it.
5.  At what point does [MDA](MDA){.twikiLink} meet up with a component
    infrastructure?
6.  Should [MDA](MDA){.twikiLink} generate every little aspect of the
    entire system?
7.  Platform specific services are not generated, nor is it needed.

<!-- -->

1.  Your generated system has to interact with other non generated
    systems which are viewed as "interfaces" or services, but generated
    system and thus the generator has to know about them.
2.  It all hinges on the definition of "Component" and "Adaptability"
3.  A component has communication interfaces and configuration
    interfaces.
4.  Separation of concerns and put them in a container (security, fault
    tolerance, load balancing, etc. systemic aspects). Keep them out of
    the component. This way a component can adapt to those concerns
    because the container allows it to.
5.  Adaptability of systemic aspects is relatively well understood and
    implementable with existing technology. Adaptability of business
    functionality is not so straightforward.
6.  N + M versus N\*M problem

### []{#Conclusion} Conclusion

LEGO BLOCKS COULD WELL WORK IF they are adaptive to context. Adaptivity
of systems aspects is easier to achieve than that of business aspects.

------------------------------------------------------------------------

[]{#Aspects} Aspects
--------------------

### []{#Summary} Summary

An important goal of modeling is to deal with the non-linearity in
software: the size in the change in requirements should be proportional
to the change in the implementation. The word "aspect" may not have a
precise definition, but it generally refers to design decisions that are
non-local relative to a given viewpoint

A model is an instance of a meta-model, which defines its notation and
semantics. There is a stack of meta-models which usually stop after 3 or
4 levels, and

Current practice is that models are integrated by a "model weaver" which
interprets/compilers the models and implements their semantics. The
meta-models are generally implicit.

Creating modular "weavers" which allow composition of models based on
their meta-models is an important research direction. Creating
correspondence models that define the semantics of model integration is
one possible approach.

Models can be used at runtime: dynamic interpretation of models that can
be modified by users and reflection to explain programs behavior.

Is there any reason to keep the models around at runtime

1.  If the user wants to change the models
2.  Reflection. Context-dependent help that is based on the state of the
    model, not just on the runtime information. In Word you can only
    print one document at a time. When you want to explain why the Print
    menu is grayed out.

### []{#What_is_an_aspect}[]{#What_is_an_aspect_} What is an aspect?

System Data UI process workflow security workflow

Viewpoint?

Can you define a system without a domant decompisition?

Is exception handling componentizable.

Setting up a domanant decomposition

Aspect-oriented programming

Aspects are things that cross-cut

### []{#How_do_you_combine_models}[]{#How_do_you_combine_models_} How do you combine models?

The meta-model semantics defines the behavior. Single compiler that
knows about all the models.

Each model is written the language of the meta-model.

Java program P (meta model is Java) [UML](UML){.twikiLink} model of the
program ([UML](UML){.twikiLink} is model) The trace is a specific
execution of the system.

What is static system? The program is static Models are declarative, but
they define

With a GUI of the system, the drawing is a model? will the meta-model
talk about position, layout, etc and the widgets. to create a
meta-model,

[UML](UML){.twikiLink} 2.0 separation of content and presentation in
modeling

### []{#Questions} Questions

Most software development begins with use cases, and CRC cards. Are they
models? Sure, they have structure, so they are models but they are not
integrated models:

-   if you define them precisely as specifications (pre/post conditions)
    then you do have a precise model. When you have precise definitions,
    you can advance very rapidly.
-   If you want to extend/change the meta-model, then you may be ok, but
    if you want to change the domain, then you have a lot of work.

The purpose of the compiler is to restrict the set of allowed
description so that they can control what people say?

What are the hard questions:

How do you provide models, you may lose expressiveness.

If you have an existing system, how do you go about integrating an new
aspect. Had to tag on a specific kind of event logging. Went through the
system and added before/after events in a system. Also useful for
business logic.

Had to add multi-national to the existing system. Change the compiler
and then everything.

Different kind of modularity: instead of splitting system up into
components, split it into a model compiler and then a set of models.

Microsoft has a tool to generate C\# from Java. In Java if you have a
method that is visible but the visibility rule is different. Their
translation is more restrictive than Java.

You could also go from Java to [UML](UML){.twikiLink}, then
[UML](UML){.twikiLink} -\> [UML](UML){.twikiLink} and then from
[UML](UML){.twikiLink} to C\#.

There is no modularity at the meta-model level.

We have some customers that will not allow JVM, others will not allow
anything from Microsoft. Is there any way to do joint development. He
defined a transformation system to move from Smalltalk V to smalltalk
Parcplace.

To be able to define the combination of models using meta-models, you
need a correspondence model.

    mode: m
       grammar G defines language L
       interpretation: f
    m elem L
    f(m) is intepretation of m

    then you create the meta-grammar and meta-interpretation

    A -> MA
    B -> MB

you need a MAB that links the two together. Can you factor out the
meta-models.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
