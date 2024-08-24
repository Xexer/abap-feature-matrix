# ABAP RESTful Programming Model

## Service Definition
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_service_definitions.htm)

A service definition exposes CDS entities that can be accessed by a business service.

## Service Binding
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abencds_service_bindings.htm)

A service binding is a repository object that binds a service definition to a RESTful protocol, thereby publishing the business service for external consumption.

## Behavior Definitions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl.htm)

RAP behavior definitions are created using the behavior definition language RAP BDL in BDL source code.

## ABAP Behavior Pools
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_behavior_pools.htm)

The ABAP behavior pool (ABP) is a special class pool for an ABAP behavior implementation and based on a RAP behavior definition (BDEF). The global class of the behavior pool does not implement the behavior itself. Instead, the behavior implementation is coded in one or more local RAP handler classes and one RAP saver class in the CCIMP include of the behavior pool.

## ABAP EML
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abeneml.htm)

The ABAP Entity Manipulation Language (EML) is a subset of ABAP for accessing RAP business objects (RAP BOs) and RAP BO interfaces. EML statements allow the data content of a RAP BO (transactional buffer) to be read or modified and the persistent storage of modified data to be triggered.

## BDEF Derived Types
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenrpm_derived_types.htm)

BDEF derived types are special data types in the context of RAP. The types are derived by the ABAP runtime framework from CDS entities and their behavior definition in the BDEF. In general, BDEF derived types are used in ABAP to enable a type-safe access to RAP BOs.

## Unmanaged Scenario
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_impl_type.htm)

## Managed Scenario
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_impl_type.htm)

The new statement `managed` can be used to create managed RAP BOs within the framework of the ABAP RESTful Application Programming Model. This scenario is intended for greenfield developments that are developed from scratch. Standard operations and services are provided by the RAP framework.

## Business Object Projection
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_impl_type.htm)

The new statement projection can be used to create projections of a business object. This projects and aliases a subset of a business object for a specific business service within the framework of the ABAP RESTful Application Programming Model.

## Validation
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_validations.htm)

Checks the consistency of RAP business object instances based on trigger conditions. A validation is automatically invoked by the RAP framework if the trigger condition of the validation is fulfilled.

## Determination
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_determinations.htm)

A determination modifies instances of RAP business objects based on trigger conditions. A determination is implicitly invoked by the RAP framework if the trigger condition of the determination is fulfilled.

## MAPPING FOR
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_type_mapping.htm)

The new statement `mapping for` can be used to map field names from legacy code to field names from the current data model. Available for unmanaged and managed business objects.

## WITH ADDITIONAL SAVE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_saving.htm#!ABAP_VARIANT_1@1@)

The new statement `with additional save` can be used to enhance the default save sequence in a managed implementation scenario.

## WITH UNMANAGED SAVE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_saving.htm#!ABAP_VARIANT_2@2@)

The new statement `with unmanaged save` can be used to implement an own saving strategy in a managed implementation scenario.

## NUMBERING:MANAGED
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_field_numbering.htm)

The new statement `numbering:managed` can be used to automatically generate values for primary key fields with a UUID. Available for managed implementation scenarios.

## New Options for Output Parameters
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_action_output_para.htm)

For actions and functions, the output parameter can now be an entity or a structure.

## SELECTIVE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_action_output_para.htm#!ABAP_ADDITION_2@2@)

The addition `selective` can be used for an output parameter to return only parts of the result structure.

## LOCK MASTER UNMANAGED
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_locking.htm#!ABAP_VARIANT_1@1@)

The new statement `lock master unmanaged` can be used if the application developer wants to implement an own locking mechanism in a managed implementation scenario. An own locking mechanism can be used instead of the RAP locking mechanism provided by the RAP framework.

## WITH DRAFT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_with_draft.htm)

The new statement `with draft` can be used to enable the draft concept for a RAP BO.

## DETERMINE ACTION
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_determine_action.htm)

Determine actions are a new type of action defined using `determine action`. With a determine action, determinations and validations can be executed on request.

## PRECHECK
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_precheck.htm)

The new RAP BO operation addition `precheck` can be used to prevent illegal changes from reaching the application buffer by prechecking modify operations.

## MANDATORY:CREATE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_field_char.htm#!ABAP_VARIANT_5@5@)

RAP BDL now supports the following new field characteristics: `mandatory:create`

## READONLY:UPDATE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_field_char.htm#!ABAP_VARIANT_6@6@)

RAP BDL now supports the following new field characteristics: `readonly:update`

## Virtual Elements
[SAP Help](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/319380e0cef94051ae9aa292ffadb59a.html?locale=en-US)

With ``virtual elements``, you define additional CDS elements that are not persisted on the database, but calculated during runtime using ABAP classes that implement the virtual element interface.

## Augmentation
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_augment_projection.htm)

For projections BDEFs, the operation augment is available. `Augmentation` allows incoming requests with a custom implementation to be enhanced, for example with default values.

