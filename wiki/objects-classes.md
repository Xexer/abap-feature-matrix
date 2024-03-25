# Objects - Classes

## CL_ABAP_DBFEATURES
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencl_abap_dbfeatures.htm)

Since not all database systems support views with parameters, the new class `CL_ABAP_DBFEATURES` with the method `USE_FEATURES` is available, which detects whether this is possible for the current database system.

## CL_ABAP_CORRESPONDING
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencl_abap_corresponding.htm)

The new system class CL_ABAP_CORRESPONDING makes it possible to specify dynamic mapping rules for the component-by-component assignment of structures and internal tables.

### CREATE_USING 
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencl_abap_corresponding_2.htm)

The new methods `CREATE_USING` and EXECUTE_USING for making assignments between internal tables by component while using lookup tables have been added to the system class CL_ABAP_CORRESPONDING.

### EXECUTE_USING 
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencl_abap_corresponding_2.htm)

The new methods CREATE_USING and `EXECUTE_USING` for making assignments between internal tables by component while using lookup tables have been added to the system class CL_ABAP_CORRESPONDING.

### CREATE_WITH_VALUE 
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencl_abap_corresponding_3.htm)

The system class CL_ABAP_CORRESPONDING now has a new method `CREATE_WITH_VALUE`, which allows the values of any suitable data objects to be assigned to the components of the target structure or target table.

## CL_DBI_UTILITIES
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenddic_database_tables_protocol.htm)

The new system class `CL_DBI_UTILITIES` contains utility methods for the database interface. The documented method `IS_LOGGING_ON` can be used to verify whether logging is currently switched on for a database table.

## CL_DYNAMIC_DESTINATION
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenrfc_destination.htm#@@ITOC@@ABENRFC_DESTINATION_2)

The methods of the class `CL_DYNAMIC_DESTINATION` are used to manage dynamic RFC destinations in ABAP release 7.50 and higher. In particular, the method `CREATE_RFC_DESTINATION` makes it possible to create a dynamic destination, which can be used in the current sessions for RFCs.

## CL_ABAP_PARALLEL
[SAP Help](https://community.sap.com/t5/application-development-blog-posts/using-class-cl-abap-parallel-for-mass-parallel-dialog-work-processes/ba-p/13579844)

Using class `CL_ABAP_PARALLEL` is a convenient way to mass process in parallel dialog work processes.  This can be especially powerful in a system with more dialog vs other types of work processes. The class has only been available in the system since release 7.54, but there is a downport up to 7.50, which can be imported via [2791374](https://me.sap.com/notes/2791374).

## CL_ABAP_CONTEXT_INFO
[SAP Help](https://help.sap.com/docs/ABAP_PLATFORM_NEW/b5670aaaa2364a29935f40b16499972d/252df8501f224b668e9d2b00ffd7b5e9.html?locale=en-US)

You can use class `CL_ABAP_CONTEXT_INFO` to retrieve information about the user session, for example, technical user name, business user name, time zone, and so on.

## CL_ABAP_ITAB_UTILITIES
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenvirtual_sort_abexas.htm)

The new method `VIRTUAL_SORT` of class CL_ABAP_ITAB_UTILITIES enables virtual sorting of a set of internal tables with the same number of rows. The internal tables are handled internally like a single combined table containing all the columns of the involved internal tables. The result is an array of row numbers of the virtually sorted combined table.

## CL_ABAP_BEHV_AUX
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abaprap_cl_abap_behv_aux.htm)

The new system class `CL_ABAP_BEHV_AUX` is available for retrieving RAP runtime context information. Using the `GET_CURRENT_HANDLER_KIND` method, you get the information about which RAP handler method is currently running.

### GET_CURRENT_CONTEXT
The system class CL_ABAP_BEHV_AUX has a new method available: RAP runtime context information. Using the `GET_CURRENT_CONTEXT` method, you get context information about the current RAP handler and RAP saver method.

### GET_CURRENT_PHASE
Using the new method GET_CURRENT_PHASE, you get information about the current RAP transactional phase.

## CL_MESSAGE_HELPER
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenif_t100_message.htm)

The new method `GET_LATEST_T100_EXCEPTION` in the class CL_MESSAGE_HELPER is used to return the last object in a chain of exception objects that has an exception text defined by a message. Here, the chain is created using the attribute PREVIOUS.

## CX_SY_STRING_SIZE_TOO_LARGE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenmemory_consumption_2.htm)

The exception that occurs when an operation with a string exceeds its maximum size is now connected to the exception class `CX_SY_STRING_SIZE_TOO_LARGE` and can be handled. Previously, it always resulted in runtime error STRING_SIZE_TOO_LARGE. This exception can also be handled for the statement CALL TRANSFORMATION if some conditions are met.

## CL_ABAP_BIGINT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencl_abap_bigint_doc.htm)

`CL_ABAP_BIGINT` contains methods for calculations with any size of integer in ABAP.

## CL_ABAP_RATIONAL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencl_abap_rational_doc.htm)

`CL_ABAP_RATIONAL` contains methods for calculating with rational numbers without any precision loss.

## CL_ABAP_DIFF
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencl_abap_diff.htm)

The new class `CL_ABAP_DIFF` compares the content of internal tables and returns information about any differences found.

## CL_ABAP_TSTMP
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencl_abap_tstmp.htm)

The new methods `MOVE_TRUNC`, `MOVE_TO_SHORT_TRUNC`, `ADD_TO_SHORT_TRUNC` and `SUBTRACTSECS_TO_SHORT_TRUNC` of system class CL_ABAP_TSTMP round the fractional seconds of long time stamps down while the existing methods MOVE, MOVE_TO_SHORT, ADD_TO_SHORT and SUBTRACTSECS_TO_SHORT round commercially.
