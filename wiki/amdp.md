# ABAP Managed Database Procedures (AMDP)

## CALL DATABASE PROCEDURE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapcall_database_procedure.htm)

The new statement `CALL DATABASE PROCEDURE` enables SQLScript to be called from ABAP programs.

## IF_AMDP_MARKER_HDB
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenamdp_classes.htm)

The new tag interface `IF_AMDP_MARKER_HDB` flags a class as an AMDP class, which can contain AMDP methods for SAP HANA database.

## BY DATABASE PROCEDURE FOR HDB LANGUAGE SQLSCRIPT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapmethod_by_db_proc.htm)

The new addition `BY DATABASE PROCEDURE FOR HDB LANGUAGE SQLSCRIPT` for the statement METHOD turns a method of an AMDP class into an AMDP procedure implementation. This is implemented in the SQLScript language of the SAP HANA database and not in ABAP. The ABAP runtime framework creates a corresponding database procedure in SAP HANA database. This procedure is executed when the AMDP method is called.

## AMDP BAdIs
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenamdp_badis.htm)

From ABAP release 7.40, SP08, special AMDP BAdIs were introduced for AMDP procedure implementations. These apply the effect of the switches from Switch Framework to the implementation of database procedures in the current database. When an AMDP procedure calls an AMDP procedure managed by an AMDP BAdI, the implementation is executed that matches the current switch setting.

## BY DATABASE FUNCTION
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapmethod_by_db_proc.htm)

Alongside the existing AMDP procedures, the AMDP framework now also supports AMDP functions in the form of table functions in the SAP HANA database. AMDP now have the new addition `BY DATABASE FUNCTION` of the statement METHOD in implementations of AMDP methods in AMDP classes. These methods are known as AMDP function implementations to distinguish them from the existing AMDP procedure implementations. Unlike AMDP procedure implementations, AMDP function implementations have a tabular return value, but cannot be called like regular functional methods in ABAP.

## FOR TABLE FUNCTION
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapclass-methods_for_tabfunc.htm)

An AMDP function implementation in whose declaration the addition `FOR TABLE FUNCTION` is specified implements a CDS table function from ABAP CDS. The parameter interface of an AMDP function implementation of this type is specified by the definition of the CDS table function. The associated AMDP function is executed as a data source of an ABAP SQL read statement when accessing the CDS table function directly or indirectly.

## Logical Database Schemas
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenlogical_database_schemas.htm)

Logical database schemas were introduced as symbolic names for physical database schemas in the SAP HANA database. Instead of physical database schemas, logical database schemas can be used by frameworks (in particular AMDP methods) to access objects from different database schemas in Native SQL or AMDP.

## Reference to ABAP Types
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenamdp_abap_types.htm)

When an AMDP method is implemented in an AMDP class with SQLScript, the following new AMDP macro

```ABAP
"$ABAP.type( [name =] abap_type )"
```

can be used to reference ABAP types. The ABAP runtime environment replaces these schemas on the database with the associated database types.

## AMDP OPTIONS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapmethods_amdp_options.htm)

The new addition AMDP OPTIONS for METHODS and CLASS-METHODS statements can be used to define attributes of AMDP methods in their declaration

## Logical HDI Containers
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenlogical_database_schemas.htm#@@ITOC@@ABENLOGICAL_DATABASE_SCHEMAS_4)

Alongside the existing logical database schemas, logical HDI containers can now be used as further logical schemas in the AMDP macro $ABAP.schema. The mapping of a physical database schema to a logical HDI container is made in the definition of an ABAP-managed HDI container, which itself links HDI objects to the Change and Transport System (CTS).

## AMDP Scalar Functions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenamdp_function_methods.htm#@@ITOC@@ABENAMDP_FUNCTION_METHODS_5)

AMDP scalar functions are now supported alongside AMDP table functions. The AMDP function implementation of an AMDP scalar function has an elementary return value and can be used in ABAP like a regular function method. In the implementation of AMDP scalar functions, it is possible to specify the database-specific option DETERMINISTIC after OPTIONS. This buffers the result of the function for the duration of a query.

## Specifying CDS Entities After USING
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapmethod_by_db_proc.htm#!ABAP_ADDITION_4@4@)

In the implementation of the AMDP method, the name of the CDS entity can now be specified after the USING addition for CDS views, CDS table functions, and CDS hierarchies. The name of the CDS managed DDIC view of a CDS view or of the AMDP function of a CDS table function can still be specified, but is best replaced by specifying CDS entities. If a CDS entity is specified, all other database objects of CDS entities must be also be specified using this entity.