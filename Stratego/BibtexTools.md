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
    Page](http://www.program-transformation.org/edit/Stratego/BibtexTools?t=1536825468)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/BibtexTools)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/BibtexTools)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/BibtexTools?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/BibtexTools?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    17](http://www.program-transformation.org/view/Stratego/BibtexTools?rev=1.17)
    [(diff 16)](http://www.program-transformation.org/rdiff/Stratego/BibtexTools?rev1=1.17&rev2=1.16)
-   [Rev
    16](http://www.program-transformation.org/view/Stratego/BibtexTools?rev=1.16)
    [(diff 15)](http://www.program-transformation.org/rdiff/Stratego/BibtexTools?rev1=1.16&rev2=1.15)
-   [Rev
    15](http://www.program-transformation.org/view/Stratego/BibtexTools?rev=1.15)
    [(diff 14)](http://www.program-transformation.org/rdiff/Stratego/BibtexTools?rev1=1.15&rev2=1.14)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/BibtexTools)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/BibtexTools?template=oopsmore&param1=1.17&param2=1.17)
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
    \...](http://www.program-transformation.org/oops/Stratego/BibtexTools?template=oopsmore&param1=1.17&param2=1.17)
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
Stratego/XT [BibTeX](BibTeX){.twikiLink} Tools {#strategoxt-bibtex-tools .twikiTopicTitle}
==============================================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Description](BibtexTools#Description)
    -   [Formatting](BibtexTools#Formatting)
    -   [Other Examples](BibtexTools#Other_Examples)
-   [Usage](BibtexTools#Usage)
    -   [Bib-to-html](BibtexTools#Bib_to_html)
    -   [Aux-to-bib](BibtexTools#Aux_to_bib)
-   [Download](BibtexTools#Download)
-   [Related Tools](BibtexTools#Related_Tools)
-   [Credits](BibtexTools#Credits)
    -   [License and Disclaimer](BibtexTools#License_and_Disclaimer)
:::

[]{#Description} Description
----------------------------

The bibtex-tools package provides components for processing
[BibTeX](BibTeX){.twikiLink} files, mainly for producing publication
lists in PDF and HTML automatically from a bibtex file. The creation of
publication pages is driven by templates for selecting bibtex entries
from the file and for dividing the entries into sections. The package
comes with standard templates for publication lists by-year, by-type,
by-year-and-type, alphabetically, etc. The program creates individual
bibtex files for each publication and refers to that from the html such
that other people can easily cite your paper. The program creates links
for fields in the bib entry which have a name starting with \'url\'.

### []{#Formatting} Formatting

The program uses the proper bibtex tool for formatting of bibtex
entries, since this is superior to and more complete than any
handcrafted attempt at formatting bibliographies. It also allows use of
different formatting styles.

For example, from an entry such as:

    @InProceedings{DV02-csmr,
      author =       {Arie van Deursen and Eelco Visser},
      title =        {The Reengineering Wiki},
      booktitle =    {Proceedings 6th European Conference on Software Maintenance and Reengineering (CSMR)},
      year =         2002,
      pages =        "217--220",
      publisher =    {IEEE Computer Society},
      url =          {http://www.program-transformation.org/re/},
      urlinfo =      {http://www.program-transformation.org/Transform/ReengineeringWikiPaper},
      urlpdf =       {http://www.cs.uu.nl/people/visser/ftp/DV02-csmr.pdf},
      pubcat =       {conference}
    }

the following entry is created:

-   A. van Deursen and E. Visser. [The Reengineering
    Wiki](http://www.program-transformation.org/re/). In *Proceedings
    6th European Conference on Software Maintenance and Reengineering
    (CSMR)*, pages 217\--220. IEEE Computer Society, 2002.
    ([info](../Transform/ReengineeringWikiPaper),
    [pdf](http://www.cs.uu.nl/people/visser/ftp/DV02-csmr.pdf), bib).

Where the title is a link to the first url field, and the (info, pdf,
bib) are links to the info url, the pdf url, and the bibtex entry for
the publication, respectively.

### []{#Other_Examples} Other Examples

For examples of the output generated see my [publication
list](http://www.cs.uu.nl/groups/ST/Visser/PublicationsByYear).

[]{#Usage} Usage
----------------

See the
[manual](http://nix.cs.uu.nl/dist/stratego/bibtex-tools-unstable-latest/bibtex-tools.pdf)
for extensive tool documentation.

### []{#Bib_to_html} Bib-to-html

Invoke the program as follows:

    bib-to-html -i file.bib --all-templates

This will produce various presentations of the publications in
`file.bib`; by-year, by-type, by-year and type, etc. The presentations
are in HTML and PDF. The HTML version points to the PDF file and each
publication points to a page with its bib entry.

There are many other options and it is possible to specify your own
selection queries and presentation templates.

### []{#Aux_to_bib} Aux-to-bib

Reduce a bibtex file to the entries cited in an aux file. Useful for
specializing a large bibtex file for a publication.

[]{#Download} Download
----------------------

Latest stable release:

-   [BibTeX Tools 0.2](BibtexToolsRelease02){.twikiLink} (for
    [Stratego/XT 0.16](StrategoRelease016){.twikiLink})

The latest build of bibtex-tools is available from

-   <http://buildfarm.st.ewi.tudelft.nl/releases/strategoxt/full-index-bibtex-tools.html#bibtex-tools-Unstable>

and includes a
[manual](http://nix.cs.uu.nl/dist/stratego/bibtex-tools-unstable-latest/bibtex-tools.pdf)
with documentation of all the components in the package and an
explanation of the
[LaTeX[^?^](http://www.program-transformation.org/edit/Stratego/LaTeX?topicparent=Stratego.BibtexTools)]{.twikiNewLink
style="background : #FFFFCE;"} techniques used.

[]{#Related_Tools} Related Tools
--------------------------------

-   [bibtex2web](http://pag.lcs.mit.edu/~mernst/software/#bibtex2web)

[]{#Credits} Credits
--------------------

The bibtex-tools package is created by [Eelco
Visser](EelcoVisser){.twikiLink}. The package makes heavy use of exising
bibtex and latex software, i.e. latex, bibtex, and hevea for conversion
from latex to html.

Thanks to Peter Mosses and Merijn de Jonge for bug reports and feature
requests.

### []{#License_and_Disclaimer} License and Disclaimer


      Copyright (C) 2000-2005 Eelco Visser

      This library is free software; you can redistribute it and/or
      modify it under the terms of the GNU Lesser General Public
      License as published by the Free Software Foundation; either
      version 2 of the License, or (at your option) any later version.

      This library is distributed in the hope that it will be useful,
      but WITHOUT ANY WARRANTY; without even the implied warranty of
      MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
      Lesser General Public License for more details.

      You should have received a copy of the GNU Lesser General Public
      License along with this library; if not, write to the Free Software
      Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA 02111-1307  USA

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
