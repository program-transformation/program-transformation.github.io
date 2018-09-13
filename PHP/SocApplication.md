::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
[![PHP-SatLogo](../pub/PHP/PhpSatLogo/PHP-SAT-LOGO-100px.jpg)](WebHome){.twikiLink}

**[PHP-sat](PhpSat){.twikiLink}**

-   [Download](PhpSatReleases){.twikiLink}
-   [Documentation](PhpSatDocumentation){.twikiLink}
-   [Bugpatterns](PhpSatBugPatterns){.twikiLink}
-   [Quality](PhpSatQuality){.twikiLink}
-   [Origin](PhpSatOrigin){.twikiLink}
-   [Name](PhpSatName){.twikiLink}

**[PHP-front](PhpFront){.twikiLink}**

-   [Download](PhpFrontReleases){.twikiLink}
-   [Documentation](PhpFrontDocumentation){.twikiLink}
-   [Quality](PhpFrontQuality){.twikiLink}
-   [Origin](PhpFrontOrigin){.twikiLink}

**[PHP-tools](PhpTools){.twikiLink}**

**[Support](PhpSupport){.twikiLink}**

-   [Mailing lists](MailingList){.twikiLink}
-   [IRC](irc://irc.freenode.net/#stratego)
-   [Issues](http://bugs.strategoxt.org/browse/PSAT)

**[Developers](PhpSatDevelopers){.twikiLink}**

-   [Subversion](https://svn.strategoxt.org/repos/psat/)
-   [Continuous Builds](ContinuousBuilds){.twikiLink}
-   [Blog](http://ericbouwers.blogspot.com/)

**[The logo](PhpSatLogo){.twikiLink}**

**[Thanks](ThankYou){.twikiLink}**
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/PHP/SocApplication?t=1536826877)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/SocApplication)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/SocApplication)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/SocApplication?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/SocApplication?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/PHP/SocApplication?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/SocApplication)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/SocApplication?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/PHP/SocApplication?template=oopsmore&param1=1.1&param2=1.1)
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
Soc Application {#soc-application .twikiTopicTitle}
===============

::: {.twikiWebTitle}
Static analysis for PHP
:::

The following text was submitted as my proposal for Google\'s Summer of
Code 2006:

    Project Title
      Using static analysis to find vulnerabilities

    Synopsis
      Applications which are written in PHP usually deal with users and
      other external sources of data. This external data should always 
      be processed in such a way that it cannot do any harm to the 
      application itself or the system it is running on. Since programmers
      are usually just like normal people they sometimes forget to 
      process input properly. A beginning programmer doesn't even
      know that input can be dangerous. 
      With the use of a statical analysis of the source code 
      of an application, 'dangerous' data can be tracked
      down and the unsafe use can be reported to the programmer.
      Tools for this analysis can be built with the help of
      Stratego/XT [1].

    Benefits to the PHP Community
      The main benefit will be that programmers are able to find
      vulnerabilities in an automated way. Testing applications will
      be easier and this can decrease the amount of bugs in applications.
      The community will also get a basis for building more
      programs that can be used to improve their code. The PHC [2] has
      some ideas for this [3].

    Deliverables
      1: A parser for the latest PHP 4 version validated against the
         test suite of the distribution.
      2: A parser for the latest PHP 5 version validated against the
         test suite of the distribution.
      3: A tool that can analyse a PHP script to find possible
         vulnerabilities. The percentage of false positives should
         not be above 40%.
      4: A description about the method used and problems encountered.

    Project Details
      This project will be built with the help of Stratego/XT. There is
      already an (incomplete) syntax definition in SDF of PHP that
      is made by Eelco Dolstra [6]. This is done in the context of
      the StringBorg [5] framework and based on the Bison/Flex
      definition of PHP itself. This SDF is not yet complete
      but provides a very good structure to make the tool to
      parse scripts to an Abstract Syntax Tree.

      The project will start with the development of a SDF that can parse
      all the test files in the current releases. This only includes the
      real code of the test-files, not the specific declaration
      of the environment. This code should be parsed and pretty-printed.
      After this transformation the output should be the
      same as the input.

      The second part of the project will consist of making a
      tool that statically analyzes the source code of an application
      for vulnerabilities. This tool will be able to see if the programmer
      uses variables that are not safe. For example the printing of a
      GET-variable that is not escaped. To detect this the tool will use
      the concepts of data-flow analysis.

    Project Schedule
      May    23, 2006: Start of the project. Starting to work on the
                       SDF grammars.

      June   26, 2006: The SDF should be finished and the test-files
                       should be parsed correctly.

      June   27, 2006: Starting to work on the static analysis.

      July 8-15, 2006: No progress. Student is away with the scouts
                       on camp.

      August  1, 2006: The tool should be able to give useful feedback
                       when parsing an open source PHP project.

      August 21, 2006: End of the project. All tools are finished.

    Project references
      During the development of this proposal I stumbled upon Pixy[4].
      A Java tool that is based on the idea of data flow analysis.
      This project will do something similar. It will extend the
      analysis with the support of the object-oriented features of
      PHP. Apart from that it will provide a solid basis to create
      other tools.

      Another source of inspiration is PHC [2]. The problem with this
      is that one should use c++ to work with it. I think that it
      is easier to develop programs that transform/analyse source
      code in Stratego/XT instead of c++ because Stratego/XT is
      specifically made for this purpose.

    Bio
      I am currently following the Master Program Software Technology
      at the Utrecht University. Before that I have completed
      the Bachelor program at the same university. I also followed
      the teacher training for primary education at the Marnix
      Academie [8].
      Apart from my study I work 1.5 days as a teacher
      in the first grade of a primary school. I'm also active in
      the scouts movement of The Netherlands [9].
      An activity is the work with 'Team Internet'. We develop and
      maintain the system that is used to record and manage all
      information related to all members of the scouts organization
      in the Netherlands. This system is completely written in PHP.
      This project can help us in the search for vulnerabilities
      and provides a basis to make more tools that support our
      development.
      Apart from this practical aspect there is another motivation
      for this project. By giving the right feedback to people that use
      this tool, they can learn from their mistakes. My teacher-part
      really likes that idea.

    If there are any questions please contact me by e-mail.

    [1] http://www.stratego-language.org/Stratego/WebHome
    [2] http://www.phpcompiler.org/index.html
    [3] http://www.phpcompiler.org/spinoffs/index.html
    [4] Pixy: A Static Analysis Tool for Detecting Web Application Vulnerabilities
        http://www.seclab.tuwien.ac.at/projects/pixy/
    [5] http://www.stratego-language.org/Stratego/StringBorg
    [6] https://svn.cs.uu.nl:12443/repos/StrategoXT/stringborg/trunk/grammars/php/syntax/
    [7] http://www.cs.uu.nl/
    [8] http://www.hsmarnix.nl/english/english.htm
    [9] http://www.scouting.nl/frontend/sol/index.php?task=rs_static&action=news

\-- [EricBouwers](../Main/EricBouwers){.twikiLink} - 08 Sep 2006\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
