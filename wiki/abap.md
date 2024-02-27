# ABAP Language

## ABAP Statements

### NEW
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_new.htm)

Create a instance of a class, like the old CREATE OBJECT.

```ABAP
DATA(object) = NEW zcl_class_name( ).
```

### VALUE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_value.htm)

Create a structure or table with the given type or from context.

``` ABAP
" Create from type
strings = VALUE string_table( ( `A` ) ( `B` ) ( `C` ) ).

" Create from context
DATA strings TYPE string_table.

strings = VALUE #( ( `A` ) ( `B` ) ( `C` ) ).
```

### REF
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_ref.htm)

Creates a reference of a variable.

```ABAP
strings = VALUE string_table( ( `A` ) ( `B` ) ( `C` ) ).

DATA(ref) = REF #( strings ).
```

### EXACT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_exact.htm)

A constructor expression with the lossless operator EXACT performs either a lossless assignment or a lossless calculation, depending on the specified argument `dobj`, and creates a result with the data type type.

### CONV
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_conv.htm)

A constructor expression with the conversion operator CONV converts the argument `dobj` to the data type specified using `type` and creates an appropriate result.

### CAST
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_cast.htm)

A constructor expression with the casting operator CAST performs a downcast or an upcast for the argument `dobj` and creates a reference variable of the static type `type` as a result.

### COND
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconditional_expression_cond.htm)

A conditional expression with the conditional operator COND has a result `result` that is dependent on logical expressions.

### SWITCH
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconditional_expression_switch.htm)

A conditional expression with the conditional operator SWITCH has a result, `result`, that is dependent on a case distinction.

### itab[]
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abentable_expressions.htm)

A table expression consists of an internal table `itab` directly followed by a line specification itab_line in square brackets [ ].

### LINE_INDEX
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenline_index_function.htm)

The table function `line_index` can be used to identify a line number in an index of an internal table and use it in operand positions.

### LINE_EXISTS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenline_exists_function.htm)

The predicate function `line_exists` can be used to check the existence of table lines; the resulting truth value can then be used directly.

### EMPTY KEY
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abaptypes_primary_key.htm)

The new addition `EMPTY KEY` of the statements TYPES, DATA, and so on can be used to define an empty table key explicitly for standard tables.

### WAIT FOR MESSAGING CHANNELS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapwait_amc.htm)

The new variant `WAIT FOR MESSAGING CHANNELS` waits for AMC messages in ABAP Messaging Channels (AMC).

### LET
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abaplet.htm)

The new LET expressions in the form LET ... IN make it possible to define variables or field symbols as helper fields in expressions.

### CORRESPONDING
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expr_corresponding.htm)

The component operator `CORRESPONDING` is a new constructor operator that enables component by component assignments to be made between structures or between internal operands at operand positions.

### WAIT FOR PUSH CHANNELS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapwait_apc.htm)

The new variant WAIT FOR PUSH CHANNELS waits for APC messages in ABAP Push Channels (APC).

### XSDBOOL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenboole_functions.htm)

The new Boolean function `xsdbool` returns the value X or a blank of the type c with the length 1, depending on the truth value of the logical expression specified as the argument.

### FILTER
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_filter.htm)

The new filter operator `FILTER` can be used to perform table filtering in which conditions are used to select or remove lines from an internal table.

### FOR GROUPS OF
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenfor_groups_of.htm)

The new variant `FOR GROUPS ... OF` in an iteration expression for table iterations using FOR can be used to group the lines of internal tables and to evaluate the groups.

### FOR IN GROUP
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenfor_in_group.htm)

The new variant `FOR ... IN GROUP` in an iteration expression for table iterations using FOR can be used to group the lines of internal tables and to evaluate the groups.

### DEFAULT (method definitions)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapmethods_default.htm)

The new addition `DEFAULT` of the statements METHODS and CLASS-METHODS can be used to make general methods, functional methods, plus event handlers of interfaces optional.

### VALUE #( ... DEFAULT/OPTIONAL)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abentable_exp_optional_default.htm)

If the type of the result of a table expression or a chaining of table expressions is controlled using the constructor operators VALUE or REF, the additions OPTIONAL and DEFAULT can be used to specify a default value. If no lines are found, no exception is raised and the default value is returned instead.