## STRICT mode
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_strict_1.htm)

BDEF `strict` mode is now available. It can be enabled using the syntax addition strict and it applies additional syntax checks to RAP behavior definitions.

## Nested Determinations on Modify
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_determinations.htm)

It is now possible to trigger a determination on modify by another determination on modify.

## AUTHORIZATION:UPDATE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_actions_auth_update.htm)

The new RAP BO operation addition authorization:update is available for managed and unmanaged BOs. It delegates the authorization control for an operation to the authorization control that is specified for the update operation.

## ALWAYS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_determine_action.htm)

The new addition `always` can be used for determinations and validations assigned to a determine action. When the determine action is called, determinations and validations with this flag are executed regardless of their trigger conditions.

## FEATURES:GLOBAL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_actions_fc.htm#!ABAP_VARIANT_2@2@)

The new RAP BO operation addition `features:global` can be used to define global feature control for RAP BO operations.

## AUTHORIZATION MASTER (GLOBAL)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_authorization.htm)

Global authorization control is available. It can be defined using authorization master (global).

## LOCK:NONE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_action.htm)

The new RAP BO operation addition `lock:none` can be used to suppress the locking mechanism for an action.

## EARLY NUMBERING
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_early_numb.htm)

The entity behavior characteristic `early numbering` can be used to define unmanaged early numbering for all primary key fields of a managed RAP BO.

## AND CLEANUP
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_saving.htm)

The new addition `and cleanup` is available for additional and unmanaged save in managed RAP BOs. It allows the application developer to implement the cleanup method.

## Define Authorization Context
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_authorization_context.htm)

It is now possible to define authorization contexts in a RAP behavior definition using the keyword define authorization context. There are different ways to activate an authorization context. When activated, all authorization objects listed in the respective context are always successful, that means, the respective authorization checks are skipped.

## Actions and Functions in Projection
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_nonstandard_projection.htm)

It is now possible to define and implement new actions and functions in a projection BDEF.

## FIELD(SUPPRESS)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_field_projection.htm)

In projection BDEFs, a new field characteristic is available: field(suppress). It removes the field in question from the BDEF derived types and from all RAP APIs.

## Abstract Behavior Definitions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_abstract.htm)

A new implementation type is available: the CDS abstract behavior definition. Such abstract BDEFs mainly serve as typing mechanism for deep action or function parameters.

## WITH CONTROL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_define_beh_abstract.htm)

The optional addition `with control` is available for abstract BDEFs. It adds a %control structure to the corresponding derived type structure.

## Business Events
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_event.htm)

Using RAP `business events`, the ABAP RESTful Application Programming Model now offers native support for event-driven architecture. RAP business events are defined with the language element event. A flat or deep output parameter can optionally be specified.

## Late Numbering
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_late_numbering.htm)

RAP `late numbering` is now also available for managed RAP BOs, managed draft-enabled RAP BOs, and for unmanaged draft-enabled RAP BOs.

## WITH PRIVILEGED MODE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_privileged_mode.htm)

A new syntax variant of `with privileged mode` is now available for RAP projection BOs.

## Interface Behavior Definitions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_rap_bo_interface.htm)

A new implementation type is available: the RAP `interface behavior definition`. Such interface BDEFs are based on CDS transactional interfaces and define the behavior of a RAP BO interface. The overall purpose of a RAP BO interface is to project a business object for stable consumption.

## FIELD(SUPPRESS) Managed
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_field_char.htm)

In managed RAP business objects, a new field characteristic is available: `field(suppress)`. It removes the field in question from the BDEF derived types and from all RAP APIs.

## FIELD(SUPPRESS) Unmanaged
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_field_char.htm)

In unmanaged RAP business objects, a new field characteristic is available: field(suppress). It removes the field in question from the BDEF derived types and from all RAP APIs.

## WITH FULL DATA
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_saving.htm#!ABAP_ADDITION_2@2@)

In managed RAP business objects, the optional addition `with full data` can be used in combination with one of the RAP saving options to ensure that full instance data is handed over to the save_modified method of the RAP saver class in the ABAP behavior pool.

## Extensions for RAP
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_extensibility_managed_unm.htm)

BDEF extensions for RAP BOs can be defined using the statement `extension`.

## Extensions for RAP Projection
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_extensibility_projection.htm)

BDEF `projection extensions` for RAP projection business objects can be defined using the statement extension for projection.

## STRICT(2)
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_strict_2.htm)

A new version of BDEF strict mode is available: Strict mode version 2, specified using strict(2). It applies even more syntax checks than the first version.

## QUERY
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_draft_query_view.htm)

The new syntax addition `query` is available to define a draft query view for a draft-enabled RAP BO. This addition is optional. Only in the context of RAP extensibility is it a mandatory prerequisite for the C0 release of the CDS behavior definition in question.

## MANDATORY:EXECUTE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_field_abstract.htm#!ABAP_VARIANT_2@2@)

