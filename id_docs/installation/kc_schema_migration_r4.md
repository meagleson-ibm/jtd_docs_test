# Performing the Keycloak schema migration

**Important:** The schema migration is a one-way change. You cannot roll back to Keycloak 24 after the upgrade is complete. Before performing the migration, make a full backup of the Keycloak database.

Keycloak itself will handle the schema migration on the first run of version 26. Only one instance should be running during the migration.

1.  Scale the Keycloak deployment down to one pod.

    This can be done through the helm values or by directly manipulating the deployment resource.

2.  Once only one Keycloak pod is running, update the image definition to use the new version of Keycloak.

    The Keycloak pod is recreated, and Keycloak performs the schema migration.

3.  After the logs indicate the migration is complete, you can scale the deployment back up to its original pod count.

    ```
    2025-06-23 18:47:36,399 INFO [org.keycloak.storage.datastore.DefaultMigrationManager] (main) Migrating older model to 25.0.0
    2025-06-23 18:47:36,442 INFO [org.keycloak.connections.infinispan.DefaultInfinispanConnectionProviderFactory] (main) Node name: intellifab-keycloak-8dd7fdcff-g89d8-43272, Site name: null
    2025-06-23 18:47:37,845 INFO [org.keycloak.storage.datastore.DefaultMigrationManager] (main) Migrating older model to 26.0.0
    2025-06-23 18:47:37,949 INFO [org.keycloak.storage.datastore.DefaultMigrationManager] (main) Migrating older model to 26.1.0
    2025-06-23 18:47:38,075 INFO [org.keycloak.storage.datastore.DefaultMigrationManager] (main) Migrating older model to 26.2.0
    2025-06-23 18:47:39,095 INFO [io.quarkus] (main) Keycloak 26.2.4.redhat-00002 on JVM (powered by Quarkus 3.20.0.redhat-00002) started in 19.506s. Listening on: http://0.0.0.0:8080 and https://0.0.0.0:8443. Management interface listening on https://0.0.0.0:9000.
    2025-06-23 18:47:39,096 INFO [io.quarkus] (main) Profile prod activated.
    2025-06-23 18:47:39,096 INFO [io.quarkus] (main) Installed features: [agroal, cdi, hibernate-orm, jdbc-postgresql, keycloak, narayana-jta, opentelemetry, reactive-routes, rest, rest-jackson, smallrye-context-propagation, smallrye-health, vertx]
    ```


**Parent topic:**[Updating to Keycloak 26 - ID Keycloak v4.0.0](../../id_docs/installation/updating_keycloak26_r4.md)

