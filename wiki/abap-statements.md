# ABAP Statements

## NEW
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_new.htm)

Create a instance of a class, like the old CREATE OBJECT.

```ABAP
DATA(object) = NEW zcl_class_name( ).
```

## VALUE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_value.htm)

Create a structure or table with the given type or from context.

``` ABAP
" Create from type
strings = VALUE string_table( ( `A` ) ( `B` ) ( `C` ) ).

" Create from context
DATA strings TYPE string_table.

strings = VALUE #( ( `A` ) ( `B` ) ( `C` ) ).
```

## REF
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_ref.htm)

Creates a reference of a variable.

```ABAP
strings = VALUE string_table( ( `A` ) ( `B` ) ( `C` ) ).

DATA(ref) = REF #( strings ).
```

## EXACT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_exact.htm)

A constructor expression with the lossless operator EXACT performs either a lossless assignment or a lossless calculation, depending on the specified argument `dobj`, and creates a result with the data type type.

## CONV
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_conv.htm)

A constructor expression with the conversion operator CONV converts the argument `dobj` to the data type specified using `type` and creates an appropriate result.

## CAST
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_cast.htm)

A constructor expression with the casting operator CAST performs a downcast or an upcast for the argument `dobj` and creates a reference variable of the static type `type` as a result.

## COND
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconditional_expression_cond.htm)

A conditional expression with the conditional operator COND has a result `result` that is dependent on logical expressions.

## SWITCH
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconditional_expression_switch.htm)

A conditional expression with the conditional operator SWITCH has a result, `result`, that is dependent on a case distinction.

## itab[]
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abentable_expressions.htm)

A table expression consists of an internal table `itab` directly followed by a line specification itab_line in square brackets [ ].

## LINE_INDEX
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenline_index_function.htm)

The table function `line_index` can be used to identify a line number in an index of an internal table and use it in operand positions.

## LINE_EXISTS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenline_exists_function.htm)

The predicate function `line_exists` can be used to check the existence of table lines; the resulting truth value can then be used directly.

## EMPTY KEY
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abaptypes_primary_key.htm)

The new addition `EMPTY KEY` of the statements TYPES, DATA, and so on can be used to define an empty table key explicitly for standard tables.

## WAIT FOR MESSAGING CHANNELS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapwait_amc.htm)

The new variant `WAIT FOR MESSAGING CHANNELS` waits for AMC messages in ABAP Messaging Channels (AMC).

## LET
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abaplet.htm)

The new LET expressions in the form LET ... IN make it possible to define variables or field symbols as helper fields in expressions.

## CORRESPONDING
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expr_corresponding.htm)

The component operator `CORRESPONDING` is a new constructor operator that enables component by component assignments to be made between structures or between internal operands at operand positions.

## WAIT FOR PUSH CHANNELS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapwait_apc.htm)

The new variant WAIT FOR PUSH CHANNELS waits for APC messages in ABAP Push Channels (APC).

## XSDBOOL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenboole_functions.htm)

The new Boolean function `xsdbool` returns the value X or a blank of the type c with the length 1, depending on the truth value of the logical expression specified as the argument.

## REDUCE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_reduce.htm)

A constructor expression with the reduction operator `REDUCE` creates a result of a data type specified using type from one or more iteration expressions.

## FILTER
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenconstructor_expression_filter.htm)

The new filter operator `FILTER` can be used to perform table filtering in which conditions are used to select or remove lines from an internal table.

## FOR GROUPS OF
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenfor_groups_of.htm)

The new variant `FOR GROUPS ... OF` in an iteration expression for table iterations using FOR can be used to group the lines of internal tables and to evaluate the groups.

## FOR IN GROUP
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenfor_in_group.htm)

The new variant `FOR ... IN GROUP` in an iteration expression for table iterations using FOR can be used to group the lines of internal tables and to evaluate the groups.

## DEFAULT (method definitions)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapmethods_default.htm)

The new addition `DEFAULT` of the statements METHODS and CLASS-METHODS can be used to make general methods, functional methods, plus event handlers of interfaces optional.

## VALUE #( ... DEFAULT/OPTIONAL)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abentable_exp_optional_default.htm)

If the type of the result of a table expression or a chaining of table expressions is controlled using the constructor operators VALUE or REF, the additions OPTIONAL and DEFAULT can be used to specify a default value. If no lines are found, no exception is raised and the default value is returned instead.

## IS INSTANCE OF
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenlogexp_instance_of.htm)

The new predicate expression `IS INSTANCE OF` can be used to detect the dynamic type of an object reference variable. This makes it possible to check the feasibility of a downcast before it is executed.

## CASE TYPE OF
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapcase_type.htm)

The special statement `CASE TYPE OF` makes it possible to check the dynamic type of an object reference variable as a case distinction.

## RAISE EXCEPTION ... MESSAGE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapraise_exception_message.htm)

The new addition `MESSAGE` of the statement RAISE EXCEPTION and of the addition THROW in a conditional expression associates any message with an exception object.

## ENUM
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenenumerated_types_usage.htm)

The statement TYPES BEGIN OF ENUM can be used to define enumerated types for enumerated variables, which can have only enumerated values defined for this type.

## RAISE SHORTDUMP
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapraise_shortdump.htm)

The new statement RAISE SHORTDUMP raises runtime errors associated with an exception object. This means more information can now be passed to the short dump than was previously possible in an exit message.

## Calculation operations
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencalculation_assignments.htm)

A calculation takes place when the assignment is made. These new operators make the statements ADD, SUBTRACT, MULTIPLY, and DIVIDE obsolete.

## String concatenation
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencalculation_assignment_string.htm)

This assignment has the same effect as the following assignment of a string expression:
- lhs = lhs && rhs.

## APPENDING BASE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencorresponding_constr_arg_type.htm)

It is now possible to specify statements with the component operator `CORRESPONDING` with the following additions in the context of nested tables in deep structures.

## DEEP APPENDING BASE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencorresponding_constr_arg_type.htm)

It is now possible to specify statements with the component operator `CORRESPONDING` with the following additions in the context of nested tables in deep structures.

## FINAL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenfinal_inline.htm)

The new declaration operator FINAL declares an immutable variable that cannot be assigned another value at other write positions of the same context.

## struc-(comp)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapassign_dynamic_components.htm)

Components of structures can be assigned to field symbols with the new syntax `struc-(comp)` that largely replaces the variant ASSIGN COMPONENT OF.

## ELSE UNASSIGN
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapassign_else_unassign.htm)

The new addition ELSE UNASSIGN can be specified for the following variants of the statement ASSIGN.

## STEP
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abaploop_at_itab_cond.htm#!ABAP_ADDITION_3@3@)

The new addition STEP defines the step size and the order for processing an internal table. For the statements LOOP and FOR, STEP can be used to control the step size and the processing order. For the statements APPEND, DELETE, INSERT, VALUE, and NEW, STEP can only be used to define the step size. It is not possible to change the processing order with STEP for these statements.

## RETURN value
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapreturn.htm)

In functional methods, the statement RETURN can be used to assign the result of an expression expr to the return value when terminating the method.

## CORRESPONDING (DEFAULT)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencorresponding_constr_mapping.htm#!ABAP_ADDITION_2@2@)

The addition DEFAULT allows the assignment of values for a target component based on an expression.