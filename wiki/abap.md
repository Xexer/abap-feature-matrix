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

### CONV

### CAST

### COND

### SWITCH


## ABAP SQL

## ABAP Unit

## ABAP Concepts

### Inline Declaration
Create variables within statements, without a DATA and datatype at the beginning of a method or form.

```ABAP
" Create from value
DATA(integer) = 6.

" With method
DATA(result) = call_a_method_with_result( ).

" In Loop-Statement
LOOP AT datas ASSIGNGING FIELD-SYMBOL(<data>).
ENDLOOP.
```