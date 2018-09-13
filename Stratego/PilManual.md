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
    Page](http://www.program-transformation.org/edit/Stratego/PilManual?t=1536825607)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/PilManual)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/PilManual)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/PilManual?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/PilManual?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Stratego/PilManual?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/PilManual)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/PilManual?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Stratego/PilManual?template=oopsmore&param1=1.1&param2=1.1)
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
Pil Manual {#pil-manual .twikiTopicTitle}
==========

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

[]{#A_simple_PIL_tutorial} A simple [PIL](PIL){.twikiLink} tutorial
-------------------------------------------------------------------

[PIL](PIL){.twikiLink} is a language based on a small subset of Java,
but simpler and with a few subtle differences and convenient additions.
Let\'s start with the famous \"Hello world!\" example. Create a new file
*hello.pil*:

    void main(Array<String> args) {
      println("Hello world!");
    }

You can now generate Java code from this program using:

    pilc -i hello.pil --java

or Python code:

    pilc -i hello.pil --python

Code is generated in the *out/* directory, optionally this destination
directory can be set with the -d switch.

Both the Python and Java back-ends need a small run-time library to run
the software. In the case of Java you can compile and run the generated
code using (assuming you installed it with Nix, otherwise, replace the
path):

    javac -cp out:/nix/store/*-pil-*/share/pil/pil.jar application/Main.java
    java -cp out:/nix/store/*-pil-*/share/pil/pil.jar application.Main

But, because this is kind of annoying for simply testing, the
[PIL](PIL){.twikiLink} distribution comes with convenient *pil-java* and
*pil-python* wrapper scripts that compile and run the program for you:

    $ pil-java hello.pil
    [ pilc | info ] Now compiling: hello.pil
    [ pilc | info ] Done with hello.pil
    Hello world!
    $ pil-python hello.pil
    [ pilc | info ] Now compiling: hello.pil
    [ pilc | info ] Done with hello.pil
    Hello world!

[]{#Word_frequency} Word frequency
----------------------------------

You will have noticed that unlike Java, [PIL](PIL){.twikiLink} also
support global function, i.e. methods that are not part of a class. Here
is a slightly more complicate example that also uses the simple type
inferencing features of [PIL](PIL){.twikiLink} (the *var* keyword):

    List<String> cutIntoWords(String text) {
      var i = 0;
      var words = new List<String>();
      var word = new MutableString();
      while(i < text.length) {
        if(text[i] == ' ') {
          words.add(word.as<String>);
          word = new MutableString();
          while(text[i] == ' ') {
            i = i + 1;
          }
        } else {
          word.append(text[i]);
          i = i + 1;
        }
      }
      words.add(word.as<String>);
      return words;
    }

    Map<String, Int> wordFrequency(String text) {
      var words = cutIntoWords(text);
      var freq = new Map<String, Int>();
      for(String word : words) {
        if(freq.contains(word)) {
          freq[word] = freq[word] + 1;
        } else {
          freq[word] = 1;
        }
      }
      return freq;
    }

    void main(Array<String> args) {
      var sentence = "This a sentence and I wonder if it can calculate the word frequency of each of these words and if it works";
      println(sentence);
      println(wordFrequency(sentence));
    }

And running it:

    $ pil-java parseSentence.pil
    [ pilc | info ] Now compiling: parseSentence.pil
    [ pilc | info ] Done with parseSentence.pil
    This a sentence and I wonder if it can calculate the word frequency of each of these words and if it works
    {it=2, can=1, calculate=1, a=1, sentence=1, the=1, frequency=1, This=1, I=1, works=1, and=2, of=2, words=1, if=2, wonder=1, word=1, each=1, these=1}
    $ pil-python parseSentence.pil
    [ pilc | info ] Now compiling: parseSentence.pil
    [ pilc | info ] Done with parseSentence.pil
    This a sentence and I wonder if it can calculate the word frequency of each of these words and if it works
    {'a': 1, 'and': 2, 'works': 1, 'word': 1, 'calculate': 1, 'sentence': 1, 'This': 1, 'of': 2, 'it': 2, 'I': 1, 'frequency': 1, 'these': 1, 'can': 1, 'words': 1, 'each': 1, 'the': 1, 'if': 2, 'wonder': 1}

\-- [ZefHemel](../Main/ZefHemel){.twikiLink} - 02 Oct 2009\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
