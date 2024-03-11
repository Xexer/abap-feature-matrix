# Core Data Services

## Define View
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_v1_views.htm)

The new ABAP CDS is the ABAP-specific implementation of the general Core Data Services (CDS). In its first phase, ABAP CDS provides a DDL for the definition of `CDS views`, used together with ABAP SQL to perform reads.

## Define View Entity
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_define_view_entity.htm)

A new kind of CDS view is available: the `CDS view entity`. CDS view entities represent an improved version of CDS DDIC-based views (obsolete) (DEFINE VIEW). They serve the same purpose and have the same structure as CDS DDIC-based views (obsolete), but offer many advantages.

## Association
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_simple_association_v1.htm)

Defines a `CDS association` with the name _assoc in a SELECT statement of a CDS DDIC-based view (obsolete). A CDS association associates the current CDS view as association source with the association target target using an ON condition cds_cond.

## Parameters in view
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_parameter_list_v1.htm)

In the statement DEFINE VIEW, `input parameters` can now be defined for CDS views that can be used in operand positions in the view. When using a CDS view with parameters in a CDS view or in ABAP SQL, the input parameters must be given actual parameters; new additions are available for this in shape of parenthesized, comma-separated lists in the statements SELECT of the DDL and SELECT of ABAP SQL.

## CDS Access Control
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_access_control.htm)

A dedicated `access control` was introduced for ABAP CDS. The new CDS DCL in ABAP CDS makes it possible to define CDS roles. If a CDS entity of a CDS view is linked with a CDS role, additional access conditions are evaluated by default when the CDS entity is accessed by a query processed by SADL and only that data is read for which the current user has an authorization or that matches a literal condition.

## Table Function
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_f1_define_table_function.htm)

The new DDL statement `DEFINE TABLE FUNCTION` can be used to define CDS table functions as a new category of CDS entities. In platform-specific SQL, a CDS table function is implemented in an associated AMDP function implementation.

## Session Variable
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_session_variable_v1.htm)

When a CDS view is accessed using ABAP SQL, three session variables (`$session.user`, `$session.client`, and `$session.system_language`) can be accessed here. In these variables, the values of the system fields sy-uname, sy-mandt and sy-langu are available.

## Session (USER_TIMEZONE)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_session_variable_v1.htm)

User time zone, nominal value of the ABAP system field sy-zonlo. The returned value has the data type CHAR, length 6.

## Session (USER_DATE)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_session_variable_v1.htm)

Current user date, nominal value of the ABAP system field sy-datlo. The returned value is of data type DATS, length 8.

## Metadata Extensions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_f1_annotate_view.htm)

`Metadata extensions` are new CDS objects that allow CDS annotations for a CDS entity to be created and transported separately from their DDL source code. Metadata extensions are included by default in the evaluation of annotations with the class CL_DD_DDL_ANNOTATION_SERVICE.

## Hierarchy
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_f1_define_hierarchy.htm)

The new statement `DEFINE HIERARCHY` can be used to create CDS hierarchies that are accessed as hierarchies in ABAP SQL read statements.

## Abstract Entity
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_f1_define_abstract_entity.htm)

An CDS abstract entity defines the type properties of a CDS entity without creating an instance of a database object. An abstract CDS entity is defined using `DEFINE ABSTRACT ENTITY` in a CDS data definition.

## Hierarchy (Temporal)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_f1_define_hierarchy.htm#!ABAP_ADDITION_3@3@)

The new addition `PERIOD` of the statement `DEFINE HIERARCHY` can now be used to create temporal hierarchies in which the hierarchy nodes are limited by time intervals.

## CDS Projection View
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_define_view_as_projection.htm)

A CDS projection view is a direct projection of the underlying CDS view and exposes only a subset of elements of the projected entity. A CDS projection view is defined using `DEFINE VIEW ENTITY AS PROJECTION ON` in a CDS data definition.

## Custom Entity
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_custom_entities.htm)

A new type of CDS entity is available: the `CDS custom entity`. CDS custom entities are used in the RAP framework to implement ABAP queries in CDS.

## ROOT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_define_root_view_v2.htm)

The new addition `ROOT` is available for CDS entities to mark an entity as a CDS root entity. In addition, CDS associations can be declared as COMPOSITION or TO PARENT. In this way, a CDS composition tree can be modeled for use in the ABAP RESTful Application Programming Model.

## EXTEND VIEW ENTITY
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_extend_view_entity.htm)

The new statement `EXTEND VIEW ENTITY` of the DDL of ABAP CDS makes it possible to add new view fields to existing CDS views entities and CDS projection views by using CDS view entity extensions.

## Typed Literal
[SAP Help]()

## EXTEND ABSTRACT ENTITY
[SAP Help]()

## REDEFINE ASSOCIATION
[SAP Help]()

## PROVIDER CONTRACT
[SAP Help]()

## ANALYTICAL_QUERY
[SAP Help]()

## TRANSACTIONAL_INTERFACE
[SAP Help]()

## EXTEND CUSTOM ENTITY
[SAP Help]()

## Simple Type
[SAP Help]()

## Enumeration
[SAP Help]()

## Scalar Functions
[SAP Help]()

## New Cardinality Syntax
[SAP Help]()
