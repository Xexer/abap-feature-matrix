# Dictionary

## Pooled, Cluster Tables
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abennews-753-ddic.htm#!ABAP_MODIFICATION_2@2@)

All support for pooled tables and cluster tables has been dropped. Any existing pooled tables and cluster tables are transformed to transparent tables. Any existing table pools and table clusters are removed. All restrictions that applied when accessing pooled tables and cluster tables hence no longer apply.

## INT8
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbuiltin_types_numeric.htm)

The new built-in data type int8 enables 8-byte integers with signs to be declared.
- The associated data type in ABAP Dictionary was introduced with the name INT8.
- The value range of the new data type int8 is -9,223,372,036,854,775,808 to +9,223,372,036,854,775,807.

## DECFLOAT16
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenddic_builtin_types.htm#@@ITOC@@ABENDDIC_BUILTIN_TYPES_1)

The following built-in ABAP Dictionary data types represent real floating point types of a database: `DECFLOAT16` for 16-digit numbers.

## DECFLOAT34
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenddic_builtin_types.htm#@@ITOC@@ABENDDIC_BUILTIN_TYPES_1)

The following built-in ABAP Dictionary data types represent real floating point types of a database: `DECFLOAT34` for 34-digit numbers.

## DATN
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenddic_date_time_types.htm)

`DATN` for date fields in the database.

## TIMN
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenddic_date_time_types.htm)

`TIMN` for time fields in the database.

## UTCLONG
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbuiltin_types_date_time.htm)

Internal 8-byte integer representation of a UTC time stamp exact to 100 nanoseconds, in ISO-8601 notation between 0001-01-01T00:00:00.0000000 and 9999-12-31T23:59:59.9999999

## GEOM_EWKB
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenddic_geo_data.htm)

The geodata type `GEOM_EWKB` is a built-in data type in ABAP Dictionary that describes the geometric position in a given coordinate reference system.

## Flagging of Deprecated Data
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenddic_deprecation.htm)

Flagging invalid data in a table and modifies the input check and input help in dynpros or WebDynpros.

## DEFINE DYNAMIC CACHE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenddicddl_define_dynamic_cache.htm)

Dynamic cached views are a kind of HANA tuning object defined using the statement `DEFINE DYNAMIC CACHE`. A dynamic cache is a DDIC integration of an SAP HANA Dynamic Result Cache.

## INDICATOR Structures
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abaptypes_indicators.htm)

The new addition `INDICATORS` of the statement TYPES defines an indicator structure as a substructure of a given structured type. An indicator structure can be used as a ABAP SQL indicator in ABAP SQL read and write statements.

## AS BITFIELD
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abaptypes_indicators.htm#!ABAP_ADDITION_2@2@)

The new addition AS `BITFIELD` behind addition INDICATORS of the statement TYPES allows a condensed indicator structure to be defined as a byte field type component of a given structured type. An condensed indicator structure can be used as a null indicator in ABAP SQL statements.