### IS INSTANCE OF
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenlogexp_instance_of.htm)

The new predicate expression `IS INSTANCE OF` can be used to detect the dynamic type of an object reference variable. This makes it possible to check the feasibility of a downcast before it is executed.

### CASE TYPE OF
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapcase_type.htm)

The special statement `CASE TYPE OF` makes it possible to check the dynamic type of an object reference variable as a case distinction.

### RAISE EXCEPTION ... MESSAGE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapraise_exception_message.htm)

The new addition `MESSAGE` of the statement RAISE EXCEPTION and of the addition THROW in a conditional expression associates any message with an exception object.

### ENUM
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenenumerated_types_usage.htm)

The statement TYPES BEGIN OF ENUM can be used to define enumerated types for enumerated variables, which can have only enumerated values defined for this type.

### RAISE SHORTDUMP
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapraise_shortdump.htm)

The new statement RAISE SHORTDUMP raises runtime errors associated with an exception object. This means more information can now be passed to the short dump than was previously possible in an exit message.

### Calculation operations
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencalculation_assignments.htm)

A calculation takes place when the assignment is made. These new operators make the statements ADD, SUBTRACT, MULTIPLY, and DIVIDE obsolete.

### String concatenation
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencalculation_assignment_string.htm)

This assignment has the same effect as the following assignment of a string expression:
- lhs = lhs && rhs.

### APPENDING BASE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencorresponding_constr_arg_type.htm)

It is now possible to specify statements with the component operator `CORRESPONDING` with the following additions in the context of nested tables in deep structures.

### DEEP APPENDING BASE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencorresponding_constr_arg_type.htm)

It is now possible to specify statements with the component operator `CORRESPONDING` with the following additions in the context of nested tables in deep structures.

### FINAL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenfinal_inline.htm)

The new declaration operator FINAL declares an immutable variable that cannot be assigned another value at other write positions of the same context.

### struc-(comp)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapassign_dynamic_components.htm)

Components of structures can be assigned to field symbols with the new syntax `struc-(comp)` that largely replaces the variant ASSIGN COMPONENT OF.

### ELSE UNASSIGN
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapassign_else_unassign.htm)

The new addition ELSE UNASSIGN can be specified for the following variants of the statement ASSIGN.

### STEP
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abaploop_at_itab_cond.htm#!ABAP_ADDITION_3@3@)

The new addition STEP defines the step size and the order for processing an internal table. For the statements LOOP and FOR, STEP can be used to control the step size and the processing order. For the statements APPEND, DELETE, INSERT, VALUE, and NEW, STEP can only be used to define the step size. It is not possible to change the processing order with STEP for these statements.

### RETURN value
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapreturn.htm)

In functional methods, the statement RETURN can be used to assign the result of an expression expr to the return value when terminating the method.

### CORRESPONDING (DEFAULT)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencorresponding_constr_mapping.htm#!ABAP_ADDITION_2@2@)

The addition DEFAULT allows the assignment of values for a target component based on an expression.

## ABAP SQL

## ABAP Unit

## ABAP Concepts

### Inline Declaration
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abeninline_declarations.htm)

The new declaration operators DATA and FIELD-SYMBOL make inline declarations possible in declaration expressions in declaration positions.

```ABAP
" Create from value
DATA(integer) = 6.

" With method
DATA(result) = call_a_method_with_result( ).

" In Loop-Statement
LOOP AT datas ASSIGNGING FIELD-SYMBOL(<data>).
ENDLOOP.
```

### ABAP Messaging Channels
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenamc.htm)

From ABAP release 7.40, SP02, `ABAP Messaging Channels (AMC)` enable a new type of communication between AS ABAP programs, which goes beyond the limits of an AS instance.

### ABAP Docs
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abendoccomment.htm)

Special ABAP Doc comments can be entered in front of declaration statements. These comments are prefixed by `"!`. Tools of an ABAP development environment that support ABAP Doc, such as ABAP development tools for Eclipse, analyze the content of ABAP Doc comments, converts it to HTML and display the content in an appropriate way.

### Meshes (Types & Processing)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_meshes.htm)

The meshes are special structures whose components are internal tables, which can be linked to each other using mesh associations. Mesh associations are evaluated by specifying mesh paths in suitable expressions and statements.

### ABAP Push Channels
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenapc.htm)

