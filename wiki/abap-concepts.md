# ABAP Concepts

## Inline Declaration
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

## ABAP Messaging Channels
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenamc.htm)

From ABAP release 7.40, SP02, `ABAP Messaging Channels (AMC)` enable a new type of communication between AS ABAP programs, which goes beyond the limits of an AS instance.

## ABAP Docs
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abendoccomment.htm)

Special ABAP Doc comments can be entered in front of declaration statements. These comments are prefixed by `"!`. Tools of an ABAP development environment that support ABAP Doc, such as ABAP development tools for Eclipse, analyze the content of ABAP Doc comments, converts it to HTML and display the content in an appropriate way.

## Meshes (Types & Processing)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_meshes.htm)

The meshes are special structures whose components are internal tables, which can be linked to each other using mesh associations. Mesh associations are evaluated by specifying mesh paths in suitable expressions and statements.

## ABAP Push Channels
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenapc.htm)

`ABAP Push Channels (APC)` enable bidirectional communication between AS ABAP and the internet using the WebSocket protocol.

## Predicative Method Calls
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenpredicative_method_calls.htm)

A predicative method call is a relational expression whose only operand is a functional method call `meth( ... )`.

## ABAP for Key Users
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_for_key_users_glosry.htm)

In ABAP release 7.50, a new ABAP version for ABAP for Key Users was introduced. This version is designed for enhancements in delivered enhancement points made by Key Users. The internal version ID in the column UCCHECK of the system table TRDIR is 2.

## ABAP Doc short texts
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abendoccomment.htm#@@ITOC@@ABENDOCCOMMENT_4)

It is now possible to define short texts in ABAP comments and synchronize them with the short texts of methods and function modules in ABAP Workbench.

## ABAP Daemons
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_daemon.htm)

An ABAP Daemon is an instance of an ABAP Daemon class in an ABAP Daemon session. An ABAP Daemon is created again automatically every time a runtime error or a message of type E, A, or X causes a program termination.

## ABAP Doc links
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abendoccomment.htm#@@ITOC@@ABENDOCCOMMENT_5)

The new syntax `{@link ...}` makes it possible to link to other documentation of repository objects (or its components) in ABAP Doc comments.

## HANA only
[SAP Help](https://help.sap.com/docs/SAP_HANA_PLATFORM/fc5ace7a367c434190a8047881f92ed8/d8d14ef53e244f6cabd10dd3f5e8c11e.html?locale=en-US)

As of this release, only an SAP HANA database is supported as the standard database of an AS ABAP. For this reason, Open SQL was renamed to ABAP SQL (see ABAP SQL in ABAP Release 7.53). Note: Using a secondary connection in ABAP SQL, it is still possible to connect to other databases.

## Open SQL to ABAP SQL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_sql.htm)

The existing name Open SQL has been changed to ABAP SQL. This renaming reflects that some parts of ABAP SQL now only support certain database platforms, specifically SAP HANA database, and hence that it is no longer fully platform-independent.

## ABAP for Cloud Development
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_versions_and_apis.htm#@@ITOC@@ABENABAP_VERSIONS_AND_APIS_1)

In ABAP release 7.53, a new ABAP version ABAP for Cloud Development was introduced. The internal version ID in the column UCCHECK of the system table TRDIR is 5.

## PCRE regular expressions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenregex_pcre_syntax.htm)

Besides the existing support of POSIX regular expressions, ABAP supports now also PCRE regular expressions that are processed by the PCRE2 Library implemented in the ABAP Kernel. PCRE regular expressions can be used in the same way as POSIX regular expressions.

## Component Selector
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenobject_component_selector.htm)

The following syntax can be used for the object component selector -> to access components and attributes dynamically now:

```ABAP
... { dref->(comp_name) }
  | { cref->(attr_name) }
  | { iref->(attr_name) } ...
```

## XPath Regular Expressions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenregex_xpath_syntax.htm)

Besides the existing support of PCRE regular expressions and POSIX regular expressions (obsolete) ABAP supports now also XPath regular expressions and XSD regular expressions. Internally, those are transformed to PCRE regular expressions and processed by the PCRE2 Library.

## XSD Regular Expressions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenregex_xsd_syntax.htm)

Besides the existing support of PCRE regular expressions and POSIX regular expressions (obsolete) ABAP supports now also XPath regular expressions and XSD regular expressions. Internally, those are transformed to PCRE regular expressions and processed by the PCRE2 Library.

## Alias Names for Secondary Keys
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenitab_key_secondary.htm)

Alias names can now be declared for secondary keys of internal tables by using the addition ALIAS of TYPES and DATA. This can be helpful when changing existing secondary keys without invalidating users.

## SELF
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenrfc_destination.htm#@@ITOC@@ABENRFC_DESTINATION_3)

The new predefined RFC destination SELF works as NONE but uses the RFC protocol fast serialization.

## Software Components (ABAP Cloud)
Software components can be created for different language versions in order to define pure TIER-1 packages in which development can be carried out according to the rules of “ABAP for Cloud”.

## T1 Fiori Deployment (ABAP Cloud)
It is currently only possible to deploy a Fiori application in a TIER-1 package from S/4 HANA 2023 FPS1.

## bgPF
[SAP Help](https://help.sap.com/docs/abap-cloud/abap-concepts/background-processing-framework?locale=en-US) · [SAP Blog](https://community.sap.com/t5/technology-blogs-by-sap/introducing-the-background-processing-framework/ba-p/13579056)

The bgPF (`background processing framework`) is a framework that offers functionality and convenience for applications, which need to run processing steps in the background, in a reliable way. It is a simple and easy-to-use feature to execute time-consuming ABAP methods asynchronously and reliably.

## ABAP SQL Table Buffer Engine
[SAP Blog](https://community.sap.com/t5/technology-blogs-by-sap/joins-on-internal-tables-the-abap-sql-table-buffer-engine-is-grown-up/ba-p/13572640)

The ABAP table buffer has an innocent-sounding name. Contrary to query buffers, which store the result of a previous query, the ABAP table buffer buffers the underlying database tables. It is then possible to execute SELECT queries on these buffered tables. This happens through a full-fledged in-memory database engine, the ABAP SQL Engine. In this case, all SQL is executed in the ABAP server and not on the database.

Release 1709 (7.52):
- Single buffered table or internal table in the FROM clause
- WHERE conditions without subselects
- COUNT(*) aggregate function (but no other aggregate functions)
- ORDER BY PRIMARY KEY

Release 1809 (7.53):
- Some common SQL functions (like CONCAT, SUBSTRING, LEFT, UPPER)
- Arithmetic expressions (+, -, *)
- SQL expressions like CASE or COALESCE
- NULL values

Release 2022 (7.57):
- Arbitrary ORDER BY clause

Release 2023 (7.58):
- Joins and CTEs on internal tables

## Service Consumption Model
[SAP Help](https://help.sap.com/docs/ABAP_PLATFORM_NEW/c238d694b825421f940829321ffa326a/96132822b3554016b653d3601bb9ff1a.html?locale=en-US)

The Service Consumption Model is an easy way to consume OData, SOAP and RFC scenarios and will be available on-premise with release 2025. Actual you can [build a wrapper](https://community.sap.com/t5/technology-blogs-by-sap/how-to-use-the-odata-client-proxy-in-sap-s-4-hana-or-how-to-use-the-odata/ba-p/13425200) with the existing classes, to use it before 2025.