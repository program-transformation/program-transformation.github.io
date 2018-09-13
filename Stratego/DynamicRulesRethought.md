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
    Page](http://www.program-transformation.org/edit/Stratego/DynamicRulesRethought?t=1536825576)
-   [Rename
    Page](http://www.program-transformation.org/rename/Stratego/DynamicRulesRethought)
-   [Attach
    File](http://www.program-transformation.org/attach/Stratego/DynamicRulesRethought)

<!-- -->

-   [Printable](http://www.program-transformation.org/view/Stratego/DynamicRulesRethought?skin=print.pattern)
-   [Wiki
    Source](http://www.program-transformation.org/view/Stratego/DynamicRulesRethought?skin=text&raw=on&contenttype=text/plain)

<!-- -->

-   [Rev
    7](http://www.program-transformation.org/view/Stratego/DynamicRulesRethought?rev=1.7)
    [(diff 6)](http://www.program-transformation.org/rdiff/Stratego/DynamicRulesRethought?rev1=1.7&rev2=1.6)
-   [Rev
    6](http://www.program-transformation.org/view/Stratego/DynamicRulesRethought?rev=1.6)
    [(diff 5)](http://www.program-transformation.org/rdiff/Stratego/DynamicRulesRethought?rev1=1.6&rev2=1.5)
-   [Rev
    5](http://www.program-transformation.org/view/Stratego/DynamicRulesRethought?rev=1.5)
    [(diff 4)](http://www.program-transformation.org/rdiff/Stratego/DynamicRulesRethought?rev1=1.5&rev2=1.4)
-   [Total
    History](http://www.program-transformation.org/rdiff/Stratego/DynamicRulesRethought)

<!-- -->

-   [More
    \...](http://www.program-transformation.org/oops/Stratego/DynamicRulesRethought?template=oopsmore&param1=1.7&param2=1.7)
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
    \...](http://www.program-transformation.org/oops/Stratego/DynamicRulesRethought?template=oopsmore&param1=1.7&param2=1.7)
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
Dynamic Rules Rethought {#dynamic-rules-rethought .twikiTopicTitle}
=======================

::: {.twikiWebTitle}
Stratego \-- Strategies for Program Transformation
:::

We\'re currently rethinking the concept of dynamic rules; quite some
changes are at stake. This topic collects some of our reasoning on
behaviour and implementation of dynamic rules.

::: {.twikiToc}
-   [Dynamic scoping for dynamic
    rules](DynamicRulesRethought#Dynamic_scoping_for_dynamic_rule)
    -   [New ideas for
        scoping](DynamicRulesRethought#New_ideas_for_scoping)
    -   [New syntax for dynamic
        rules](DynamicRulesRethought#New_syntax_for_dynamic_rules)
        -   [Generalized rules
            blocks](DynamicRulesRethought#Generalized_rules_blocks)
        -   [Scope labeling](DynamicRulesRethought#Scope_labeling)
        -   [Rule generation](DynamicRulesRethought#Rule_generation)
        -   [Rewriting
            behaviour](DynamicRulesRethought#Rewriting_behaviour)
    -   [More efficient scope-handling using multiple
        hash-tables](DynamicRulesRethought#More_efficient_scope_handling_us)
-   [Maintaining Scopes stack as a list of
    changesets](DynamicRulesRethought#Maintaining_Scopes_stack_as_a_li)
    -   [Purpose](DynamicRulesRethought#Purpose)
    -   [Ideas](DynamicRulesRethought#Ideas)
-   [Open Issues](DynamicRulesRethought#Open_Issues)
    -   [bagof fails if LHS is unknown
        (fixed)](DynamicRulesRethought#bagof_fails_if_LHS_is_unknown_fi)
    -   [bagof behaves incorrect for overlapping
        LHS](DynamicRulesRethought#bagof_behaves_incorrect_for_over)
:::

[]{#Dynamic_scoping_for_dynamic_rule} Dynamic scoping for dynamic rules
-----------------------------------------------------------------------

### []{#New_ideas_for_scoping} New ideas for scoping

-   A scope has a scope-name, which is some sort of meta-identifier for
    one or more scopes. For dynamic rules this is the name of the rule.
-   Secondly, a scope also has a label, to identify it from other
    (parent-) scopes with the same name. Update: This is now available
    in the new dynamic rules.
-   Items within a scope should bind themselves to a named scope, and
    optionally specify a label to define which scope the item is placed
    in. If unspecified, the most recent (inner) scope shall
    automatically be taken. Update: This is now available in the new
    dynamic rules.
-   The idea is that a scope-label should be defined and used at runtime
    (i.e. is a `Term`). This allows for context-based scoping. Update:
    This is now available in the new dynamic rules.
-   Note that the combination of scope-name and scope-label is not
    unique. For example consider this fragment:

<!-- -->

        let x := 3
         in let y := 5
             in let x := 4
                 in x + y
                end
             end
             + x
        end
        // (result is (4+5)+3)

-   If the runtime-determined label for some dynamic rule is taken to be
    the `Identifier` of the `Decl` of a `Let`, then, during
    transformation of the above fragment, we will have at \'x+y\' the
    following scope-list:
    `[("MyRule", "x"), ("MyRule", "y"), ("MyRule", "x")]`\
    (Just FYI, this non-uniqueness is no problem at all)

### []{#New_syntax_for_dynamic_rules} New syntax for dynamic rules

#### []{#Generalized_rules_blocks} Generalized rules blocks

Generation of dynamic rules used to occur in `rules(..)` and
`override rules(..)` (and later
`extend rules(..)=/=extend override rules(..)` as well). This has now
been generalized to a new `rules(..)` block. Each rule now itself
defines whether it extends the existing ruleset, overwrites rules in any
higher scope, or just generates a new rule instance in the current
scope.

#### []{#Scope_labeling} Scope labeling

Dynamic rules scopes are always specific for one rulename (Id). A new
feature is optional labeling of these dynamic rules scopes with
(runtime) terms. Scopes may be assigned multiple labels. *(For
experienced dynamic-rules-users: This is a generalisation of the
scope-association in an `override rules(..)` block. Generation of new
rules can be aimed at specifically labeled scopes (see next section).)*

Assigning labels to a scope can be done at the scope definition:

        {| RuleName1.lblA, ..., RuleNameN.lblN :
          s
        |}

It is also possible to assign labels to the current scope we\'re in,
this can be done within a `rules(..)` block:

          rules(
            RuleA + lbl
            ...
          )

#### []{#Rule_generation} Rule generation

The `extend rules(..)` construct has been removed, instead dynamic rule
definitions can state their own semantics:

          rules(
            // Generate new rule in current scope that destroys all existing rules with the same dummified LHS
            Rule(as1|as2) : t1 -> t2 where s

            // Generate new rule in current scope that extends the existing ruleset
            Rule(as1|as2) :+ t1 -> t2 where s

            // Undefine all rules in current scope with same dummified LHS
            Rule(as1|as2) :- t1
          )

All dynamic rule definitions can also be aimed at scopes with a certain
label:

          rules(
            // Generate new rule in scope for 'Rule' with label `t'
            Rule(as1|as2).t : t1 -> t2 where s

            // Generate new rule in current scope and label the current scope with `t'
            Rule(as1|as2)+t : t1 -> t2 where s

            // (Mentioned before) Just assign a label to the current scope
            Rule + t
          )

Note that scope-labeling and association of (closures/bindings of)
generated dynamic rules to scopes, is only based upon the rulename, not
upon its arity. E.g.: `RuleA` and `RuleA(s|t)` share the same stack of
bindings.

#### []{#Rewriting_behaviour} Rewriting behaviour

When calling a generated dynamic rule, the most recent scope is
determined in which a rule instance was generated. If multiple rule
instances have been generated within that scope, rewriting is tried
until the first one that succeeds. If none of the rule instances can
rewrite succesfully, the call fails.

### []{#More_efficient_scope_handling_us} More efficient scope-handling using multiple hash-tables

-   Put each new scope in its own hashtable.
-   Maintain a list of nested scopes.
    -   One list for each scope name (i.e rulename)
    -   Each list-element is a small tuple containing the label of the
        scope and a pointer to the hashtable for that specific scope.

<!-- -->

-   Lookup of scoped items (i.e. rule-bindings) just comes down to take
    the table-list for the desired scope-name, and just perform a lookup
    in the tables \-- starting with the frontmost table (i.e. innermost
    scope) \-- until the item with the requested key is found.
-   Multiple values for same key within one scope. Should still be
    possible (`extend rules`!), so for each key we keep one (key, value)
    pair in the scope table, but the value is itself a stack (-like
    list).
-   As Martin suggested: get rid of the table-table. Instead of a static
    `ATermTable SSL_table_table` in tables.c, let the compiler generate
    a hashtable variable where needed.
    -   In the case of dynamic rules: one compile-time hashtable becomes
        available. This table contains for each rulename (which serves
        as the key) a list of scope-tables.
    -   Another option: for each rulename generate a separate (list-)
        variable.

[]{#Maintaining_Scopes_stack_as_a_li} Maintaining Scopes stack as a list of changesets
--------------------------------------------------------------------------------------

### []{#Purpose} Purpose

-   Easier intersection of scoped rulesets.
-   Cheaper forking (e.g. during dataflow analysis) of traversals that
    involve generation and intersection of dynamic rulesets.

### []{#Ideas} Ideas

-   A scope specification with items (here: context-bindings) in it,
    could be represented as a change set on top of any previous scope
    specifications (which are change sets themselves).
-   A changeset is not specific for one scope at all! It can cover all
    previous scopes and may introduce new ones.
-   Forking during dataflow analysis becomes easy now: start two new
    changesets with the same parent set.\
    **Note:** Lookup will also use the parent sets, but changing/adding
    only happens in the current change set of course.
-   Maintaining change sets is probably useful during subtraversals.
    After the required info has been computed (e.g. intersected
    ruleset), the resulting change set may be \'committed\' to toplevel
    rulesets (to avoid unnecessary chained lookup)

[]{#Open_Issues} Open Issues
----------------------------

-   If within a certain scope, rewriting with a dynrule fails, do we
    want to try higher scopes as well? (inheritance) I know this is
    contradictory to the current semantics: generating a new rule
    \'hides\' all previous rules for the same LHS. Still, it\'s
    something we should consider.\
    Update: The best is to lookup the most recent scope in which a rule
    was generated and then stick to that scope.
-   If we do so: a special rule should be available that **does**
    undefine/ hide previously generated rules.\
    An extra flexibility would be to specify: undefine in current scope,
    or undefine in all scopes up into the first scope that it was
    introduced in.\
    Update : undefining in higher scopes automatically happens when
    generating rules in the current scope.

### []{#bagof_fails_if_LHS_is_unknown_fi} bagof fails if LHS is unknown (fixed)

-   bagof fails if LHS is unknown, it succeeds with empty list if LHS is
    known but all rewritings failed.
-   Easily fixable by catching failure upon binding-lookup and returning
    empty list. (Or the other way around: fail if filter produces empty
    list, but this seems less intuitive for a *bagof*)

### []{#bagof_behaves_incorrect_for_over} bagof behaves incorrect for overlapping LHS

-   Consider the following fragment:

<!-- -->

        overlap-test =
        {| RuleA :
          extend rules(RuleA: Foo(x, y) -> Bar(y, x) where <gt> (x, y))
        ; extend rules(RuleA: Foo(x, y) -> Bar(x, y) where <leq> (x, y))
        ; !7 => b
        ; extend rules(RuleA: Foo(x, b) -> Seven(b, x))
        
        // Below is what currently happens
        ; <bagof-RuleA> Foo(3, 7) => [Bar(3,7)]
        
        // Below is what one would expect
        ; <bagof-RuleA> Foo(3, 7) => [Bar(3,7), Seven(7,3)] // (list order may differ)
        |}

-   Cause of the above: For **each** extend rules, a new bagof-RuleA is
    generated, later wrapped in one list of choices, see the following
    (somewhat edited) lifted code:

<!-- -->

        bagof-RuleA( | ) =
          ( ?h_13@Foo(f_13, g_13)
            ; where(!Foo([], []); extend-rewrite(!"RuleA" |)
                    ; filter({e_88 : where(id; ?e_88); !(h_13, e_88)}
                             ; aux-RuleA(|) |)
                    ; ?i_13)
            ; !i_13
           + ( ?y_12@Foo(w_12, x_12)
               ; where(!Foo([], []); extend-rewrite(!"RuleA" |)
                       ; filter({k_85 : where(id; ?k_85); !(y_12, k_85)}
                                ; aux-RuleA(|) |)
                       ; ?z_12)
               ; !z_12
               ; id
              + ( ?p_12@Foo(n_12, o_12)
                  ; where(!Foo([], o_12); extend-rewrite(!"RuleA" |)
                          ; filter({u_82 : where(id; ?u_82); !(p_12, u_82)}
                                   ; aux-RuleA(|) |)
                          ; ?q_12)
                  ; !q_12
                 + fail)))

-   The LHS of the first two rules overlap the LHS of the third, so the
    initial match (e.g. `?h_13@Foo(f_13,g_13)`) succeeds, the rest of
    the second rule also succeeds, so its result is returned, and the
    third strategy in the choiced-list (`?p12@...`) is not tried at
    all.\
    Besides : the first two `extend rules` are indexed with key
    `Foo([],[])`, the third with `Foo([],7)`. So, the bindings for the
    third are not returned by the call
    `!Foo([], []); extend-rewrite(!"RuleA" |)`\
    So, although normally the third rule would succeed (and may even be
    the preferred one), it\'s never seen as a result.
-   Fix for this problem: In the binding table, maintain an additional
    list with all `(LHS, binding)` tuples for the rule, for example
    like:

<!-- -->

        ( "__drbindings__",
          [ (Foo([], 7), Defined("z_3")),
            (Foo([],[]), Defined("c_2")),
            (Foo([],[]), Defined("d_0"))
          ]
        )

-   the `full-bagof-RuleA` is a quick-n-dirty approach to get the
    desired bagof-behaviour:

<!-- -->

        full-bagof-RuleA :
          t_1 ->
          s_1
          where get-scoped-values-current(|"RuleA", "__drbindings__")
                ; filter({ key, bnds :
                           ?(key, bnds)
                         ; <matchHelper(|key)> t_1 // determines whether current term would match the dummified LHS
                         ; !(t_1, bnds)
                         ; aux-RuleA(|)
                         })
                ; ?s_1

        matchHelper(|key) =
          ?t_1@Foo(x, b)
        ; where(!key => Foo([], b))
        ; where(!t_1 => Foo(_, b))

        matchHelper(|key) =
          ?v_1@Foo(x, y)
        ; where(!key => Foo([], []))
        ; where(!v_1 => Foo(_, _))

-   Also note that although the first two extend rules have the same
    LHS, still a separate bagof-RuleA is generated for them. Not
    incorrect, but redundant.

\-- [ArthurVanDam](../Main/ArthurVanDam){.twikiLink} - 29 Mar 2004\
[]{#TopicEnd}
:::

::: {.twikiTopicInfo .twikiRevInfo .twikiGrayText .twikiMoved}
:::
:::
:::
:::
