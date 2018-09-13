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
    Page](http://www.program-transformation.org/edit/GPCE11/Tutorial5OntologiesAndSE?t=1536828822)
-   [Rename
    Page](http://www.program-transformation.org/rename/GPCE11/Tutorial5OntologiesAndSE)
-   [Attach
    File](http://www.program-transformation.org/attach/GPCE11/Tutorial5OntologiesAndSE)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/GPCE11/Tutorial5OntologiesAndSE?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/GPCE11/Tutorial5OntologiesAndSE?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/GPCE11/Tutorial5OntologiesAndSE?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/GPCE11/Tutorial5OntologiesAndSE?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/GPCE11/Tutorial5OntologiesAndSE?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/GPCE11/Tutorial5OntologiesAndSE)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/GPCE11/Tutorial5OntologiesAndSE?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/GPCE11/Tutorial5OntologiesAndSE?template=oopsmore&param1=1.2&param2=1.2)
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
Tutorial 5 {#tutorial-5 .twikiTopicTitle}
==========

::: {.twikiWebTitle}
Generative Programming and Component Engineering
:::

### []{#Ontologies_and_Software_Language} Ontologies and Software Language Engineering

##### []{#http_www_sfu_ca_dgasevic_Dragan}[]{#_http_www_sfu_ca_dgasevic_Dragan} [Dragan Gašević](http://www.sfu.ca/~dgasevic/), [Fernando Silva Parreiras](http://www.fernando.parreiras.nom.br/), [Tobias Walter](http://www.uni-koblenz-landau.de/koblenz/fb4/institute/IFI/AGStaab/Persons/tobias-walter/tobias-walter)

###### []{#Abstract} Abstract

Trying to advance the current practices for sharing data, resources and
knowledge on the Web, the research community has been researching
challenges around the idea of the Semantic Web. The central component of
the Semantic Web are ontologies, commonly deﬁned as formal and explicit
definitions of shared domain conceptualizations. To have an
interoperable and standardized set of technologies, the Semantic Web
research oﬀered a stack of standards and tools including automated
reasoners and ontology languages, i.e., languages to describe formally a
domain of discourse. This stack of standards and tools is popularly
called semantic technologies. Among ontology languages, the Web Ontology
Language (OWL) \[4\] is the most prominent.

Mainly, due to the similarities in the design of OWL and object-oriented
languages, the research community started exploring a potential synergy.
Indeed, OWL provides important features complementary to UML class-based
modeling and OCL that improve software languages: it allows diﬀerent
ways of describing classes; it handles these descriptions as ﬁrst-class
entities; it provides additional constructs like transitive closure for
properties; and it enables dynamic classiﬁcation of objects based upon
class descriptions.

The most notable work has been done on integrating ontologies and
model-driven engineering, especially, for the tasks related to
model-driven language engineering. As the OWL language is based on
description logic, standard ontology reasoners can be used for various
types of processing of software languages such as consistency checking,
constraint validation, and query processing and with applications in
different software engineering areas such as component-based software
development, software product lines, or requirements engineering. For
example, the knowledge encoded in OWL evolves independently of the
execution logic, i.e., developers maintain class descriptions in the
ontology and not in the software. Moreover, developers may use class
descriptions to semantically query the domain. Semantic query plays an
important role where shared terminologies, interoperability and
consistency detection are required.

Striving to introduce the basics and potentials for ontologies for
software language engineering, this tutorial aims to:

1.  deﬁne ontologies and the OWL language;
2.  describe basics of description logics-based reasoning designed for
    ontology languages;
3.  describe the current eﬀorts on relations between the OWL language
    and languages such as UML, MOF and OCL; and
4.  illustrate applications of ontology-enhanced software

languages for software design patterns, software product lines,
domain-speciﬁc languages, and software language reﬁnement.

After the tutorial, participants will be able (1) to understand the
concepts of ontologies, OWL language and its formal reasoning
potentials; (2) to realize the valued added by ontology-enabled software
languages and (3) to identify potential applications for semantic
technologies in software development and diﬀerent software language
engineering approaches other than those based on model-driven
engineering principles.

###### []{#References} References

\[1\] Gaševic, Dragan, Djuric, Dragan, Devedžic, Vladan. Model Driven
Engineering and Ontology Development. Springer, Berlin, 2. edition,
2009.

\[2\] F. Silva Parreiras and S. Staab. Using Ontologies with UML
Class-based Modeling: The TwoUse Approach. Data Knowl. Eng. in press.

\[3\] F. Silva Parreiras, S. Staab, and A. Winter. Improving design
patterns by description logics: A use case with abstract factory and
strategy. In Modellierung 2008, volume P-127 of LNI, pages 89--104. GI,
2008.

\[4\] W3C OWL Working Group. OWL 2 Web Ontology Language Document
Overview. W3C Working Draft 27 March 2009. Available at
<http://www.w3.org/TR/2009/WD-owl2-overview-20090327//>.

\[5\] T. Walter, F. Silva Parreiras, and S. Staab. OntoDSL: An
Ontology-Based Framework for Domain-Speciﬁc Languages. In Model Driven
Engineering Languages and Systems, 12th International Conference, MODELS
2009, volume 5795, pages 408--422. Springer, 2009.

###### []{#Author_bios} Author bios

[Fernando Silva Parreiras](http://www.fernando.parreiras.nom.br/),
pursues his PhD since the beginning of 2006 under the supervision of
Prof. Steﬀen Staab. He is the leader of the Special Interest Group
Software Web at the Web Science and Technology Institute (WeST) at the
University of Koblenz-Landau, Germany. He has been investigating the
integration of model-driven engineering and Ontology in the scope of the
EU project MOST. His related publications include papers in
Modellierung'2008, ER'2008, ICSC'2009, MoDELS'2009 and ECMFA 2010. He
has served as program committee member of conferences like SLE and and
workshops like ONTOSE and SWESE and as organizer of the TWOMDE workshop.

[Dragan Gašević](http://www.sfu.ca/~dgasevic/) is a Canada Research
Chair in Semantic Technologies and an Associate Professor in the School
of Computing and Information Systems at Athabasca University. He is also
an Adjunct Professor in the School of Interactive Arts and Technology at
Simon Fraser University and an associated research member of the GOOD
OLD AI Research Network at the University of Belgrade. He is a recipient
of Alberta Ingenuity's 2008 New Faculty Award. His research interests
include semantic technologies, software language engineering,
technology-enhanced learning, and service-oriented architectures. He has
(co-)authored more than 200 research papers and delivered more than 10
tutorials at major conferences such as WWW, MODELS, CAiSE, and ISWC. He
has been serving on editorial boards of three international journals and
has edited special issues in journals such as IET Software and IEEE TSE.
He has been the organizer, chair, and member of program committees of
many international conferences.

[Tobias
Walter](http://www.uni-koblenz-landau.de/koblenz/fb4/institute/IFI/AGStaab/Persons/tobias-walter/tobias-walter)
is PhD. student at the University of Koblenz-Landau under the
supervision of Prof. Dr. Jürgen Ebert and Prof. Dr. Steﬀen Staab.
Currently he is member of the Institute for Software Technology and the
Institute for Web Science and Technology. Here, his research focuses on
the combination of domain-speciﬁc modeling languages and diﬀerent
ontology technologies. Further he is interested in the design and use of
new software modelling languages and its implementation in tools. From
2008 he is contributing to the MOST project where he is investigating
the conceptual integration of Model-Driven Architecture (MDA) and
Ontologies. His related publications include papers at MoDELS'2009,
ECMFA'2010, WC-DSL'2009, ICSC'2009 and different workshops.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
