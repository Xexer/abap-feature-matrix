# ABAP Unit

## PARTIALLY IMPLEMENTED
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapinterfaces_partially.htm)

In test classes, the new addition `PARTIALLY IMPLEMENTED` can be specified in the statement INTERFACES, which allows only parts interfaces to be implemented. This is particularly useful in test doubles.

## Class Double (Interface)
[SwH Blog](https://software-heroes.com/en/blog/abap-unit-tdf-test-double-en)

Creates a double for a global interface with the class `CL_ABAP_TESTDOUBLE`.

## Class Double (Class)

## TEST-SEAM
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abentest_seams.htm)

Test seams are language constructs designed especially for unit tests and are implemented using the following statements:
- Defines a test seam as a replaceable area in the production code of a program.
- Replaces the executable statements of a test seam with the statements of an injection in a test class of the same program.

## SQL Double
[SwH Blog](https://software-heroes.com/en/blog/abap-unit-tdf-sql-double-en)

Creates a double for a table with the class `CL_OSQL_TEST_ENVIRONMENT`.

## CDS Double
[SwH Blog](https://software-heroes.com/en/blog/abap-unit-tdf-cds-double-en)

Creates a double for a Core Data Service with the class `CL_CDS_TEST_ENVIRONMENT`.

## "! @testing
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abentest_relations.htm)

This special ABAP Doc comment can be used in front of the declaration of a test class or a test method to define a test relation that links the test class or test method with the repository object specified after `@testing`.

## CL_OSQL_REPLACE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencl_osql_replace.htm)

The system class `CL_OSQL_REPLACE` implements a replacement service that can be used to redirect access to data sources in ABAP SQL statements during the execution of unit tests in ABAP Unit. The system class CL_OSQL_REPLACE can only be used in test classes of ABAP Unit.

## Function Double
[SwH Blog](https://software-heroes.com/en/blog/abap-unit-tdf-function-double-en)

Creates a double of a function module with the class `CL_FUNCTION_TEST_ENVIRONMENT`.

## RAP Double

## Authorization Double

