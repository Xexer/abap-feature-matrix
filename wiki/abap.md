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

### FOR GROUPS
[SAP Help]()

### DEFAULT (method definitions)
[SAP Help]()

### VALUE #( ... DEFAULT/OPTIONAL)
[SAP Help]()

### IS INSTANCE OF
[SAP Help]()

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

### Predicative Method Calls
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenpredicative_method_calls.htm)

A predicative method call is a relational expression whose only operand is a functional method call `meth( ... )`.