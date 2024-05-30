# ABAP Unit

## PARTIALLY IMPLEMENTED
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapinterfaces_partially.htm)

In test classes, the new addition `PARTIALLY IMPLEMENTED` can be specified in the statement INTERFACES, which allows only parts interfaces to be implemented. This is particularly useful in test doubles.

## Class Double (Interface)
[SAP Help](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/abap-oo-test-double-framework?locale=en-US)

Creates a double for a global interface with the class `CL_ABAP_TESTDOUBLE`.

## Class Double (Class)
[SAP Help](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/managing-object-oriented-dependencies-with-abap-unit?locale=en-US)

A slightly different approach is possible if the object under test directly uses the DOC. The DOC has to be a non-final ABAP class. In this case it is possible to implement a test-specific subclass as a test double.

## TEST-SEAM
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abentest_seams.htm) · [SAP Help 2](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/managing-other-dependencies-with-abap-unit?locale=en-US)

Test seams are language constructs designed especially for unit tests and are implemented using the following statements:
- Defines a test seam as a replaceable area in the production code of a program.
- Replaces the executable statements of a test seam with the statements of an injection in a test class of the same program.

## SQL Double
[SAP Help](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/abap-sql-test-double-framework?locale=en-US)

Creates a double for a table with the class `CL_OSQL_TEST_ENVIRONMENT`.

## CDS Double
[SAP Help](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/abap-cds-test-double-framework?locale=en-US)

Creates a double for a Core Data Service with the class `CL_CDS_TEST_ENVIRONMENT`.

## "! @testing
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abentest_relations.htm)

This special ABAP Doc comment can be used in front of the declaration of a test class or a test method to define a test relation that links the test class or test method with the repository object specified after `@testing`.

## CL_OSQL_REPLACE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencl_osql_replace.htm)

The system class `CL_OSQL_REPLACE` implements a replacement service that can be used to redirect access to data sources in ABAP SQL statements during the execution of unit tests in ABAP Unit. The system class CL_OSQL_REPLACE can only be used in test classes of ABAP Unit.

## Function Double
[SAP Help](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/managing-dependencies-on-abap-function-modules-with-abap-unit?locale=en-US)

Creates a double of a function module with the class `CL_FUNCTION_TEST_ENVIRONMENT`.

## Authority Check Helper
[SAP Help](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/managing-dependencies-on-abap-authority-checks-with-abap-unit?locale=en-US)
Use the class `CL_AUNIT_AUTHORITY_CHECK` to change your authorities during Unit Test runtime. You can set specific authorization, that you want to test with your AUTHORITY CHECK.

## Transactional Buffer Double
[SAP Help](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/transactional-buffer-double-support?locale=en-US)

Creates a double for the transactional buffer of a RAP object. Use the class `CL_BOTD_TXBUFDBL_BO_TEST_ENV` with the methods PREPARE_ENVIRONMENT_CONFIG and CREATE to initialize the double.

## Mock EML API
[SAP Help](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/mock-eml-api-support?locale=en-US)

Creates a double for the EML statement to access or modify a RAP object. Use the class `CL_BOTD_MOCKEMLAPI_BO_TEST_ENV` with the methods PREPARE_ENVIRONMENT_CONFIG and CREATE to initialize the double. Before use, you have to configure the call, like the class double.

## bgPF Spy
[SAP Blog](https://community.sap.com/t5/technology-blogs-by-sap/introducing-the-background-processing-framework/ba-p/13579056)

Observe a bgPF (background processing framework) process while using the class `CL_BGMC_TEST_ENVIRONMENT` with the method CREATE_FOR_SPYING, so you could validate informations like processes started.