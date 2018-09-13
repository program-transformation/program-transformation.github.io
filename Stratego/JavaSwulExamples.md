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
    Page](http://www.program-transformation.org/edit/Stratego/JavaSwulExamples?t=1536825594)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/JavaSwulExamples)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/JavaSwulExamples)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/JavaSwulExamples?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/JavaSwulExamples?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    6](http://www.program-transformation.org/view/Stratego/JavaSwulExamples?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/JavaSwulExamples?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/JavaSwulExamples?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/JavaSwulExamples?rev1=1.5&rev2=1.4)
-   [Rev
    4](http://www.program-transformation.org/view/Stratego/JavaSwulExamples?rev=1.4)
    [(diff 3)](http://www.program-transformation.org/rdiff/Stratego/JavaSwulExamples?rev1=1.4&rev2=1.3)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/JavaSwulExamples)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/JavaSwulExamples?template=oopsmore&param1=1.6&param2=1.6)
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
    \...](http://www.program-transformation.org/oops/Stratego/JavaSwulExamples?template=oopsmore&param1=1.6&param2=1.6)
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
Java Swul Examples {#java-swul-examples .twikiTopicTitle}
==================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

::: {.twikiToc}
-   [Introduction](JavaSwulExamples#Introduction)
-   [Nesting panels](JavaSwulExamples#Nesting_panels)
-   [Menubar](JavaSwulExamples#Menubar)
-   [Events](JavaSwulExamples#Events)
-   [Creating a GridBagLayout with
    ease](JavaSwulExamples#Creating_a_GridBagLayout_with_ea)
-   [Widget-o-rama](JavaSwulExamples#Widget_o_rama)
:::

[]{#Introduction} Introduction
------------------------------

The examples covered in this page show some of the capabilities of
[Java-Swul](Java-Swul){.twikiLink}. All the examples are based on code
in the `xmpl` directory in the [Java-Swul
repository](https://svn.cs.uu.nl:12443/repos/StrategoXT/java-swul/).

[]{#Nesting_panels} Nesting panels
----------------------------------

The following Java-Swul code is taken from a file called
`xmpl/Test3.javaswul` in the Java-Swul package.

    import javax.swing.*;
    import java.awt.*;
      
    public class Test3 {
      public static void main(String[] ps) {
        JFrame frame = frame {
          title = "Welcome!"
          content = panel of border layout {
            center = label { text = "Hello World" }
            south = panel of grid layout {
              row = {
                button { text = "cancel" }
                button { text = "ok"}
              }
            }
          }
        };
        frame.pack();
        frame.setVisible(true);
      }
    }

When we assimilate/compile/run
(`swulc -i Test3.javaswul -o Test3.java && javac Test3.java && java Test3`)
this program this will produce:

![Test3.png](http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/Test3.png)

The curious will immidiatly wonder what the command
`swulc -i Test3.javaswul -o Test3.java` will produce in Test3.java. This
is shown below.

    import javax.swing.*;
    import java.awt.*;
     
    public class Test3
    {
      public static void main(String[] ps)
      {
        JButton jButton_1;
        JButton jButton_0;
        JPanel jPanel_1;
        JLabel jLabel_0;
        JPanel jPanel_0;
        JFrame jFrame_0;
        jFrame_0 = new JFrame();
        jFrame_0.setTitle("Welcome!");
        jPanel_0 = new JPanel();
        BorderLayout borderLayout_0 = new BorderLayout();
        jPanel_0.setLayout(borderLayout_0);
        jFrame_0.setContentPane(jPanel_0);
        JFrame frame = jFrame_0;
        jLabel_0 = new JLabel();
        jLabel_0.setText("Hello World");
        jPanel_0.add(jLabel_0, BorderLayout.CENTER);
        jPanel_1 = new JPanel();
        GridLayout gridLayout_0 = new GridLayout(1, 2);
        jButton_0 = new JButton();
        jButton_0.setText("cancel");
        jButton_1 = new JButton();
        jButton_1.setText("ok");
        jPanel_1.setLayout(gridLayout_0);
        jPanel_1.add(jButton_0);
        jPanel_1.add(jButton_1);
        jPanel_0.add(jPanel_1, BorderLayout.SOUTH);
        frame.pack();
        frame.setVisible(true);
      }
    }

[]{#Menubar} Menubar
--------------------

The creating of menubars is an excellent example of where in Java the
long list of statements becomes an unreadable and hard to understand
mess. The best example is the url where Sun explains [how to use
Menus](http://java.sun.com/docs/books/tutorial/uiswing/components/menu.html).

This demostration menubar looks like this:

![MenuLookDemo.png](http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/MenuLookDemo.png)

The code that generates this menu is not immidiatly clear in itself.
Extra measures are needed as you can see in the next code sniplet.

![MenuLookDemo2.png](http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/MenuLookDemo2.png)

To accomplisch the same as shown in the above code sniplet you could
write in Java-Swul the following:

    menu item {
      text = "Both text and icon"
      icon = "images/middle.gif"
      mnemonic = b
    }
    menu item {
      icon = "images/middle.gif"
      mnemonic = d
    }
    menu separator
    menu radiobutton {
      text = "A radio button menu item"
      group = a
      selected = true
      mnemonic = r
    }
    menu radiobutton {
      text = "Another one"
      mnemonic = o
      group = a
    }

Complete Java-Swul source and generated source can be downloaded.

-   <http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/MenuLookDemo.javaswul>
-   <http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/MenuLookDemo.java>
    (generated)
-   <http://java.sun.com/docs/books/tutorial/uiswing/components/example-1dot4/MenuLookDemo.java>
    (from java.sun.com)

[]{#Events} Events
------------------

To demonstrate how the events that the userinterface components generate
can be handled in Java-Swul we take the following interface.

![Test19.png](http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/Test19.png)

Event handlers are connected to the window, the file menu, an item in
the file menu, to the button and to the slider. That an event from of
user interface component shoud be listened to and how it should be
handled is declared as a property of a Swul component. The right hand
side of such a property is an block of Java statements. The following
piece of code shows how the previous user interface is created and how
the event handlers are declared.

    import javax.swing.*;
    import java.awt.*;
    import java.beans.*;
    import java.awt.event.*;
    import javax.swing.event.*;
     
    public class Test19 {

      public static void main(String[] ps) {
        JFrame frame = frame {
          window event = { System.out.println("I'm a frame on fire!"); }
          menubar = {
            menu {
              menu event = { System.out.println("Fired event: "+event.toString()); }
              text = "File"
              items = { 
                menu item {
                  text = "New"
                  action event = { System.out.println("Create something new"); }
                }
                menu item {
                  text = "Open"
                }
              }
            }
            
          }
          content = panel of border layout {
            south = button {
              text = "Click-y-click"
              action event = { 
                Test19.handleClick() ; 
                System.out.println("Click-y-click some more");
              }
            }
            center = slider named aSlider {
              change event = {
                System.out.println(aSlider.getValue());
              }
            }
          }
          title = "Hello world"
        };
        frame.pack();
        frame.setVisible(true);
      }
      
      public static void handleClick(){
        System.out.println("Click-y-click once");
      }
    }

The event blocks are collected into a new innerclass that is created in
the class where the events properties were declared. The components are
connected to the methods in this new innerclass by the creation and
connection of EventHandler objects. In this way only a single object is
created to hold the reactions to events and the EventHandler uses
proxies to create only a single object per eventtype. This reduces the
footprint of the Java program when an eventtype accurs more then once
compared to the classic method of using (annoymous-)innerclasses per
event.

Some of the generated code to create and connect the components is shown
here:

    jFrame_0.addWindowListener   ((WindowListener)EventHandler.create(WindowListener.class, classHandler_0, "windowListener_0", ""));
    jMenu_0.addMenuListener      ((MenuListener)  EventHandler.create(MenuListener.class,   classHandler_0, "menuListener_0",   ""));
    jMenuItem_0.addActionListener((ActionListener)EventHandler.create(ActionListener.class, classHandler_0, "actionListener_0", ""));
    jButton_0.addActionListener  ((ActionListener)EventHandler.create(ActionListener.class, classHandler_0, "actionListener_1", ""));
    aSlider.addChangeListener    ((ChangeListener)EventHandler.create(ChangeListener.class, classHandler_0, "changeListener_0", ""));
    ...
      public static class ClassHandler_0 {
        ClassHandler_0 () { }

        public void changeListener_0(ChangeEvent event) {
          System.out.println(aSlider.getValue());
        }

        public void actionListener_1(ActionEvent event) {
          Test19.handleClick();
          System.out.println("Click-y-click some more");
        }

        public void actionListener_0(ActionEvent event) {
          System.out.println("Create something new");
        }

        public void menuListener_0(MenuEvent event) {
          System.out.println("Fired event: " + event.toString());
        }

        public void windowListener_0(WindowEvent event) {
          System.out.println("I'm a frame on fire!");
        }
      }

Complete Java-Swul source and generated source can be downloaded.

-   <http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/Test19.javaswul>
-   <http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/Test19.java>
    (generated)

[]{#Creating_a_GridBagLayout_with_ea} Creating a GridBagLayout with ease
------------------------------------------------------------------------

A GridBagLayout is in practice a complex layout. If you would create a
layout of your components with this layoutmanager this often means
calculation of cell locations and width/height values.

Take for instance the following interface:

![Test17.png](http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/Test17.png)

Components can span multiple cells. In the example they span horizontal,
vertical, both or neither. Java-Swul can calculate the values of the
width, height, x-position and y-position for you. The input for this
calculation is a more understandable way of writing down how the grid
should be filled.

The above screen is the result of the following java / java-swul code.
Placement of components is closer to the concept that a gridlayout
offers, making it easier to create and alter a gridlayout.

    import javax.swing.*;
    import java.awt.*;

    public class Test17 {
      public static void main(String[] ps) {
        JFrame f = frame {
          title = "Welcome!"
          content = panel of border layout {
            center = panel of gridbag layout {
              row = { new JButton("Button1") new JButton("Button2") <<<                    <<<                    }
              row = { new JButton("Button3") <<<                    ___                    new JButton("Button4") }
              row = { ___                    new JButton("Button5") new JButton("Button6") ^^^                    }
              row = { new JButton("Button7") <<<                    new JButton("Button8") ^^^                    }
              row = { ^^^                    ___                    new JButton("Button9") <<<                    }
            }
          }
        };
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        f.pack();
        f.setSize(f.getPreferredSize());
        f.setVisible(true);
      }
    }

Complete Java-Swul source and generated source can be downloaded.

-   <http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/Test17.javaswul>
-   <http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/Test17.java>

[]{#Widget_o_rama} Widget-o-rama
--------------------------------

The next screenshot is from a file called `xmpl/Test16.javaswul` in the
Java-Swul package.

![Test16.png](http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/Test16.png)

The Java-Swul source used to create this crowded interface contains the
next code-example. The surrounding Java code is left out to save some
space. The complete Java code is further down on this page.

        this {
          title = "Welcome"
          content = panel {
            border = raised bevel border
            layout = border layout {
              north = scrollpane of panel of grid layout {
                row = { textarea { 
                    rows   = 10
                    columns = 10
                    text = "A 10 by 10 textarea"
                  }
                  tree { }
                }
              }
              center = panel of grid layout {
                row = {
                  label { 
                    text = "This an JLabel" 
                  }
                  button { 
                    text = "This is a JButton" 
                  }
                  slider {
                  }
                }
                row = {
                  radiobutton {
                    text = "JRadioButton in a group"
                    group = radiogroup1
                    selected = true
                  }
                  textfield { 
                    text = "a JTextField" 
                  }
                  progressbar { 
                    value = 23 
                  }
                } 
                row = {
                  checkbox { 
                    text = "a JCheckBox in a group" 
                  }
                  combobox { 
                  }
                  togglebutton { 
                    text = "a JToggleButton" 
                    group = someGroup
                  }
                }
                row = {
                  radiobutton {
                    text = "another JRadioButton"
                    group = radiogroup1
                  }
                  label {
                  }
                  togglebutton { 
                    text = "another JToggleButton" 
                    group = someGroup
                    selected = true
                  } 
                } 
              }
            }
          }
        };

As you can see it is quite verbose. Writing things down in this
structured way causes lots of lines with just an `}` and spaces.
Java-Swul has some sugur to it. The line
`scrollpane of panel of grid layout { row = { ... } }` is short for:

    scrollpane { 
      content = panel {
        layout = grid layout {
          row = { ... }
        }
      }
    }

So you can skip nestings that are acceptable with default properties.

Complete Java-Swul source and generated source can be downloaded.

-   <http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/Test16.javaswul>
-   <http://www.stratego-language.org//pub/Stratego/JavaSwulExamples/Test16.java>

\-- [ReneDeGroot](../Main/ReneDeGroot){.twikiLink} - 15 Dec 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
