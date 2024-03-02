# ABAP SQL

## Blank-Separated Lists
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_sql_lists_obsolete.htm)

In ABAP SQL, all operands in lists can now be separated by commas and this is also the recommended way of separating them from ABAP release 7.40, SP05. Until now, comma-separated lists could only be used when single target fields were specified in parentheses after INTO in SELECT and when data objects were specified in parentheses after WHERE. This makes blank-separated lists `obsolete`.

## Comma-Separated Lists
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapselect.htm)
In ABAP SQL, all operands in lists can now be separated by commas and this is also the recommended way of separating them from ABAP release 7.40, SP05. Until now, comma-separated lists could only be used when single target fields were specified in parentheses after INTO in SELECT and when data objects were specified in parentheses after WHERE.

## Host Variables (@)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_sql_host_variables.htm)

ABAP data objects used in ABAP SQL statements (usually variables) are now interpreted as host variables, as in statically embedded Native SQL. From ABAP release 7.40, SP05, host variables can and should be prefixed with the escape character `@`. Host variables without the escape character are obsolete. If the escape character is used in front of a name of an ABAP SQL statement, the syntax check is performed in a strict mode, which handles the statement more strictly than the regular syntax check.

## INLINE Declaration
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abeninline_declarations.htm)

After the addition INTO of a SELECT statement, inline declarations can be made from ABAP release 7.40, SP08 using the declaration operator `DATA(...)` with the prefixed escape character @. Inline declarations can be made for individual parenthesized data objects (@DATA(elem1),@DATA(elem2),...), for individual work areas INTO @DATA(wa), and for internal tables INTO TABLE @DATA(itab).

```ABAP 
SELECT * 
  FROM T000 
  INTO TABLE @DATA(clients)
```

## CASE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_searched_case.htm)

The operator `CASE` can now be used to perform complex case distinctions (searched case) as well as simple case distinctions.

## Read CDS with parameters
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapselect_data_source.htm#!ABAP_ALTERNATIVE_2@2@)

From ABAP release 7.40, SP08, CDS views can be defined with input parameters that are assigned actual parameters when used. To enable this, the option of a parenthesized comma-separated list for parameter passing was added to the data source specified in the statement SELECT:

```ABAP
( pname1 = act1, pname1 = act2, ...)
```

## UNION
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapunion_clause.htm)

From ABAP release 7.50, the addition UNION creates the union of the results sets of two SELECT statements.

## @( expr )
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_sql_host_variables.htm)

From ABAP release 7.50, host expressions with the syntax @( expr ) can be specified in many operand positions in which host variables are possible. For expr, all ABAP expressions can calls are possible that can be specified in general expression positions.

## CDS Path Expressions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_sql_path.htm)

From ABAP release 7.50, path expressions can be specified in SELECT statements that access CDS views with associations published for outside use as follows.

## Common Table Expressions (WITH)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapwith.htm)

The new ABAP SQL statement `WITH` enables common table expressions (CTEs) to be defined for use in the WITH statement. A common table expression creates a results set that is used in the queries of the WITH statement as a data source. The main query of the WITH statement has an INTO clause and transfers its results set to ABAP data objects.

## Cross Join
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapselect_join.htm)

As well as an inner and outer join, it is now possible to use a `cross join` in a SELECT statement.

## DIVISION
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_arith_func.htm)

The new numeric function `DIVISION` enables divisions with decimal places.

## LOWER and UPPER
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_string_func.htm)

The new string functions `LOWER` and `UPPER` implement uppercase and lowercase.

## String functions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_string_func.htm)

The new string functions `LEFT`, `CONCAT_WITH_SPACE`, `INSTR`, and `RPAD` perform operations on strings.

## Date functions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_date_func.htm#@@ITOC@@ABENSQL_DATE_FUNC_3)

The new date functions `DATS_IS_VALID`, `DATS_DAYS_BETWEEN`, `DATS_ADD_DAYS` and `DATS_ADD_MONTHS` execute operations with date fields.

## EXTENDED RESULT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapselect_extended_result.htm)

The new addition `EXTENDED RESULT` of an INTO clause can be used to provide an extended result for an object of the class CL_OSQL_EXTENDED_RESULT, which can be queried using methods of the class.

## SELECT FROM @itab
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapselect_itab.htm)

An internal table can be specified as a data source data source of a query. This statement cannot be executed on all database systems, if the data from the internal table needs to be passed to the database.

## Operator LIKE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_sql_expr_logexp.htm)

The following is now possible for conditions in expressions: The operator `LIKE` is now also supported.

## Binary operations
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_type_conv_func.htm)

The new type conversion functions BINTOHEX and HEXTOBIN make it possible to convert byte strings to character strings (and the other way round) in SQL expressions, which is not possible with a CAST expression.

## WITH PRIVILEGED ACCESS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapselect_data_source.htm)

The new addition `WITH PRIVILEGED ACCESS` switches CDS access control off.

