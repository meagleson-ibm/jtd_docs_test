# Updating to Keycloak 26 - ID Keycloak v4.0.0

As of intellifab-keycloak-theme release v4.0.0, the bundled version of Red Hat Build of Keycloak was updated to version 26.

In addition to updating the container image, you must complete the following steps.

1.  [Update the deployment and configmap manifests to reflect required changes to run the new version](update_manifests_r4.md).

2.  [Perform Keycloak DB schema migration to version 26](kc_schema_migration_r4.md).


-   **[Updating the deployment and configuration manifests](../../id_docs/installation/update_manifests_r4.md)**  
The hostnames specified in the configmap must be HTTPS. If you are specifying HTTP or not specifying the protocol at all, prepend HTTPS to the beginning of both KC\_HOSTNAME and KC\_HOSTNAME\_ADMIN.
-   **[Performing the Keycloak schema migration](../../id_docs/installation/kc_schema_migration_r4.md)**  


