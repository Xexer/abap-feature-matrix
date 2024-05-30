# ABAP Cloud

## Software Components (ABAP Cloud)
Software components can be created for different language versions in order to define pure TIER-1 packages in which development can be carried out according to the rules of “ABAP for Cloud”.

## T1 Fiori Deployment (ABAP Cloud)
It is currently only possible to deploy a Fiori application in a TIER-1 package from S/4 HANA 2023 FPS1.

## Software Component Relations
(SAP Help)[https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/working-with-software-component-relations?locale=en-US]

Software Component Relations enable the release of all objects of a software component for another software component. This means that release via a C1 contract is no longer necessary and only two components share the objects and releases. This is particularly interesting in the context of reusable components (BC), which take on central tasks and occasionally need to access the caller's components.