## NOT BETWEEN and LIKE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_sql_expr_logexp.htm)

The addition `NOT` can now specified in front of BETWEEN and LIKE in relation expressions for expressions.

## Secondary Connections
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abendb_connections.htm)

On an AS ABAP with a SAP HANA database as its standard database, only those secondary connections should be used from the database table DBCON whose secondary database is also a SAP HANA database. Alongside the CONNECTION addition in ABAP SQL, this also applies to Native SQL (ADBC and EXEC SQL).

## IS INITIAL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenwhere_logexp_initial.htm)

The relational expression `IS [NOT] INITIAL` can now be used in a condition sql_cond to compare operands with their type-dependent initial value. When used, this expression leads to the strict mode from ABAP release 7.53.

## TIMS_IS_VALID
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_time_func.htm#@@ITOC@@ABENSQL_TIME_FUNC_2)

New TIMS functions: `TIMS_IS_VALID`

## Timestamp functions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_timestamp_func.htm#@@ITOC@@ABENSQL_TIMESTAMP_FUNC_3)

New timestamp functions: `TSTMP_IS_VALID`, `TSTMP_CURRENT_UTCTIMESTAMP`, `TSTMP_SECONDS_BETWEEN`, `TSTMP_ADD_SECONDS`


## Date/Time Conversions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_date_time_conversions.htm)

New date/time conversions: `TSTMP_TO_DATS`, `TSTMP_TO_TIMS`, `TSTMP_TO_DST`, `DATS_TIMS_TO_TSTMP`

## ABAP_SYSTEM_TIMEZONE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_timezone_func.htm#!ABAP_VARIANT_1@1@)

The function `ABAP_SYSTEM_TIMEZONE` returns the system time zone of the AS ABAP for the client passed to client. The actual parameter for the optional formal parameter client must have the built-in dictionary type CLNT and contain a valid client ID.

## ABAP_USER_TIMEZONE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_timezone_func.htm#!ABAP_VARIANT_2@2@)

The function `ABAP_USER_TIMEZONE` returns the user time zone of AS ABAP for the user name passed to user and the client passed to client.

## WITH ASSOCIATIONS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapwith_associations.htm)

When CDS views are accessed within a common table expression, the addition `WITH ASSOCIATIONS` of the statement WITH can now be used to publish associations of these views for use in path expressions of the current WITH statement. The addition REDIRECTED TO can also be used to replace the target data source of the published association with a previous CTE or the current CTE.

## INTO ... NEW
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapselect_into_target.htm)

The new addition `NEW` can be used to implicitly create anonymous data objects as target areas. The addition NEW now also makes inline declarations possible when using dynamic tokens and after the statement FETCH.

## INTO ... INDICATORS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapselect_indicators.htm)

The new addition `INDICATORS` can be used to specify a null indicator.

## STRING_AGG
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapselect_aggregate.htm)

The new aggregate function STRING_AGG can be used to chain character-like results of the rows of the results set of a query or of the current group as a string.

## PERIOD FROM TO VALID FROM TO
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenselect_hierarchy_generator.htm#!ABAP_ADDITION_3@3@)

The hierarchy generator HIERARCHY can now use the new addition `PERIOD FROM TO VALID FROM TO` to create temporal hierarchies in which the hierarchy nodes are limited by time intervals.

## HIERARCHY DESCENDANTS AGGREGATE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenselect_hierarchy_agg_navis.htm)

The new hierarchy navigator `HIERARCHY_DESCENDANTS_AGGREGATE` can be used to calculate aggregate functions for descendant nodes.

## LEAD/LAG
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_win_func.htm#!ABAP_VARIANT_6@6@)

ABAP SQL now supports the following new window functions in window expressions: `LEAD`, `LAG`

## UUID
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_uuid.htm)

Calls the `UUID` function as an SQL expression or operand of an expression in ABAP SQL. The function UUID does not have any parameters and creates a new unique UUID of the type RAW with the length 16 for each row read from the result set.

``` ABAP
SELECT carrid, carrname, uuid( ) AS uuid
       FROM scarr
       INTO TABLE @FINAL(result).
```

## ALLOW_PRECISION_LOSS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapselect_allow_precision_loss.htm)

The `ALLOW_PRECISION_LOSS` statement can improve the performance of an aggregate expression agg_exp at the cost of accuracy of the result. This function should only be used on decimal values and when loss of precision is acceptable.

## FIRST_VALUE / LAST_VALUE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensql_win_func.htm#!ABAP_VARIANT_7@7@)

Specifies one of the value functions FIRST_VALUE or LAST_VALUE as a window function. The FIRST_VALUE function returns the first value of a sorted set of values, the LAST_VALUE function returns the last value of a sorted set of values.



## Multiple tables FROM @itab
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapselect_itab.htm)

It is now possible to process multiple internal tables accessed with `FROM @itab` within one ABAP SQL statement with the ABAP SQL engine. Currently, this is restricted to joins of internal tables where no database tables are involved.