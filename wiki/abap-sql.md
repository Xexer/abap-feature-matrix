# ABAP SQL

## SELECT FROM @itab
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapselect_itab.htm)

An internal table can be specified as a data source data source of a query. This statement cannot be executed on all database systems, if the data from the internal table needs to be passed to the database.

## Multiple tables FROM @itab
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapselect_itab.htm)

It is now possible to process multiple internal tables accessed with `FROM @itab` within one ABAP SQL statement with the ABAP SQL engine. Currently, this is restricted to joins of internal tables where no database tables are involved.