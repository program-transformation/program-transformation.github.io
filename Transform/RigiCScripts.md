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
    Page](http://www.program-transformation.org/edit/Transform/RigiCScripts?t=1536826551)
-   [Rename
    Page](http://www.program-transformation.org/rename/Transform/RigiCScripts)
-   [Attach
    File](http://www.program-transformation.org/attach/Transform/RigiCScripts)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Transform/RigiCScripts?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Transform/RigiCScripts?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    1](http://www.program-transformation.org/view/Transform/RigiCScripts?rev=1.1)
-   [Total
    History](http://www.program-transformation.org/rdiff/Transform/RigiCScripts)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Transform/RigiCScripts?template=oopsmore&param1=1.1&param2=1.1)
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
    \...](http://www.program-transformation.org/oops/Transform/RigiCScripts?template=oopsmore&param1=1.1&param2=1.1)
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
Rigi CScripts {#rigi-cscripts .twikiTopicTitle}
=============

::: {.twikiWebTitle}
Program-Transformation.Org: The Program Transformation Wiki
:::

A sample RCL script that is used to pre-process the
[RSF](RSF){.twikiLink} generated with `cparse` for Rigi has been written
by [JohannesMartin](JohannesMartin){.twikiLink}. The RCL script is
generic and works for most C programs. He also used the script (with
slight modifications) to look at web site structures.

Note that the preprocessing takes away detail and creates a specific
structure in the graph. For example, all of the standard library is
filtered out. You can use the script as a starting point and modify it
to suit your own, specific needs.

    # load rsf file and perform some preliminary modifications
    proc load_cprog {filename} {
        set_domain cparse 0
        rcl_win_set_drawing 0
        rcl_load_rsf $filename
        puts "Delete standard library nodes..."
        c_delete_std
        puts "Delete disconnected variables..."
        c_delete_disconnected Variable
        puts "Delete disconnected prototypes..."
        c_delete_disconnected Prototype
        puts "Delete disconnected datatypes..."
        c_delete_disconnected Datatype
        puts "Delete disconnected constants..."
        c_delete_disconnected Constant
        puts "Delete disconnected functions..."
        c_delete_disconnected Function
        puts "Delete disconnected unknowns..."
        c_delete_disconnected Unknown

        puts "Redirecting prototypes..."
        c_redirect Prototype prototypes
        puts "Redirecting external variable declarations..."
        c_redirect Variable declares
        c_redirect Constant declares
        puts "Redirecting datatypes..."
        c_redirect Datatype isTheSameAs 
        puts "Collapsing function parameters..."
        c_collapse2 Function isDefinedIn in

        puts "Delete disconnected variables..."
        c_delete_disconnected Variable
        puts "Delete disconnected prototypes..."
        c_delete_disconnected Prototype
        puts "Delete disconnected datatypes..."
        c_delete_disconnected Datatype
        puts "Delete disconnected constants..."
        c_delete_disconnected Constant
        puts "Delete disconnected functions..."
        c_delete_disconnected Function
        puts "Delete disconnected unknowns..."
        c_delete_disconnected Unknown

        rcl_grid_all
        rcl_win_set_drawing 1
        rcl_refresh
    }


    # Delete every nodes that represent artifacts out of the standard library
    # (/usr/include/*) and standard data types.
    proc c_delete_std { } {
        rcl_select_none
        rcl_select_grep ".*/usr/include/.*"
        rcl_select_name int 1
        rcl_select_name char 1
        rcl_select_name long 1
        rcl_select_name void 1
        rcl_select_name float 1
        rcl_select_name double 1
        
        set winnodes [rcl_select_get_list]
        rcl_select_none

        foreach node $winnodes {
       rcl_node_delete $node
        }
    }


    # For all nodes of type ntype (winnodes), find a target node
    # (destination) for a first (and only) outgoing arc of type atype (arc1).
    # Redirect all incoming arcs of nodes belonging to 'winnodes' to enter
    # node 'destination'.
    # Delete winnodes and their dependencies out of the graph  
    # an example of usage: c_redirect Prototype prototypes
    proc c_redirect {ntype atype} {
        rcl_select_none
        rcl_select_type $ntype
        set winnodes [rcl_select_get_list]
        rcl_select_none
        
        foreach node $winnodes {
       set arclist [rcl_node_get_arclist $node $atype out 0 0]
       if { [llength $arclist] >= 1 } {        
           set arc1 [lindex $arclist 0]
           set enterings [rcl_node_get_arclist_in_window $node any in]
           set destination [rcl_get_arc_dst $arc1]
           foreach arc2 $enterings {
          set type [rcl_get_arc_type $arc2]
          if { [rcl_get_arctype level] != $type } {
              set source [rcl_get_arc_src $arc2]
              rcl_arc_create2 $source $destination $type
          }
           }
           rcl_node_delete $node
       }
        }   
        rcl_refresh
    }


    # For all nodes of type ntype, collapse them and all nodes
    # that are connected to them with an arc of type atype 
    # (the direction of the connection is dir)
    # to a single node (the collapsed node is given the same name as 
    # the original ntype type nodes).
    # an exampe of usage: c_collapse Function isDefinedIn in
    proc c_collapse {ntype atype dir} {
        rcl_select_none
        rcl_select_type $ntype
        set winnodes [rcl_select_get_list]
        rcl_select_none

        foreach node $winnodes {
       rcl_select_id $node
       set name [rcl_get_node_name $node]
       select_neighbors $atype $dir 1
       if {[rcl_collapse Collapse $name] == 0} { return }
        }
    }


    # For all nodes of type ntype:
    # - collapse all nodes that are connected to the node with an arc of 
    #   type atype (the direction of the connection is dir) to a single node.
    # - redirect all arcs going to or coming from the node to the
    #   new collapsed node.
    # - give the new collapsed node the name of the original node
    #   delete the original node
    # an exampe of usage: c_collapse Function isDefinedIn in
    proc c_collapse2 {ntype atype dir} {
        rcl_select_none
        rcl_select_type $ntype
        set winnodes [rcl_select_get_list]
        rcl_select_none

        foreach node $winnodes {
       rcl_select_id $node
       select_neighbors $atype $dir 1
       rcl_select_deselect_id $node
       if { [ llength [ rcl_select_get_list ] ] >= 1 } {
           if { [ rcl_collapse $ntype [ rcl_get_node_name $node ] ] == 0} { 
          return 
           }
           set id [rcl_select_get_list]

           set arclist [ rcl_node_get_arclist $node any out 1 1 ]
           foreach arc $arclist {
          set type [rcl_get_arc_type $arc]
          set dst [rcl_get_arc_dst $arc]
          if { $id != $dst } {
              rcl_arc_create2 $id $dst $type
          }
           }
           set arclist [ rcl_node_get_arclist $node any in 1 1 ]
           foreach arc $arclist {
          set type [rcl_get_arc_type $arc]
          set src [rcl_get_arc_src $arc]
          if { $src != $id } {
              rcl_arc_create2 $src $id $type
          }
           }
           rcl_node_delete $node
       }
        }
    }


    # Delete disconnected nodes of type 'ntype' from the graph
    # an example of usage: c_delete_disconnected Variable
    proc c_delete_disconnected {ntype} {
        rcl_select_none
        rcl_select_type $ntype
        set winnodes [rcl_select_get_list]
        rcl_select_none
        
        foreach node $winnodes {
       set nnodes [rcl_node_get_neighbors_in_window $node any any]
       if {[llength $nnodes] < 1} {
           rcl_node_delete $node
       }
        }
        rcl_refresh
    }


    # Find partitions of the graph that are connected with arcs of type atype
    # and make them into subsystems.
    proc c_partition {atype} {
        rcl_set_current_arctype $atype
        while { 1 } {
       rcl_select_all
       set nodes [rcl_select_get_list]
       foreach id $nodes {
           rcl_select_id $id
           set oldnum 0
           set newnum 1
           while { $newnum > $oldnum } {
          rcl_select_forward_tree
          rcl_select_reverse_tree
          set oldnum $newnum
          set newnum [rcl_select_num_nodes]
           }
           if { $newnum > 1 } {
          puts "Collapsing $newnum nodes..."
          rcl_collapse Collapse "Subsystem ($newnum children)"
          set id 0
          break
           }
       }
       if { $id != 0 } {
           break
       }
        }
    }


    # Find partitions of the graph by node names and make them into subsystems.
    # Name is a regular expression characterizing the names of all nodes to be 
    # collapsed.
    proc c_partition_by_name {name} {
        rcl_select_none
        rcl_select_grep "$name"
        set num [rcl_select_num_nodes]
        if { $num > 1 } {
       puts "Collapsing $num nodes for library $name..."
       rcl_collapse Collapse "$name Subsystem ($num children)"
        }
    }

    # Remove mangling from names and move into annotate attribute
    proc c_unmangle_names {} {
        rcl_select_all
        set nodes [rcl_select_get_list]
        foreach id $nodes {
       set name [rcl_get_node_name $id]
       if { [regsub {^([^^]*)\^.*} "$name" {\1} newname] > 0 } {
           rcl_set_node_name $id $newname
           regsub {^([^^]*)\^(.*)} "$name" {\2} annotate
           rcl_set_node_attr $id annotate $annotate
       }
        }
        rcl_refresh
    }

------------------------------------------------------------------------

[CategoryRigi](CategoryRigi){.twikiLink}\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