In RAP abstract behavior definitions, a new RAP field characteristic is available: `mandatory:execute`. It declares the field in question as mandatory. Whenever the hierarchical type is used as input parameter for a RAP action or a RAP function, a value must be supplied.

## RESULT SELECTIVE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_action_output_para.htm#!ABAP_ADDITION_2@2@)

The addition `result selective` is now also possible for deep result types. It can be specified for an output parameter of a RAP action or RAP function to return only parts of the result structure.

## Save Actions with Phase Specification
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_action_onsave.htm)

RAP save actions can now specify one or both of the RAP saver methods finalize or adjustnumbers in brackets to indicate the RAP saver method during which the action can be executed.

## REPEATABLE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_action_repeatable.htm)

RAP actions and RAP functions can be defined as `repeatable`. This syntax addition explicitly allows multiple executions of the same action or function on the same RAP BO entity instance within the same ABAP EML or OData request. The BDEF derived type of a repeatable action or function has an extra %cid component, in contrast to the BDEF derived type of non-repeatable actions or function.

## EXTEND SERVICE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensrvd_extend_service.htm)

It is now possible to define service definition extensions in CDS SDL using the statement `EXTEND SERVICE`.

## PROVIDER CONTRACTS
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensrvd_provider_contract.htm)

The new statement `PROVIDER CONTRACTS` is now available for CDS service definitions. A provider contract defines the type of service binding that is to be used for a service definition. The effect is that stricter syntax checks are applied.

## RAISE ENTITY EVENT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_event.htm)

It is now possible to raise a RAP entity event using this statement.

## Side Effects
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_side_effects.htm)

RAP `side effects` define interdependencies among RAP BO properties that trigger a reload of the affected properties on the user interface. Side effects are translated into annotations in the OData metadata of a RAP service. The syntax for defining RAP side effects is side effects.

## Locale Events
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_use_projection.htm)

In RAP interface behavior definitions, RAP business events can be reused using the syntax `use event`.

## NOTRIGGER[:WARN]
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_field_char.htm#!ABAP_VARIANT_7@7@)

A new RAP field characteristic is available for managed and unmanaged RAP BOs: `notrigger[:warn]`. Fields with this attribute must not be used in a trigger condition of a RAP validation or a RAP determination.

## Static Default Factory Actions
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_action_default_factory.htm)

The syntax addition `default` is available for static factory actions in managed, unmanaged, and projection BDEFs. Exactly one static factory action per RAP BO entity can be defined as default static factory action. The addition default is evaluated by consuming frameworks, such as OData.

## OPTIMIZED
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_draft_action.htm#!ABAP_VARIANT_2@2@)

The optional addition `optimized` is now available for the draft action Activate. SAP recommends always using this addition, since it speeds up the activation of draft instances.

## AUTHORIZATION:GLOBAL
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_actions_auth_global.htm)

Two new RAP BO operation additions are available for actions and determine actions: `authorization:global`

## AUTHORIZATION:INSTANCE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_actions_auth_instance.htm)

Two new RAP BO operation additions are available for actions and determine actions: `authorization:instance`

## WITH MANAGED INSTANCE FILTER
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_mngd_instance_check_proj.htm)

The optional addition `with managed instance filter` is available for projection BDEFs and interface BDEFs. If specified, the WHERE condition of the underlying CDS transactional query or CDS transactional interface is evaluated when the BDEF is accessed with ABAP EML or OData requests from Web clients.

## EXTENSION FOR ABSTRACT
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_extension_for_abstract.htm)

The new statement `extension for abstract` of the RAP BDL makes it possible to add abstract BDEF extensions to abstract behavior definitions. Abstract BDEFs are mainly used as parameters for RAP actions, RAP functions, and RAP business events. An abstract BDEF extension allows you to extend these parameters.

## DRAFT ACTION ADDITIONALSAVE
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenbdl_draft_action.htm#!ABAP_ADDITION_1@1@)

A new draft action is available, `draft action AdditionalSave`. This draft action allows users to define a custom saving strategy for draft instances. It is intended in particular for draft actions with a user-defined implementation, defined using the addition with additional implementation.

## BOPF-Based RAP BO Migration
[SAP Help](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/0a54d0c8a2be4136a8b5d41a367dd537/40535a6f276149bfb1fd03baadd5ba92.html)

A migration tool has been released to migrate CDS-based BOPF business objects to BOPF-based RAP business objects. For details on BOPF-based RAP business objects, see the topic RAP - BOPF-Based RAP Business Objects.

## CL_ABAP_TX
[SAP Help](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abaprap_cl_abap_tx.htm)

Used to explicitly set transitions for RAP transactional phases.

## Leading Entity
(SAP Help)[https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/b09e4d53bfca4544a9f8910bcc2cd9d6.html?locale=en-US]

You can now define a leading entity in the service definition. In the service binding this entity is then marked. Use the following association:

```abap
@ObjectModel.leadingEntity.name: ''
```