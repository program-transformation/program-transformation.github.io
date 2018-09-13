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
    Page](http://www.program-transformation.org/edit/Stratego/BuildfarmConfiguration?t=1536825539)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/BuildfarmConfiguration)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/BuildfarmConfiguration)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/BuildfarmConfiguration?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/BuildfarmConfiguration?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    5](http://www.program-transformation.org/view/Stratego/BuildfarmConfiguration?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/BuildfarmConfiguration?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/BuildfarmConfiguration?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/BuildfarmConfiguration?rev1=1.4&rev2=1.3)
-   [Rev
    3](http://www.program-transformation.org/view/Stratego/BuildfarmConfiguration?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/Stratego/BuildfarmConfiguration?rev1=1.3&rev2=1.2)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/BuildfarmConfiguration)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/BuildfarmConfiguration?template=oopsmore&param1=1.5&param2=1.5)
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
    \...](http://www.program-transformation.org/oops/Stratego/BuildfarmConfiguration?template=oopsmore&param1=1.5&param2=1.5)
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
Buildfarm Configuration {#buildfarm-configuration .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

To add a job, you need to:

1.  describe your package in `packages.nix` (e.g. `fooFront`)
2.  add a release to `releases.nix` (e.g. `fooFrontUnstable`), referring
    to fooFront in `packages.nix`
3.  add a job to the buildfarm `jobs.nix` (e.g. `fooFrontTrunk`),
    referring to fooFront in `packages.nix`

[]{#Pointers} Pointers
----------------------

### []{#Package_Descriptions} Package Descriptions

-   <https://svn.nixos.org/repos/nix/release/trunk/jobs/strategoxt/packages.nix>

See the other package descriptions for examples. Important are:

-   packageName (e.g. `"foo-front"`)
-   attrPrefix (e.g. `"fooFront"`)
-   contactEmail
-   notifyAddresses (non-empty list of email addresses)
-   svn, with usually a trunk attribute
-   requires (e.g. `[aterm sdf2Bundle strategoxt]`)
    -   Dependencies on other packages that are being built in this
        buildfarm. The exact package to built against will be determined
        by the inputs of the build job, which are links to
        `release-info.xml`.
-   svnRequires (e.g. `requires`)
-   buildInputs (e.g. `[pkgs.pkgconfig]`)
    -   dependencies from nixpkgs, not being built in this buildfarm
-   svnBuildInputs
    -   stuff needed when building from svn, not being built in this
        buildfarm
-   `systemSupported` (e.g. `systemSupport pkgs commonSystemsSupported`)

Make sure that the file is syntactically correct before committing:
`packages.nix` is imported by the jobs configuration. If there is a
syntactic problem in `packages.nix`, then the entire buildfarm will go
down. You can use nix-instantiate to check the syntax of `packages.nix`,
or (better) you can evaluate the entire `jobs.nix` file (see Jobs).

### []{#Releases} Releases

-   <https://svn.nixos.org/repos/nix/release/trunk/jobs/strategoxt/releases.nix>

Just copy one of the examples.

### []{#Jobs} Jobs

-   <https://svn.nixos.org/repos/nix/configurations/trunk/tud/buildfarm/strategoxt/jobs.nix>

This file is somewhat documented. Adding a job without strange
dependencies should be fairly easy.

Make sure to check if the job you added is syntactically correct,
otherwise the entire buildfarm will go down. For that, instantiate the
main jobs.nix file (which is one level up from the strategoxt
directory).

    $ pwd
    /home/martin/wc/supervisor/strategoxt

    $ /nix/bin/nix-instantiate ../jobs.nix --eval-only --strict --xml 

You can also test your job. First you have check out a couple of
directories:

    $ svn co https://svn.nixos.org/repos/nix/release/trunk release
    $ svn co https://svn.nixos.org/repos/nix/configurations/trunk/tud/buildfarm

After this, you must update the file
`release/jobs/strategoxt/test/generate-test.sh` and make it point to the
`release` directory you checked out. After this, you\'re ready to start
building:

    $ cd release/jobs/strategoxt/test
    $ ./generate-test.sh fooFrontTrunk
    $ ./fetch-inputs.sh
    $ nix-build test.nix

where `fooFrontTrunk` should be substitued with your favourite package.

[]{#Configuration} Configuration
--------------------------------

-   Baseline packages:
    -   <https://svn.nixos.org/repos/nix/configurations/trunk/tud/buildfarm/strategoxt/baseline.nix>

<!-- -->

-   Available systems:
    -   <https://svn.nixos.org/repos/nix/configurations/trunk/tud/buildfarm/strategoxt/systems.nix>

[]{#Want_something_else}[]{#Want_something_else_} Want something else?
----------------------------------------------------------------------

If you don\'t want to use the system of packages.nix and dependencies on
releases produced by the buildfarm, then you can take a look at the Nix
jobs:

-   <https://svn.nixos.org/repos/nix/release/branches/new/jobs/nix/nix.nix>
-   <https://svn.nixos.org/repos/nix/configurations/trunk/tud/buildfarm/jobs.nix>

\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
