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
    Page](http://www.program-transformation.org/edit/PHP/TheExampleProject?t=1536826878)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/TheExampleProject)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/TheExampleProject)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/TheExampleProject?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/TheExampleProject?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    10](http://www.program-transformation.org/view/PHP/TheExampleProject?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/PHP/TheExampleProject?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/PHP/TheExampleProject?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/PHP/TheExampleProject?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/PHP/TheExampleProject?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/PHP/TheExampleProject?rev1=1.8&rev2=1.7)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/TheExampleProject)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/TheExampleProject?template=oopsmore&param1=1.10&param2=1.10)
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
    \...](http://www.program-transformation.org/oops/PHP/TheExampleProject?template=oopsmore&param1=1.10&param2=1.10)
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
The Example Project {#the-example-project .twikiTopicTitle}
===================

::: {.twikiWebTitle}
Static analysis for PHP
:::

These pages describe how you can set-up your PHP-Front-based project. We
will use a real-life example to explain all the steps that are involved
in making a PHP-Front-based-project.

This tutorial is specifically targeted at starting a project based upon
PHP-Front. It is desired to have some knowledge about Stratego/XT and
grammars, but we will try to make everything clear. It would still be
useful to browse through the [documentation of
Stratego/XT](http://hydra.nixos.org/jobset/psat/strategoxt-manual-unstable-latest/manual/chunk-chapter/index.html).

The project that we will follow is the *php-tools* -project. This
project will hold a number of useful tools that can help in the
development of PHP-projects. The following steps have already been made
and documented:

::: {.twikiToc}
-   [Initialization](TheExampleProject#Initialization)
    -   [Repository](TheExampleProject#Repository)
    -   [Package configuration](TheExampleProject#Package_configuration)
-   [The first tool](TheExampleProject#The_first_tool)
    -   [Basic tool
        configuration](TheExampleProject#Basic_tool_configuration)
    -   [Setting up testing](TheExampleProject#Setting_up_testing)
    -   [Defining tests](TheExampleProject#Defining_tests)
    -   [Tool implementation](TheExampleProject#Tool_implementation)
    -   [Close issue](TheExampleProject#Close_issue)
-   [Adding an option](TheExampleProject#Adding_an_option)
    -   [First stop: tests](TheExampleProject#First_stop_tests)
    -   [Adding the logic](TheExampleProject#Adding_the_logic)
    -   [New pretty-printing](TheExampleProject#New_pretty_printing)
:::

[]{#Initialization} Initialization
----------------------------------

### []{#Repository} Repository

In this project we will work with a SVN repository to be able to keep
track of our changes and to revert stupid mistakes. The easiest way to
get the right structure for the SVN-repository is to use
[TheEmptyModule](TheEmptyModule){.twikiLink} as a template. So we create
a for our project on our own SVN-repository and copy
[TheEmptyModule](TheEmptyModule){.twikiLink} to it:\
(\$SVNROOT = <https://svn.strategoxt.org/repos>)

    [eric]$ svn mkdir $SVNROOT/psat/php-tools -m "New directory for project"

    Committed revision 303.
    [eric]$ svn co $SVNROOT/psat/php-tools ./php-tools
    Checked out revision 303.
    [eric]$ svn co $SVNROOT/psat/empty-module ./tmp
     ....
    Checked out revision 303.
    [eric]$ cd tmp/
    [eric]$ svn cp ./trunk ../php-tools/
    A         ../php-tools/trunk
    [eric]$ cd ../php-tools/
    [eric]$ svn commit -m "Added basic structure"
    Adding         trunk

    Committed revision 304.

This already gives us a complete directory and build-structure to work
with.

### []{#Package_configuration} Package configuration

*The rest of this tutorial will assume that the trunk-directory in the
repository is the root. E.g. the file \'bootstrap\' is directly in the
root*

We will first rename the .spec to reflect our project:

    [eric]$ svn mv empty-module.spec.in php-tools.spec.in
    A         php-tools.spec.in
    D         empty-module.spec.in
    [eric]$ svn mv empty-module.pc.in php-tools.pc.in
    A         php-tools.pc.in
    D         empty-module.pc.in

There are some variables that need to be changed within these files. I
have included the svn diffs for both files below. The latests versions
of the files can also be found in the
[repository](https://svn.strategoxt.org/repos/psat/php-tools)

    [eric]$ vim php-tools.spec.in 
    [eric]$ vim php-tools.pc.in 
    [eric]$ svn diff php-tools.spec.in
    Index: php-tools.spec.in
    ===================================================================
    --- php-tools.spec.in   (revision 304)
    +++ php-tools.spec.in   (working copy)
    @@ -1,10 +1,10 @@
    -Summary: Empty module: very empty module 
    +Summary: PHP-Tools is a collection of tools to analyze PHP-sources 
     Name: @PACKAGE_TARNAME@
     Version: @PACKAGE_VERSION@
     Release: 1
     License: LGPL
     Group: Development/Languages/PHP
    -URL: empty_module.com
    +URL: www.php-sat.org
     Source: @PACKAGE_TARNAME@-@PACKAGE_VERSION@.tar.gz
     BuildRoot: %{_tmppath}/%{name}-@PACKAGE_VERSION@-buildroot
     Requires: aterm >= 2.4
    [eric]$ svn diff php-tools.pc.in
    Index: php-tools.pc.in
    ===================================================================
    --- php-tools.pc.in     (revision 304)
    +++ php-tools.pc.in     (working copy)
    @@ -5,7 +5,7 @@
     strcflags=-I ${sdfdatadir} -I ${pkgdatadir}
     strcxtcflags=--xtc-repo ${xtc_repo}
     
    -Name: empty-module
    -Description: The empty module
    +Name: PHP-Tools 
    +Description: A package of tools to analyse PHP code 
     Version: @PACKAGE_VERSION@

The next file that needs to be adapted to our project, and ourselves, is
configure.ac

    [eric]$ vim configure.ac 
    [eric]$ svn diff configure.ac
    Index: configure.ac
    ===================================================================
    --- configure.ac        (revision 304)
    +++ configure.ac        (working copy)
    @@ -1,5 +1,5 @@
     AC_PREREQ([2.58])
    -AC_INIT([empty-module],[0.1],[empty-module-dev@somewhere])
    +AC_INIT([PHP-Tools],[0.1],[psat-dev@cs.uu.nl])
     AC_CONFIG_AUX_DIR([config])
     AM_INIT_AUTOMAKE([1.7.2 -Wall -Wno-portability])
     
    @@ -24,8 +24,8 @@
     AC_PROG_LIBTOOL
     
     AC_CONFIG_FILES([
    -  empty-module.spec
    -  empty-module.pc
    +  php-tools.spec
    +  php-tools.pc
       Makefile
     
       src/Makefile

And the last file is the Makefile.am:

    [eric]$ vim Makefile.am 
    [eric]$ svn diff Makefile.am
    Index: Makefile.am
    ===================================================================
    --- Makefile.am (revision 304)
    +++ Makefile.am (working copy)
    @@ -3,8 +3,8 @@
     SUBDIRS = src tests
     BOOTCLEAN_SUBDIRS = $(SUBDIRS)
     
    -EXTRA_DIST        = $(pkgdata_DATA) Makefile.xt php-sat.spec php-sat.spec.in php-sat.pc bootstrap autoxt.m4
    +EXTRA_DIST        = $(pkgdata_DATA) Makefile.xt php-tools.spec php-tools.spec.in php-tools.pc bootstrap autoxt.m4
     
     ACLOCAL_AMFLAGS = -I .
     
    -pkgconfig_DATA = php-sat.pc
    +pkgconfig_DATA = php-tools.pc

If everything is correct the package will still build, but now with you
own information.

    [eric]$ ./bootstrap 
    [eric]$ ./configure prefix=/home/eric/bin/hp-tools --enable-bootstrap
    [eric]$ cat php-tools.spec
    Summary: PHP-Tools is a collection of tools to analyze PHP-sources 
    Name: php-tools
    Version: 0.1pre304
    Release: 1
     ....

You can change the contents of the files **NEWS**, **AUTHORS** and
**README** to whatever you want. Just make sure that you commit at the
end:

    [eric]$ svn commit -m "Added correct configuration in the files"
    Sending        Makefile.am
    Sending        configure.ac
    Deleting       empty-module.pc.in
    Deleting       empty-module.spec.in
    Adding         php-tools.pc.in
    Adding         php-tools.spec.in
    Transmitting file data ....
    Committed revision 306.

If you want to get a copy of the project after doing all this, get it
from:

<https://svn.strategoxt.org/repos/psat/php-tools/tags/version0.0/>

[]{#The_first_tool} The first tool
----------------------------------

The first tool that we will make has the functionality described in
<http://bugs.strategoxt.org/browse/PSAT-9>. The input of this tool will
be a php-file and it will generate a list of all the uses of one of the
global-arrays.

### []{#Basic_tool_configuration} Basic tool configuration

After the decision for the name, input-vector, the file for this tool is
made in the appropriate sub-directory (keep in mind that we are working
from the trunk):

    [eric]$ touch ./src/tools/input-vector.str

After the making of the file we will fill in the basic components of a
tool, notice that you can use the following code as a basis for all of
your tools:

    module input-vector 
    imports
      libphp-front
      libstratego-lib
      libstratego-tool-doc

    strategies
      main-input-vector =
        io-stream-wrap(
          input-vector-options
        , input-vector-usage
        , input-vector-about
        , process-php-stream( parse-php-stream
                            ; input-vector-main
                            )
        )

    strategies
      /**
       * Options that can be used
       */
      input-vector-options =
        parse-php-options // Normal PHP options 

    strategies
      /**
       * Main strategy of the program.
       */
      input-vector-main = 
        id  

    /**
     * Documentation
     */
    strategies
      input-vector-usage =
        <tool-doc>
          [ Usage("input-vector [OPTIONS]")
          , Summary("Lists all the usages of the input-arrays from a given PHP-File.")
          , OptionUsage()
          , AutoReportBugs()
          ]

      input-vector-about =
        <tool-doc>
          [ AutoProgram()
          , Author(Person("Eric Bouwers", "eric@bouwers.info"))
          , GNU_LGPL("2007", "Eric Bouwers <eric@bouwers.info>")
          , Config([
              DefaultXTCRepository()
            , CurrentXTCRepository()
            ])
          ]

This template above does the following things:

1.  Defines the module of this tool
2.  Imports the most important modules from the environment
3.  Defines the start strategy. This strategy wraps all the options and
    our functionality in a stream-function. Our functionality is called
    after the parsing the input file.
4.  Defines the options that can be used, we only use the
    parse-php-options form the php-front-library
5.  Defines a strategy that will hold our own functionality, for now
    just the \'id\'-strategy
6.  Defines two strategies that capture how to use it and the maker of
    the program (me)

In order to make this thing build we will have to adapt the Makefile.am
in the ./src/tools/-directory. The tool will have to be added, the
sources listed and the right modules should be linked. We mainly use the
pre-defined things from the `empty-module`. Here is a diff:

    Index: Makefile.am
    ===================================================================
    --- Makefile.am (revision 307)
    +++ Makefile.am (working copy)
    @@ -1,7 +1,7 @@
     include $(top_srcdir)/Makefile.xt
     include $(wildcard *.dep)
     
    -bin_PROGRAMS = empty-module 
    +bin_PROGRAMS = input-vector 
     
     EXTRA_DIST     = $(wildcard *.str) $(wildcard *.meta)
     CLEANFILES     = $(wildcard *.dep) $(wildcard *.c)
    @@ -14,7 +14,7 @@
       $(STRATEGO_XTC_STRCFLAGS) \
       $(STRATEGO_GPP_STRCFLAGS)
     
    -empty_module_SOURCES = empty-module.c 
    +input_vector_SOURCES = input-vector.c 
     
    -empty_module_LDADD = $(top_builddir)/src/lib/libempty-module.la $(PHP_FRONT_LINS) $(STRATEGO_GPP_LIBS) \
     $(SSL_LIBS) $(STRATEGO_TOOL_DOC_LIBS)
    -
    +#empty_module_LDADD = $(top_builddir)/src/lib/libempty-module.la $(PHP_FRONT_LIBS) $(STRATEGO_GPP_LIBS) \
     $(SSL_LIBS) $(STRATEGO_TOOL_DOC_LIBS)
    +input_vector_LDADD = $(PHP_FRONT_LIBS) $(STRATEGO_GPP_LIBS) $(SSL_LIBS) $(STRATEGO_TOOL_DOC_LIBS)

If you issue the command `make` in the src/tools/-directory the tool
should compile without warnings, but if you try to run `make` in the
root-directory you will still get some errors. So let\'s fix these
issues!

First adapt the file `Makefile.am` in the root by removing the directory
`test` from the `SUBDIRS` variable:

    -SUBDIRS = src tests
    +SUBDIRS = src 

We then do the same with the directories `grammar` and `lib` in the file
`./src/Makefile.am`:

    -SUBDIRS = grammar lib tools
    +SUBDIRS = tools

The project is now able to completely build and install the tool without
any problems.

### []{#Setting_up_testing} Setting up testing

A clear definition of the task that your tool will be doing is always a
handy reference. So we will define some tests for our tool. These tests
are put where they belong, in a `tools` -directory under `tests`.

    [eric]$ mkdir tests/tools/
    [eric]$ touch tests/tools/input-vector-tests.str
    [eric]$ svn add tests/tools/
    A         tests/tools
    A         tests/tools/input-vector-tests.str
    [eric]$ svn cp ./tests/Makefile.am-libtool ./tests/tools/Makefile.am
    A         tests/tools/Makefile.am

Then we specify the following module with a basic template for
test-modules:

    module input-vector-tests
    imports 
      input-vector

    strategies

      main-input-vector-tests =
        option-wrap(general-options,
           test-suite(!"Input vector tests",
                        input-vector-tests
                     )
                   )
    strategies
      /**
       * Wrapper strategy for easier definition of 
       * tests
       */
      iv-test(|msg, src, result)=
        apply-test( !msg
                  , input-vector-main
                  , <parse-php-string> src
                  , !result
                  )   

    strategies
      /**
       * Strategy that holds the tests
       */
      input-vector-tests = id    
      ; iv-test(|
       "Simple get"
      ,"<?php
          $foo = $_GET['foo'];
       ?>"
      , "$_GET['foo']"
      )

This file:

1.  Specifies his own module-name
2.  Imports the tool that is going to be checked
3.  Defines the main strategy with a test-suite, wrapped in normal
    options
4.  Defines a short-cut strategy for testing this tool. This strategy
    takes care of calling the actual test-strategy, parses the input and
    calls the right strategy to test.
5.  Defines a strategy with one test, this test is used to check whether
    or not the test-suite works.

In order to get this to compile in a nice way we need to alter some
configuration files again. Here is the list:

`./tests/tools/Makefile.am`

    Index: tests/tools/Makefile.am
    ===================================================================
    --- tests/tools/Makefile.am     (revision 0)
    +++ tests/tools/Makefile.am     (working copy)
    @@ -3,20 +3,21 @@
     
     TESTS = $(check_PROGRAMS)
     check_PROGRAMS=\
    -  empty-module-tests 
    +  input-vector-tests 
     
     
     
     STRINCLUDES = \
       -I $(srcdir) -I $(top_srcdir)/src/lib -I $(top_builddir)/src/lib \
    +  -I $(top_srcdir)/src/tools -I $(top_builddir)/src/tools \
       $(PHP_FRONT_STRCFLAGS) \
       $(STRATEGO_XTC_STRCFLAGS) \
       $(STRATEGO_SGLR_STRCFLAGS)
     
    -LDADD += $(top_builddir)/src/lib/libempty-module.la $(PHP_FRONT_LIBS) \
     $(STRATEGO_GPP_LIBS) $(SSL_LIBS)
    +LDADD += $(PHP_FRONT_LIBS) $(STRATEGO_GPP_LIBS) $(SSL_LIBS)
     STRCFLAGS  = --main main-$* --format-check 0 -O 0
     
     EXTRA_DIST = $(wildcard *.str)
     CLEANFILES = $(wildcard *.c) $(wildcard *.dep)
     
    -nodist_empty_module_tests_SOURCES = empty-module-tests.c
    +nodist_input_vector_tests_SOURCES = input-vector-tests.c

We have added the path to the tool in the STRINCLUDES variable,
specified the test-suite as a program to check and told `make` that the
`.c` file is actually generated.

Next up `./configure.ac`

    Index: configure.ac
    ===================================================================
    --- configure.ac        (revision 307)
    +++ configure.ac        (working copy)
    @@ -32,6 +32,8 @@
       src/grammar/Makefile
       src/lib/Makefile
       src/tools/Makefile
    -
    +  
    +  tests/Makefile
    +  tests/tools/Makefile
     ])

We have added the two `Makefile` files for the checking mechanism.
Notice that we will have to add a `Makefile.am` in the directory
`/tests/` in order to go into the subdirectories. This is exactly the
same as the `Makefile.am` -file in the `./src=-directory`, so we will
just copy this one:

    [eric]$ svn cp ./src/Makefile.am ./tests/

Within the previous section we removed the test-directory. In order to
be able to run the tests from the root we have to re-enable them again.
So, we adapt the file `Makefile.am` in the root again, adding the
directory `test` to the `SUBDIRS` variable:

    -SUBDIRS = src 
    +SUBDIRS = src tests

And now everything is in place to run the automated build project and
the checks! Just type `make check` to build everything and test the
test-suite. Notice that the test-suite will fail now, but that is a good
sign at the moment.

### []{#Defining_tests} Defining tests

The definition of the tests greatly depends on the design of the tool.
What are the exact steps, and thus strategies, that need to be
implemented? In this case the tool has to do two separate steps:

-   Retrieve a list of array-access nodes in abstract syntax
-   Pretty print this list into a single list.

So we first define the main strategy in terms of these two steps:

    strategies
      /**
       * Main strategy of the program.
       */
      input-vector-main = 
         get-input-arrays
       ; pretty-print-list 

Now we can define the tests that are going to check and describe what
these strategies do. The following sample shows just a single test per
function, but the actual test-suite contains 17 tests. These cover the
names of all the arrays and the boundary cases when dealing with lists.
This file can be found in the
[repository](https://svn.strategoxt.org/repos/psat/php-tools/trunk/tests/).

    strategies
      /**
       * Wrapper strategies for easier definition of 
       * tests
       */
      gia-test(|msg, src, result)=
        apply-test( !msg
                  , get-input-arrays
                  , <parse-php-string> src
                  , !result
                  )   
      
      ppal-test(|msg, src, result)=
        apply-test( !msg
                  , pretty-print-list
                  , !src
                  , !result
                  )   
    strategies
      /**
       * Strategy that holds the tests for
       * get-input-arrays
       *
       * Arrays: _GET, _POST, _REQUEST, _SERVER, HTTP_SERVER_VARS, _COOKIE, _FILES
       *        HTTP_COOKIE_VARS, HTTP_GET_VARS, HTTP_POST_VARS, HTTP_POST_FILES, 
       */
      get-input-arrays-tests = 
       gia-test(|
       "Simple get test"
      ,"<?php
        $foo = $_GET['foo']
        ?>"
      ,[ArrayAccess(Variable(Simple("_GET")),Some(ConstantEncapsedString(SingleQuoted([Literal("foo")]))))]
      )   

      /**
       * Strategy that holds the tests for
       * pretty-print-list
       */
      pretty-print-array-list-tests =
        ppal-test(|
          "Simple pretty printer"
        , [ArrayAccesss(Variable(Simple("_GET")),Some(ConstantEncapsedString(SingleQuoted([Literal("foo")]))))]
        , ["$_GET['foo']"]
        )

### []{#Tool_implementation} Tool implementation

After the definition of the tests we can start to implement the
strategies. We start with the strategy for collecting an array-access.
In order to make it somewhat generic we want this strategy to receive a
list of names and match an list ArrayAccess when the name is of the
variable is an element of this list:

      /**
       * Matches on an ArrayAccess when the name of the ArrayAccess is in the
       * given list. 
       * 
       * @param names List of names 
       * @type ArrayAccess(Variable(Simple(_) ->? ArrayAccess(Name(_),_)
       */ 
      match-array-access(|names) =
        ?ArrayAccess(Variable(Simple(name),_)
      ; where(<elem> (name,names) )

And we also want a list of names:

      /**
       * Builds a list of array names to retrieve the access from
       * @type List(String(_))
       */
      array-names =
        ![ "_GET"     , "HTTP_GET_VARS"
         , "_POST"    , "HTTP_POST_VARS"
         , "_COOKIE"  , "HTTP_COOKIE_VARS"
         , "_FILES"   , "HTTP_POST_FILES"
         , "_REQUEST" , "_SERVER" 
         ]

With the definition of these building block the implementation of the
`get-input-arrays` can be made rather easy because we can just use a
strategy from PHP-Front. The strategy is called `php-collect-inclusion`
and collects all the nodes that make the given strategy succeed in a
set:

      /** 
       * Retrieves the input vectors from a PHP-Source tree
       *
       * @type Document(..) -> List(ArrayAccess(...))  
       */
      get-input-arrays = 
       php-collect-inclusion(
         match-array-access(|<array-names>)
       ) 

When we compile and execute the test-suite by issuing `make check`, we
see that the collect tests pass. On to the implementation of the
pretty-printer strategy.

The strategy that handles the pretty-printing of a list is pretty
straightforward. We just map the strategy `pp-php-to-string` over the
list:

      /**
       * Pretty prints a list of ArrayAccess to a single string
       *
       * @type List(ArrayAccess(..)) -> List(String)
       */
      pretty-print-list = 
        map(pp-php-to-string) 

All we have to do now is to call `lines` on this list. This strategy
will transform a list of strings to a long string where each string is
separated by a newline. The main strategy now becomes:

      /**
       * Main strategy of the program.
       */
      input-vector-main = 
         get-input-arrays
       ; pretty-print-list  
       ; lines

After compilation we find out that all our tests pass, the tool is
finished!

If you want to get a copy of the project after doing all this, get it
from:

<https://svn.strategoxt.org/repos/psat/php-tools/tags/version0.1/>

### []{#Close_issue} Close issue

It is always nice to close an issue when you are done with a task. It
gives a kind of finished feeling :) See
<http://bugs.strategoxt.org/browse/PSAT-9> for the (closed) issue.

[]{#Adding_an_option} Adding an option
--------------------------------------

In order to give the users of our tool more information we add the
possibility of receiving extended output. Instead of the normal list of
super-globals we add an option to output not only the entries from the
arrays, but also the occurrence of this super-global-access.

### []{#First_stop_tests} First stop: tests

To make sure that the added option actually works we add two tests to
the already existing test-suite of our tool (in
tests/tools/input-vector-tests.str):

     ; iv-ext-test(|
        "Simple get extended"
      , FILE("testfiles/extended-get-1.php")
      , "$_GET['foo'] on line 2
    "
      )
     ; iv-ext-test(|
        "Simple get extended"
      , FILE("testfiles/extended-get-2.php")
      , "$_GET['foo'] on line 2
    $_GET['foo'] on line 3
    $_GET['bar'] on line 3
    "
      )

Notice that we added extra information to the output, namely the
line-number of the first occurrence. Also, we had to put the code of the
tests into actual files because the strategy \'parse-string\' cannot
deal with the option to preserve-position-info. This is something that
is absolutely needed in order to get the line-number. Furthermore, we
have also added an extra test-function that first sets the option for
generating extended output:

      iv-ext-test(|msg, src, result)=
       apply-test( !msg
                 , input-vector-main
                 , where (set-extended-output) ; <parse-php> src
                 , !result
                 ) 

Unfortunately, our test-suite cannot be compiled because the strategy
\'set-extended-output\' is not defined. Let us add this to the tool (in
src/tools/input-vector.str):

     /**
      * Extra options for extended output
      */
      strategies
        extended-output-option =
            Option("--extended-output"
                  , set-extended-output 
                  , !HelpString("--extended-output", 
                      "Add the number of the line of the first occurrence to the output. [off]")
                  )

        set-extended-output =
           <set-config> ("extended-output", "yes")
         ; <set-preserve-positions> "yes"

        get-extended-output =
            <get-config> "extended-output" => "yes"

As you can see, an option is defined by three separate strategies. The
first one defines the actual option by creating an actual Option. The
second one is a \'setter\'-strategy, the same one that is used in the
tests, and the last one is a getter-strategy.

Now that the strategies are in place we can compile the tool and compile
and run the test-suite. The result is as to be expected, two failing
tests.

### []{#Adding_the_logic} Adding the logic

When we take a closer look at the failing tests we can see that they do
not fail because the output lacks the line numbers, the output is simply
the empty string! This behavior is caused by the added annotations for
position-info.

The function \'match-array-access\' matches a name and checks whether
this name is in the given array. When annotations are added to the name
that is checked it will not be in the array with names, so not a single
array-access is accepted. The solution is pretty simple, just remove the
annotations before checking whether the name is an element of the given
array:

      match-array-access(|names) =
        ?ArrayAccess(Variable(Simple(name)),_) 
      ; where( name' := <strip-annos> name
             ; <elem> (name',names))

### []{#New_pretty_printing} New pretty-printing

Now that the array-access is collected again we can move to the final
part of the exercise, pretty-printing the extended output. First we add
a conditional check to the printing-strategy:

      pretty-print-list =
        if get-extended-output 
        then map(extended-pp-php-to-string)
        else map(pp-php-to-string)
        end

Then we define a strategy \'extended-pp-to-string\' that pretty-prints
the node and formats a message with the line-number. The code pretty
much speaks for itself.

      extended-pp-php-to-string = 
         ?array
       ; where( msg := <concat-strings> [<pp-php-to-string> array, " on line [STARTLINE]"] )
       ; <format-location-string(|msg)> array

And that is all that is to it to add an option to an existing tool!\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
