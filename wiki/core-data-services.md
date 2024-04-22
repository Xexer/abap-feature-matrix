# Core Data Services

## Define View
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_v1_views.htm)

The new ABAP CDS is the ABAP-specific implementation of the general Core Data Services (CDS). In its first phase, ABAP CDS provides a DDL for the definition of `CDS views`, used together with ABAP SQL to perform reads.

## Define View Entity
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_define_view_entity.htm)

A new kind of CDS view is available: the `CDS view entity`. CDS view entities represent an improved version of CDS DDIC-based views (obsolete) (DEFINE VIEW). They serve the same purpose and have the same structure as CDS DDIC-based views (obsolete), but offer many advantages.

## EXTEND VIEW
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_extend_view.htm)

The new statement `EXTEND VIEW` of the DDL of the ABAP CDS makes it possible to add new view fields to existing CDS views - without making changes - by using CDS DDIC-based view extensions.

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

## Session (SYSTEM_DATE)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_session_variable_v1.htm)

When a CDS view is accessed using ABAP SQL, it is possible to access the new session variable `$session.system_date` in which the values of the system field sy-datum are available.

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
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_typed_literal_v2.htm)

`Typed literals` are now available for CDS view entities. Typed literals allow an explicit type declaration and they are available for many built-in ABAP Dictionary data types.

## EXTEND ABSTRACT ENTITY
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_extend_abstract_entity.htm)

The new statement EXTEND ABSTRACT ENTITY of the DDL of ABAP CDS makes it possible to add new elements to existing CDS abstract entities by using CDS abstract entity extensions.

## REDEFINE ASSOCIATION
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_proj_view_redefined_assoc.htm)

In CDS projection views, it is now possible to redefine the CDS associations from the projected entity in the header part. This is done using the keyword `REDEFINE ASSOCIATION`. Redefinition can include a new filter, alias name, and redirection to a new association target, which must also be a CDS projection view, thus moving the complete data model to the projection layer.

## PROVIDER CONTRACT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_pv_provider_contract.htm)

It is now possible to specify a provider contract for CDS projection views using the keyword `PROVIDER CONTRACT`. The provider contract specifies in which scenario a CDS projection view is used, and the scenario in turn determines in which runtime the view is executed and which features are available. Actual only: `TRANSACTIONAL_QUERY`

## ANALYTICAL_QUERY
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_pv_provider_contract.htm#!ABAP_ADDITION_3@3@)

CDS analytical projection views for modelling analytical queries are available. A CDS analytical projection view is defined using DEFINE TRANSIENT VIEW ENTITY AS PROJECTION ON. The value for the provider contract must be set to ANALYTICAL_QUERY.

## TRANSACTIONAL_INTERFACE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_pv_provider_contract.htm#!ABAP_ADDITION_2@2@)

A new type of CDS projection view is available: the CDS transactional interface. CDS transactional interfaces serve as stable public interface layer in a CDS data model. They are typically used in the context of the ABAP RESTful Application Programming Model to provide the basis for a RAP BO interface. A CDS transactional interface view is defined using DEFINE VIEW ENTITY AS PROJECTION ON. The value for the provider contract must be set to `TRANSACTIONAL_INTERFACE`.

## EXTEND CUSTOM ENTITY
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_extend_custom_entity.htm)

The new statement `EXTEND CUSTOM ENTITY` of the DDL of ABAP CDS makes it possible to add new elements to existing CDS custom entities by using CDS custom entity extensions.

## Simple Type
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_define_simple_type.htm)

CDS simple types define elementary data types natively in ABAP CDS. A CDS simple type can be enriched with metadata using CDS annotations. The syntax statement for defining a CDS simple type is `DEFINE TYPE`.

## Enumeration
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_define_enum_type.htm)

CDS enumerated types define enumerated types natively in ABAP CDS. The syntax statement for defining a CDS enumerated type is `DEFINE TYPE ENUM`.

## Scalar Functions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_define_scalar_function.htm)

The new CDS entity is available: the CDS scalar function. It is defined using the CDS DDL statement `DEFINE SCALAR FUNCTION`. A CDS scalar function is linked with an AMDP function in which it is implemented using SQLScript.

## New Cardinality Syntax
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_cardinality_v2.htm#!ABAP_ALTERNATIVE_1@1@)

A new syntax for specifying the cardinality of CDS associations, CDS joins, and of filter conditions of CDS path expressions is now available:

```ABAP
{MANY | ONE | EXACT ONE} TO {MANY | ONE | EXACT ONE}
```

This syntax allows a source and a target cardinality to be specified, while the previously available numeric syntax only allowed the target cardinality to be specified. The new cardinality syntax can be used to improve query performance. It is available in CDS view entities, CDS projection views, CDS custom entities, and CDS abstract entities.

## Table Entities
[SAP Roadmap](https://help.sap.com/docs/abap-cross-product/roadmap-info/implementation)

So far, the ABAP CDS-based modeling approach didn’t cover the definition of the persistence layer of your application. With CDS table entities this gap will be closed. They'll allow you the define and manage HANA database tables via “first class” CDS concepts (like associations, annotations, CDS simple types and CDS aspects) and by offering “nice” camel-case names for entity- and element names.