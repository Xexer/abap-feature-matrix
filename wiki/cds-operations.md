# CDS Operations

## JOIN (Inner, Left, Right)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_joined_data_source_v2.htm)

Defines a join between two data sources of a CDS view entity. The code above is part of the syntax of a data source data_source and recursively contains the syntax of a second data source data_source.

## WHERE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_where_clause_v2.htm)

Defines a `WHERE` condition for the result set of a CDS view entity. When the CDS view entity is accessed, the result set contains only the data from the data source data_source that meets the condition cds_cond specified after WHERE.

## GROUP BY
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_group_by_v2.htm)

Groups those rows in the result set of a CDS view entity that have the same content in the elements specified by the fields field1, field2, ... or path expressions path_expr1, path_expr2 ... as a single row. The fields must be specified using the same names as the fields in the data source data_source.

## HAVING
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_having_clause_v2.htm)

Defines a `HAVING` condition for the result set of a CDS view entity after a GROUP BY clause is evaluated. A HAVING condition can only be specified together with GROUP BY.

## UNION
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_union_v2.htm)

Merges the rows of the result sets of multiple SELECT statements of CDS view entities into one result set. As a prerequisite, the result sets must have the same number of elements and the element pairs that occur in the same position of the result set must have a compatible data type.

## Cross Join
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_joined_data_source_v1.htm)

As well as an inner and outer join, it is now possible to use a `cross join` in a SELECT statement.

## LOAD BULK|INCREMENTAL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_f1_define_hierarchy.htm#!ABAP_ADDITION_9@9@)

The hierarchy generator DEFINE HIERARCHY can now use the new addition `LOAD BULK|INCREMENTAL|load_option` to specify the load policy for a generated hierarchy.

## EXCEPT (View Entity)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_except_v2.htm)

The set operator `EXCEPT` returns all rows of a SELECT statement of a CDS view entity that are not part of the result sets of the following SELECT statements. As a prerequisite, the result sets must have the same number of elements and the element pairs that occur in the same position of the result set must have a compatible data type.

## INTERSECT (View Entity)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_intersect_v2.htm)

The set operator `INTERSECT` returns all distinct rows that are included in all result sets of multiple SELECT statements of CDS view entities. As a prerequisite, the result sets must have the same number of elements and the element pairs that occur in the same position of the result set must have a compatible data type.

## UNION (View Entity)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_union_v2.htm)

`UNION` clauses are now supported in CDS view entities. There are a few differences to UNION clauses in CDS DDIC-based views. The most important difference is that branches of union clauses can be nested within each other in CDS view entities.

## DISTINCT (View Entity)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_select_statement_v2.htm)

The addition DISTINCT is now available for SELECT statements in CDS view entities. `DISTINCT` removes duplicates from the result set. If DISTINCT is specified, the elements cannot have the type LCHR, LRAW, STRING, RAWSTRING, or GEOM_EWKB