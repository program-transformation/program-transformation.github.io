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
    Page](http://www.program-transformation.org/edit/PHP/PhpSatConfiguration?t=1536826876)
-   [Rename
    Page](http://www.program-transformation.org/rename/PHP/PhpSatConfiguration)
-   [Attach
    File](http://www.program-transformation.org/attach/PHP/PhpSatConfiguration)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/PHP/PhpSatConfiguration?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/PHP/PhpSatConfiguration?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/PHP/PhpSatConfiguration?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/PHP/PhpSatConfiguration?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/PHP/PhpSatConfiguration?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/PHP/PhpSatConfiguration)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/PHP/PhpSatConfiguration?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/PHP/PhpSatConfiguration?template=oopsmore&param1=1.2&param2=1.2)
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
Php Sat Configuration {#php-sat-configuration .twikiTopicTitle}
=====================

::: {.twikiWebTitle}
Static analysis for PHP
:::

::: {.twikiToc}
-   [Why configuration?](PhpSatConfiguration#Why_configuration)
-   [Format](PhpSatConfiguration#Format)
-   [Default configuration](PhpSatConfiguration#Default_configuration)
:::

[]{#Why_configuration}[]{#Why_configuration_} Why configuration?
----------------------------------------------------------------

The configuration file is used to configure the security-analysis within
php-sat. It contains information about three things:

-   Which variables bring tainted data into the script
-   Which functions/constructs can make this data safe
-   Which [SafetyLevel](SafetyLevel){.twikiLink} the parameters of a
    function should have

This information can differ between projects and configurations of PHP.
The most obvious example would be the [magic
quotes](http://www.php.net/magic_quotes) directive. This directive
influences the security algorithm directly because the input-data will
have a higher [SafetyLevel](SafetyLevel){.twikiLink}.

[]{#Format} Format
------------------

The format of the configuration file is best explained with the
following example file:

    1: [tainted sources]
    2:   array:    _SERVER           level: escaped-slashes 
    3:   function: file_get_contents level: raw-input 
     
    4: [sensitive sinks]
    5:   construct: echo ( escaped-html   && escaped-slashes )
    6:   function:  mail ( matched-string || string-from-list, matched-string, matched-string )
     
    7: [function result]
    8:   function: addslashes       level: escaped-slashes

1.  Starts the section that lists the sources of
    [TaintedData](TaintedData){.twikiLink} in the configuration file.
    All sources that bring [TaintedData](TaintedData){.twikiLink} into
    your script should be defined here
2.  An input-array can be declared as bringing in
    [TaintedData](TaintedData){.twikiLink} by giving the keyword
    `array:` and the name followed by a
    [SafetyLevel](SafetyLevel){.twikiLink}. A
    [SafetyLevel](SafetyLevel){.twikiLink} is declared by
    `level: safety-level-name`.
3.  A function can be declared as
    [TaintedData](TaintedData){.twikiLink}-source in the same way, but
    the keyword is `function:`.
4.  Starts the [SensitiveSink](SensitiveSink){.twikiLink}-section of the
    configuration file. All functions and constructs that should be
    checked for preconditions should be defined here.
5.  The precondition for a construct can be defined by the keyword
    `construct:` followed by the name of the construct. This should be
    followed by a precondition for the parameters you want to check. A
    [SafetyLevel](SafetyLevel){.twikiLink} can be combined by the `&&`
    (and) or `||` (or) operator. These operators work as expected.
6.  Functions can be defined as
    [SensitiveSink](SensitiveSink){.twikiLink} in the same way as
    constructs, but the keyword is `function:`. This line also gives an
    example of the definition of preconditions for multiple parameters.
7.  Starts the section that defines the functions that make the data
    safe. All functions that can influence data should be defined in
    this section.
8.  Defining the [SafetyLevel](SafetyLevel){.twikiLink} of the result of
    a function can be done by using the `function:` keyword followed by
    a name and a [SafetyLevel](SafetyLevel){.twikiLink}.

[]{#Default_configuration} Default configuration
------------------------------------------------

The default configuration that is used by php-sat can be found under
*prefix* /share/php-sat and is called **PHP-SAT.ini**.

![ALERT!](../pub/TWiki/TWikiDocGraphics/warning.gif){width="16"
height="16"} Editting the default configuration file will **not**
influence php-sat directly.\
![ALERT!](../pub/TWiki/TWikiDocGraphics/warning.gif){width="16"
height="16"} After you have altered the file you should pass it to
php-sat using the `-cf f | --config-file f` flag.

The default configuration is currently very small. If you have an
improved version please share it with us.\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
