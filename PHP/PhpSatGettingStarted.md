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
    Page](http://www.program-transformation.org/edit/PHP/PhpSatGettingStarted?t=1536826875)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/PhpSatGettingStarted)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/PhpSatGettingStarted)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/PhpSatGettingStarted?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/PhpSatGettingStarted?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    3](http://www.program-transformation.org/view/PHP/PhpSatGettingStarted?rev=1.3)
    [(diff 2)](http://www.program-transformation.org/rdiff/PHP/PhpSatGettingStarted?rev1=1.3&rev2=1.2)
-   [Rev
    2](http://www.program-transformation.org/view/PHP/PhpSatGettingStarted?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/PHP/PhpSatGettingStarted?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/PHP/PhpSatGettingStarted?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/PhpSatGettingStarted)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/PhpSatGettingStarted?template=oopsmore&param1=1.3&param2=1.3)
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
    \...](http://www.program-transformation.org/oops/PHP/PhpSatGettingStarted?template=oopsmore&param1=1.3&param2=1.3)
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
Php Sat Getting Started {#php-sat-getting-started .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Static analysis for PHP
:::

::: {.twikiToc}
-   [Analyzing a file](PhpSatGettingStarted#Analyzing_a_file)
-   [Analyzing multiple
    files](PhpSatGettingStarted#Analyzing_multiple_files)
    -   [Simple inclusion](PhpSatGettingStarted#Simple_inclusion)
    -   [Complex inclusion](PhpSatGettingStarted#Complex_inclusion)
    -   [Printing included
        files](PhpSatGettingStarted#Printing_included_files)
-   [Interpreting the
    output](PhpSatGettingStarted#Interpreting_the_output)
:::

[]{#Analyzing_a_file} Analyzing a file
--------------------------------------

After you have [installed](PhpSatDocumentation#Installation) php-sat you
can run it by typing:

      php-sat -h

If this command does not produce a list of all the options that are
available for php-sat you should check your installation.

We will start with a simple file, *foo.php* that contains an example of
the bug-pattern
[C002](https://svn.strategoxt.org/repos/psat/php-sat/trunk/doc/correctness/C002_to-many-parameters.txt):

    $ cat foo.php
    <?php
      function foo($bar){
         echo $bar;
      }

      foo("param1", "param2");
    ?>

We can feed this to php-sat by using the `-i` option (we also use the
`--extended-output` option to show the complete file again):

    $ php-sat -i foo.php --extended-output
    <?php
      function foo($bar){
        echo $bar;
      }
      /**
       * PHP-SAT check (Correctness)
       * Pattern ID : C002
       * Description: Too many parameters in function call
       */
      foo("param1", "param2");
    ?>

The output can also be saved into a file by giving the filename to the
`-o` option:

    $ ls
    foo.php
    $ php-sat -i foo.php -o foo.php.php-sat --extended-output
    $ ls
    foo.php  foo.php.php-sat
    $ cat foo.php.php-sat 
    <?php
      function foo($bar){
        echo $bar;
      }
      /**
       * PHP-SAT check (Correctness)
       * Pattern ID : C002
       * Description: Too many parameters in function call
       */
      foo("param1", "param2");
    ?>

[]{#Analyzing_multiple_files} Analyzing multiple files
------------------------------------------------------

But what if we have this *foo-simple.php*:

    $ cat foo-simple.php
    <?php
      include 'foo.inc';
     
      foo("param1", "param2");
    ?>

this *foo-complex*.php:

    $ cat foo-complex.php
    <?php
      $postfix = 'inc';
      include 'foo.'.$postfix;
     
      foo("param1", "param2");
    ?>

and this *foo.inc*:

    $ cat foo.inc 
    <?php
      function foo($bar){
         echo $bar;
      }
    ?>

The output of php-sat on *foo-simple.php* would then be:

    $ php-sat -i foo-simple.php --extended-output
    <?php
      include 'foo.inc';
      foo("param1", "param2");
    ?>

and on *foo-complex.php*:

    $ php-sat -i foo-complex.php --extended-output
    <?php
      $postfix = 'inc';
      include 'foo.' . $postfix;
      foo("param1", "param2");
    ?>

which is still correct, php-sat only reports things it finds, so
reporting nothing is still correct, but we would want php-sat to include
the files that are included. There are two modes in which php-sat can
include files, *simple* and *complex*.

### []{#Simple_inclusion} Simple inclusion

Simple inclusion means that php-sat will try to include *every* file
that is included by a *literal* name. Every
include/require/include\_once/require\_once statement that is followed
by a literal string will be included if the file can be found. This mode
does not respect the \*\_once-semantics, nor will it take into account
concatenated names.

So the \_php-simple.php\_-problem can be solved by passing the
`--simple-inclusion` flag to php-sat.

    $ php-sat -i foo-simple.php --simple-inclusion --extended-output
    <?php
      include 'foo.inc';
      /**
       * PHP-SAT check (Correctness)
       * Pattern ID : C002
       * Description: Too many parameters in function call
       */
      foo("param1", "param2");
    ?>

This the same output as before, we could even use the `-o` option is we
wanted.

The output for *foo-complex.php* is still not informative:

    $ php-sat -i foo-complex.php --simple-inclusion --extended-output
    <?php
      $postfix = 'inc';
      include 'foo.' . $postfix;
      foo("param1", "param2");
    ?>

### []{#Complex_inclusion} Complex inclusion

Complex inclusions is not complex for the user, just for php-sat itself.
This mode will trigger
[constant-propogation](http://en.wikipedia.org/wiki/Constant_propagation)
which will, as the name implies, propagate constant information through
the scripts. This causes the complex mode to use more resources, but
enables a larger set of analysis\'s.

This mode does respect the semantics of the \*\_once-statements, so
files will only be included the first time they are encountered.

The complex mode can be seen as an extension to the simple mode, every
file that is included in the simple mode will also be included by the
complex mode.

So the output for *foo-simple.php* with the `--complex-inclusion` flag
will be:

    $ php-sat -i foo-simple.php --complex-inclusion --extended-output
    <?php
      include 'foo.inc';
      /**
       * PHP-SAT check (Correctness)
       * Pattern ID : C002
       * Description: Too many parameters in function call
       */
      foo("param1", "param2");
    ?>

and for *foo-complex.php*:

    $ php-sat -i foo-complex.php --complex-inclusion --extended-output
    <?php
      $postfix = 'inc';
      include 'foo.' . $postfix;
      /**
       * PHP-SAT check (Correctness)
       * Pattern ID : C002
       * Description: Too many parameters in function call
       */
      foo("param1", "param2");
    ?>

### []{#Printing_included_files} Printing included files

In real world situation the included files could also contain
bug-patterns. These patterns can either be static, always available in
the source file, or dynamic, available under certain
inclusion-conditions. It is useful to examine the included files after
they are included to check for these patterns.\
The default behavior for included files is that they are discarded from
the memory after the analysis. This behavior can be altered by passing
the `--print-included-files` flag. This flag will print *all* included
files to the same location as the original files, giving them a
=php-sat=-postfix.

Here is a little example with simple inclusion. We have the same files
as before:

    $ ls
    foo-simple.php foo-complex.php foo.php foo.inc

When we use php-sat with a target we get one extra file with a result:

    $ php-sat -i foo-simple.php -o foo-simple.php.php-sat --simple-inclusion --extended-output
    $ ls
    foo-simple.php foo-complex.php foo.php foo.inc foo-simple.php.php-sat

Passing `--print-included-files` will give yet another extra file with a
result:

    $ php-sat -i foo-simple.php -o foo-simple.php.php-sat --simple-inclusion --print-included-files --extended-output
    $ ls
    foo-simple.php foo-complex.php foo.php foo.inc foo-simple.php.php-sat foo.inc.php-sat

[]{#Interpreting_the_output} Interpreting the output
----------------------------------------------------

Please take a look at the [bug-patterns
section](PhpSatBugPatterns){.twikiLink} to find out how the results
should be interpreted.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
