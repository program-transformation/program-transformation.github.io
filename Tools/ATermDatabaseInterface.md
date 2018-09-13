::: {.fullPage}
::: {.twikiMiddleContainer}
::: {.twikiLeftBar}
::: {.twikiLeftBarContents}
[Home](WebHome){.twikiLink}

**XT Tools**

-   [Reference Docs](ToolReference){.twikiLink}
-   [GPP](GenericPrettyPrinter){.twikiLink}
-   [ATerm](ATermTools){.twikiLink}
-   [SDF](SdfTools){.twikiLink}
-   [AsFix](AsFixTools){.twikiLink}

**Languages**

-   [Stratego](../Stratego/WebHome){.twikiLink}
-   [SDF](../Sdf/WebHome){.twikiLink}
-   [ATerm](ATermFormat){.twikiLink}

**Software**

-   [Stratego/XT](../Stratego/StrategoDownload){.twikiLink}
-   [SDF2 Bundle](../Sdf/SdfBundle){.twikiLink}
-   [KoalaCompiler](KoalaCompiler){.twikiLink}
-   [AutoBundle](AutoBundle){.twikiLink}
-   [AutoBuild](AutoBuild){.twikiLink}
-   [DailyBuildSystem](DailyBuildSystem){.twikiLink}

[![](http://www.program-transformation.org/twiki/pub/rss.gif "RSS 1.0 feed")](http://www.program-transformation.org/twiki/bin/view/Tools/WebRss?skin=rss)
:::
:::

::: {.twikiMain}
::: {.toolBar}
::: {.flexMenuBar}
::: {.flexMenu onmouseover="return showMenu(event, 100);" onmouseout="return hideMenu(event, 100);"}
Page

::: {#flexMenuContent100 .flexMenuContent}
-   [Edit
    Page](http://www.program-transformation.org/edit/Tools/ATermDatabaseInterface?t=1536826787)
-   [Rename
    Page](http://www.program-transformation.org/rename/Tools/ATermDatabaseInterface)
-   [Attach
    File](http://www.program-transformation.org/attach/Tools/ATermDatabaseInterface)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Tools/ATermDatabaseInterface?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Tools/ATermDatabaseInterface?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    10](http://www.program-transformation.org/view/Tools/ATermDatabaseInterface?rev=1.10)
    [(diff 9)](http://www.program-transformation.org/rdiff/Tools/ATermDatabaseInterface?rev1=1.10&rev2=1.9)
-   [Rev
    9](http://www.program-transformation.org/view/Tools/ATermDatabaseInterface?rev=1.9)
    [(diff 8)](http://www.program-transformation.org/rdiff/Tools/ATermDatabaseInterface?rev1=1.9&rev2=1.8)
-   [Rev
    8](http://www.program-transformation.org/view/Tools/ATermDatabaseInterface?rev=1.8)
    [(diff 7)](http://www.program-transformation.org/rdiff/Tools/ATermDatabaseInterface?rev1=1.8&rev2=1.7)
-   [Total
    History](http://www.program-transformation.org/rdiff/Tools/ATermDatabaseInterface)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Tools/ATermDatabaseInterface?template=oopsmore&param1=1.10&param2=1.10)
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
    \...](http://www.program-transformation.org/oops/Tools/ATermDatabaseInterface?template=oopsmore&param1=1.10&param2=1.10)
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
ATerm Database Interface {#aterm-database-interface .twikiTopicTitle}
========================

::: {.twikiWebTitle}
XT \-- A Bundle of Program Transformation Tools
:::

::: {.twikiToc}
-   [Description](ATermDatabaseInterface#Description)
-   [Interface](ATermDatabaseInterface#Interface)
-   [Invocation](ATermDatabaseInterface#Invocation)
-   [Download](ATermDatabaseInterface#Download)
-   [Implementation](ATermDatabaseInterface#Implementation)
-   [Installation](ATermDatabaseInterface#Installation)
    -   [Basic applications](ATermDatabaseInterface#Basic_applications)
    -   [Configuration and
        extension](ATermDatabaseInterface#Configuration_and_extension)
-   [Todo or might do](ATermDatabaseInterface#Todo_or_might_do)
:::

### []{#Description} Description

The [SATerm Database
Interface[^?^](http://www.program-transformation.org/edit/Tools/SATermDatabaseInterface?topicparent=Tools.ATermDatabaseInterface)]{.twikiNewLink
style="background : #FFFFCE;"} (aterm-dbi) offers an
[ATermServices](ATermService){.twikiLink} look on a relational database.
aterm-dbi uses Java Stratego.ATerm Servlets.

### []{#Interface} Interface

Currently there is just a query service. It is accessible on the URL
`aterm-dbi/query`. The query service is an
[ATermService](ATermService){.twikiLink} . It accepts a `Query` term in
the body of a HTTP POST request and returns the result of the query in
the body of the reponse.

For example this query:

      Query("SELECT ID, Name FROM Customer")

Might result in this `ResultSet` :

      ResultSet(
        MetaData(
          Columns(
            [ Column(Name("id"),   Type(Std("INTEGER"), Db("int4")))
            , Column(Name("name"), Type(Std("CHAR"),    Db("bpchar")))
            ]
          )
        )
      , Data(
         [ Row([160, "Meindert Kroese"])
         , Row([159, "Steven van Dijk"])
         , Row([158, "Martijn Schrage"])
         , Row([157, "Sandor Spruit"  ])
         ]
        )
      )

The Stratego.ATerm Database Interface rewrites values of SQL types to an
Stratego.ATerm representation. The current implementation can just
handle integer types (INTEGER, SMALLINT, and BIGINT) and string types
(CHAR, VARCHAR, and LONGVARCHAR). This will be extended in the future to
handle all SQL data types.

### []{#Invocation} Invocation

From Stratego you can invoke the services of aterm-dbi with the
`http-transform` strategy of
[StrategoNetworking](../Stratego/StrategoNetworking){.twikiLink}.

There is one problem: the Java implementation of the
[ATermLibrary](../Stratego/ATermLibrary){.twikiLink} doesn\'t provide a
reader for BAF, the [Binary Stratego.ATerm
Format[^?^](http://www.program-transformation.org/edit/Tools/BinaryStrategoATermFormat?topicparent=Tools.ATermDatabaseInterface)]{.twikiNewLink
style="background : #FFFFCE;"}. Because of this format is very
efficient, it is used by [XTC](../Stratego/XTC){.twikiLink} by default.
You should thus invoke the services of aterm-dbi in TAF, the [Textual
Stratego.ATerm
Format[^?^](http://www.program-transformation.org/edit/Tools/TextualStrategoATermFormat?topicparent=Tools.ATermDatabaseInterface)]{.twikiNewLink
style="background : #FFFFCE;"}. You could do this with this strategy:

      http-text-transform(service-url) =
        xtc-temp-files(
          write-to-text
        ; xtc-http-transform(service-url)
        ; read-from
        )

Invocation of the query service of aterm-dbi:

      <http-text-transform(!URL("http://127.0.0.1:8080/aterm-dbi/query"))>
          Query("SELECT ID, Name FROM Customer")

### []{#Download} Download

You can download the latest release at:

-   <http://losser.st-lab.cs.uu.nl/~mbravenb/software/aterm-dbi/>

The `war` file is a Java Web Archive, a binary distribution. You can
immediately put this file in your servlet container. The .tar.gz files
are source distributions. You need [Ant](http://ant.apache.org) to build
the sources.

You can also get the latest sources from the Subversion repository:

      svn checkout %SVNSTRATEGOXT%/trunk/experimental/aterm-dbi

See [latest
sources[^?^](http://www.program-transformation.org/edit/Tools/LatestSources?topicparent=Tools.ATermDatabaseInterface)]{.twikiNewLink
style="background : #FFFFCE;"} for more information on how to checkout
packages from the [StrategoXT](../Stratego/StrategoXT){.twikiLink}
subversion repository.

In the samples package of [Stratego
Networking[^?^](http://www.program-transformation.org/edit/Tools/StrategoNetworking?topicparent=Tools.ATermDatabaseInterface)]{.twikiNewLink
style="background : #FFFFCE;"} you can find some samples in the
`xmpl/aterm-dbi` directory (unreleased, use the Subversion repository).

### []{#Implementation} Implementation

aterm-dbi is a J2EE application. It uses a JDBC `DataSource` that is
made available by the application server it is hosted in via the JNDI.
Advantages of this approach:

-   by using techniques developed for database servers that should be
    able to handle a lot of requests, the Stratego.ATerm Database
    Interface scales very well.

<!-- -->

-   You don\'t need to modify any Java code to use a different database
    managament system, or one at a different location.

### []{#Installation} Installation

You should be able to run the Stratego.ATerm database interface on any
J2EE Application Server and using any database system implementation (as
long as there is a JDBC 3 driver available).

I will provide instructions for a configuration where I\'m using Tomcat
5 and PostgreSQL. Please consult the documentation of the application
and database server if you choose other software.

#### []{#Basic_applications} Basic applications

First of all you need a [PostgreSQL](http://www.postgresql.org/)
database. You need version 7.2 or 7.3. Please refer to the documentation
of PostgreSQL if you need to install the database system by yourself.

You need a [Java 2 SDK](http://java.sun.com/j2se/) to run Tomcat. It is
wise to use a recent release (version 1.4.x). Make sure the environment
variable JAVA\_HOME points to the location where you installed your
J2SDK.

Next, you need [Tomcat 5](http://jakarta.apache.org/tomcat/). Tomcat 4
will not do the job! Installation of Tomcat 5 is very straightforward
nowadays.

#### []{#Configuration_and_extension} Configuration and extension

Now the basic components of Java based database application are
available, now comes the Stratego.ATerm database interface specific
part.

You need a [JDBC3 driver for your
DBMS](http://industry.java.sun.com/products/jdbc/drivers), in this case
the [JDBC3 driver for PostgreSQL](http://jdbc.postgresql.org/). Put it
in the `common/lib` directory of your Tomcat installation.

Now it\'s finally time to install the web archive (.war) of aterm-dbi.
You should put this war in the `webapps` directory of Tomcat.

We still have to configure Tomcat with the database you want to use.
This is application server and database specific, so you will probably
need to consult some other documentation.

In Tomcat you should add this to the `Host` element with the `name`
attribute `localhost`:

      <Context path="/aterm-dbi" docBase="aterm-dbi.war" debug="5" reloadable="true">
        <Logger className="org.apache.catalina.logger.FileLogger"
                   prefix="aterm-dbi-log."
                   suffix=".txt"
                timestamp="true"/>

        <Resource name="jdbc/aterm-dbi"
                  auth="Container"
                  type="org.postgresql.jdbc3.Jdbc3PoolingDataSource"/>

        <ResourceParams name="jdbc/aterm-dbi">
          <parameter>
            <name>factory</name>
            <value>org.postgresql.jdbc3.Jdbc3ObjectFactory</value>
          </parameter>

          <parameter>
             <name>databaseName</name><value>.....</value>
          </parameter>

          <parameter>
             <name>serverName</name><value>127.0.0.1</value>
          </parameter>

          <parameter>
            <name>user</name><value>....</value>
          </parameter>

          <parameter>
           <name>password</name><value>.....</value>
          </parameter>
        </ResourceParams>
      </Context>

Of course you should fill in your database-, server-, and username and
your password.

We\'ve chosen the `PoolingDataSource` implementation of the PostgreSQL
JDBC driver, but if your application server offers a connection pooling
implementation which interfaces with a `ConnectionPoolDataSource`, you
should choose that option.

### []{#Todo_or_might_do} Todo or might do

-   Implement services for inserts, updates and deletes. Maybe use terms
    instead of concrete syntax in some cases.

<!-- -->

-   Convert more SQL data types like bit, boolean, dates etc.

<!-- -->

-   Conceptually it is much more attractive to send an AST
    representation of the SQL statements to the
    [ATermService](ATermService){.twikiLink} instead of concrete syntax
    for SQL in an Stratego.ATerm wrapper. This would be an excellent
    combination with the use of
    [ConcreteSyntax](../Stratego/ConcreteSyntax){.twikiLink} for SQL in
    Stratego. This would at compile-time ensure syntactical correctness
    of the SQL statements. There are some problems:
    -   Many SQL statements use database specific constructs. The
        practical use of the [Stratego.ATerm Database
        Interface[^?^](http://www.program-transformation.org/edit/Stratego/ATermDatabaseInterface?topicparent=Tools.ATermDatabaseInterface)]{.twikiNewLink
        style="background : #FFFFCE;"} would decrease if we would
        enforce standard SQL.
    -   We need a [PrettyPrinter](../Stratego/PrettyPrinter){.twikiLink}
        on the server-side, because the database system (well, JDBC)
        just accepts concrete syntax for SQL.
    -   We need a SQL syntax definition (but a starting-point is already
        available)

\-- [MartinBravenboer](../Main/MartinBravenboer){.twikiLink} - 10 Mar
2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
*Tools.ATermDatabaseInterface moved from Stratego.ATermDatabaseInterface
on 03 Dec 2004 - 01:33 by
[MartinBravenboer](../Main/MartinBravenboer){.twikiLink}* - [put it
back](http://www.program-transformation.org/rename/Tools/ATermDatabaseInterface?newweb=Stratego&newtopic=ATermDatabaseInterface&confirm=on "Click to move topic back to previous location, with option to change references.")
:::
:::
:::
:::