`ABAP Push Channels (APC)` enable bidirectional communication between AS ABAP and the internet using the WebSocket protocol.

### Predicative Method Calls
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenpredicative_method_calls.htm)

A predicative method call is a relational expression whose only operand is a functional method call `meth( ... )`.

### ABAP for Key Users
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_for_key_users_glosry.htm)

In ABAP release 7.50, a new ABAP version for ABAP for Key Users was introduced. This version is designed for enhancements in delivered enhancement points made by Key Users. The internal version ID in the column UCCHECK of the system table TRDIR is 2.

### ABAP Doc short texts
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abendoccomment.htm#@@ITOC@@ABENDOCCOMMENT_4)

It is now possible to define short texts in ABAP comments and synchronize them with the short texts of methods and function modules in ABAP Workbench.

### ABAP Daemons
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_daemon.htm)

An ABAP Daemon is an instance of an ABAP Daemon class in an ABAP Daemon session. An ABAP Daemon is created again automatically every time a runtime error or a message of type E, A, or X causes a program termination.

### ABAP Doc links
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abendoccomment.htm#@@ITOC@@ABENDOCCOMMENT_5)

The new syntax `{@link ...}` makes it possible to link to other documentation of repository objects (or its components) in ABAP Doc comments.

### HANA only
[SAP Help](https://help.sap.com/docs/SAP_HANA_PLATFORM/fc5ace7a367c434190a8047881f92ed8/d8d14ef53e244f6cabd10dd3f5e8c11e.html?locale=en-US)

As of this release, only an SAP HANA database is supported as the standard database of an AS ABAP. For this reason, Open SQL was renamed to ABAP SQL (see ABAP SQL in ABAP Release 7.53). Note: Using a secondary connection in ABAP SQL, it is still possible to connect to other databases.

### Open SQL to ABAP SQL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_sql.htm)

The existing name Open SQL has been changed to ABAP SQL. This renaming reflects that some parts of ABAP SQL now only support certain database platforms, specifically SAP HANA database, and hence that it is no longer fully platform-independent.

### ABAP for Cloud Development
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_versions_and_apis.htm#@@ITOC@@ABENABAP_VERSIONS_AND_APIS_1)

In ABAP release 7.53, a new ABAP version ABAP for Cloud Development was introduced. The internal version ID in the column UCCHECK of the system table TRDIR is 5.

### PCRE regular expressions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenregex_pcre_syntax.htm)

Besides the existing support of POSIX regular expressions, ABAP supports now also PCRE regular expressions that are processed by the PCRE2 Library implemented in the ABAP Kernel. PCRE regular expressions can be used in the same way as POSIX regular expressions.

### Component Selector
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenobject_component_selector.htm)

The following syntax can be used for the object component selector -> to access components and attributes dynamically now:

```ABAP
... { dref->(comp_name) }
  | { cref->(attr_name) }
  | { iref->(attr_name) } ...
```

### XPath Regular Expressions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenregex_xpath_syntax.htm)

Besides the existing support of PCRE regular expressions and POSIX regular expressions (obsolete) ABAP supports now also XPath regular expressions and XSD regular expressions. Internally, those are transformed to PCRE regular expressions and processed by the PCRE2 Library.

### XSD Regular Expressions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenregex_xsd_syntax.htm)

Besides the existing support of PCRE regular expressions and POSIX regular expressions (obsolete) ABAP supports now also XPath regular expressions and XSD regular expressions. Internally, those are transformed to PCRE regular expressions and processed by the PCRE2 Library.

### Alias Names for Secondary Keys
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenitab_key_secondary.htm)

Alias names can now be declared for secondary keys of internal tables by using the addition ALIAS of TYPES and DATA. This can be helpful when changing existing secondary keys without invalidating users.

### SELF
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenrfc_destination.htm#@@ITOC@@ABENRFC_DESTINATION_3)

The new predefined RFC destination SELF works as NONE but uses the RFC protocol fast serialization.

### Software Components (ABAP Cloud)
Software components can be created for different language versions in order to define pure TIER-1 packages in which development can be carried out according to the rules of “ABAP for Cloud”.


### T1 Fiori Deployment (ABAP Cloud)
It is currently only possible to deploy a Fiori application in a TIER-1 package from S/4 HANA 2023 FPS1.

