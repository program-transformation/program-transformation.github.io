::: {#content}
::: {#header}
![Stratego
Logo](http://stratego.insanity.nl/StrategoLogoTextlessWhite-100px.png)

<div>

[Octave](WebHome){.twikiLink} {#web-title}
=============================

Octave-Compiler.org

</div>
:::

::: {#main}
::: {#main2}
Octave To C {#octave-to-c .topic-header}
===========

::: {.topic-text}
The [Octave to C++ Backend](OctaveToC){.twikiLink} is a C++ code
generator. It performs the following translations,

-   [Octave to
    .oct[^?^](http://www.program-transformation.org/edit/Octave/OctaveToOct?topicparent=Octave.OctaveToC)]{.twikiNewLink
    style="background : #FFFFCE;"} ([dynamically linked
    function[^?^](http://www.program-transformation.org/edit/Octave/DynamicallyLinkedFunction?topicparent=Octave.OctaveToC)]{.twikiNewLink
    style="background : #FFFFCE;"}
-   [Octave to C++
    (standalone)[^?^](http://www.program-transformation.org/edit/Octave/OctaveToC++Standalone?topicparent=Octave.OctaveToC)]{.twikiNewLink
    style="background : #FFFFCE;"}

The latest sources of the Octave Optimizer can be found at

-   <https://svn.cs.uu.nl:12443/repos/octave/octavec/trunk/octave2c/>

### []{#Example_factorial}[]{#Example_factorial_} Example (factorial)

Consider the following Octave function,

    function x = factorial(n)
         x = 1;
         while(n>1)
          x = x * n;
          n = n -1;
         end
    endfunction

Using [Octave to
.oct[^?^](http://www.program-transformation.org/edit/Octave/OctaveToOct?topicparent=Octave.OctaveToC)]{.twikiNewLink
style="background : #FFFFCE;"} compilation, it results in (without the
includes),

    DEFUN_DLD (factorial, args, nargout, "")
    {
      octave_value_list c_0;
      octave_value x;
      octave_value n;
      n = args(0);
      x = 1;
      while ( do_binary_op(octave_value::op_gt, n, 1).all().all().bool_array_value()(0) )
        {
          x = do_binary_op(octave_value::op_mul, x, n);
          n = do_binary_op(octave_value::op_sub, n, 1);
        }
      c_0(0) = x;
      return(c_0);
    }

Using [Octave to C++
(standalone)[^?^](http://www.program-transformation.org/edit/Octave/OctaveToC++Standalone?topicparent=Octave.OctaveToC)]{.twikiNewLink
style="background : #FFFFCE;"} compilation, the following script

    for n = 1:1000
       b = factorial(n);
    end
    b

results in,

    void a_0_c_0 ()
    {
      double n;
      double b;
      int d_0;
      for ( d_0 = 0 ; (d_0 < floor((((1000 - 1) + 1) / 1))) ; d_0++ )
        {
          n = (1 + (d_0 * 1));
          b = factorial_d_0(n);
        }
      set_global_value("ans", b);
      get_global_value("ans").print_name_tag(std::cout, "ans");
      get_global_value("ans").print(std::cout);
    }
    double factorial_d_0 (double n)
    {
      double x;
      x = 1;
      while ( (n > 1) )
        {
          x = (x * n);
          n = (n - 1);
        }
      return(x);
    }
    int main ()
    {
      init_octave_internals();
      a_0_c_0();
    }
:::
:::
:::

::: {#sidebar}
::: {.box}
::: {.box2}
[Home](WebHome){.twikiLink} {#home .sidebar-title}
---------------------------

-   [About](AboutOctaveCompiler){.twikiLink}
-   [News](OctaveCompilerNews){.twikiLink}
-   [Documentation](OctaveCompilerDocumentation){.twikiLink}
-   [Bugs](https://catamaran.labs.cs.uu.nl/jira/browse/OCT)
-   [Download](OctaveCompilerDownload){.twikiLink}

\
\
:::
:::
:::

::: {#footer}
<div>

<div>

------------------------------------------------------------------------

[search](WebSearch){.twikiLink} \| [index](WebIndex){.twikiLink} \|
[recent changes](WebChanges){.twikiLink} \|
[statistics](WebStatistics){.twikiLink}    
[printable](http://www.program-transformation.org/view/Octave/OctaveToC?skin=print)
\|
[refresh](http://www.program-transformation.org/fresh/Octave/OctaveToC)
\|
[edit](http://www.program-transformation.org/edit/Octave/OctaveToC?t=1536826798)
\|
[history](http://www.program-transformation.org/rdiff/Octave/OctaveToC)
\| [more
actions](http://www.program-transformation.org/oops/Octave/OctaveToC?template=oopsmore&param1=1.3&param2=1.3)

</div>

</div>
:::
:::
