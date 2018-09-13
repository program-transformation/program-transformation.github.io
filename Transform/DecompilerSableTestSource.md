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
    Page](http://www.program-transformation.org/edit/Transform/DecompilerSableTestSource?t=1536826467)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/DecompilerSableTestSource)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/DecompilerSableTestSource)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/DecompilerSableTestSource?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/DecompilerSableTestSource?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    2](http://www.program-transformation.org/view/Transform/DecompilerSableTestSource?rev=1.2)
    [(diff 1)](http://www.program-transformation.org/rdiff/Transform/DecompilerSableTestSource?rev1=1.2&rev2=1.1)
-   [Rev
    1](http://www.program-transformation.org/view/Transform/DecompilerSableTestSource?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/DecompilerSableTestSource)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/DecompilerSableTestSource?template=oopsmore&param1=1.2&param2=1.2)
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
    \...](http://www.program-transformation.org/oops/Transform/DecompilerSableTestSource?template=oopsmore&param1=1.2&param2=1.2)
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
Decompiler Sable Test Source {#decompiler-sable-test-source .twikiTopicTitle}
============================

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

The paper [\"Decompiling Java Bytecode: Problems, Traps and
Pitfalls\"](http://www.sable.mcgill.ca/publications/papers/#cc2002-2)
contains this small but important test program (concatenation of 4 Java
source files):

    public class Circle implements Drawable {
        public int radius;
        public Circle(int r) {radius = r;}
        public boolean isFat() {return false;}
        public void draw() {
            // Code to draw...
        }
    }

    public class Rectangle implements Drawable {
        public short height, width;
        public Rectangle(short h, short w) {
            height = h; width = w; }
        public boolean isFat() {return (width > height);} 
        public void draw() {
            // Code to draw ...
        }
    }
    public interface Drawable {
        public void draw();
    }

    public class Main {

        public static void f(short i) {
            Circle c; Rectangle r; Drawable d;
            boolean is_fat;

            if (i > 10) {                   // 6
                r = new Rectangle(i, i);    // 7
                is_fat = r.isFat();         // 8
                d = r;                      // 9
            }
            else {
                c = new Circle(i);          // 12
                is_fat = c.isFat();         // 13
                d = c;                      // 14
            }
            if (!is_fat) d.draw();          // 16
        }                                   // 17

        public static void main(String args[])
            { f((short) 11); }
    }

The tricky thing about this program is the assignment to the local
variable `d`, which is of type `Drawable`. This really tests Java
decompilers, since the types of local variables is one of the two main
problems that they have.

\-- [MikeVanEmmerik](../Main/MikeVanEmmerik){.twikiLink} - 13 Feb 2003\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
