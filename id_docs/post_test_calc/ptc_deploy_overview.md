# Post Test Calculation deployment

Use the Intelligent Design Admin Console to deploy the Post Test Calculation application and services.

**Note:** Intelligent Design Post Test Calculation R2.3 is compatible with Intelligent Design 2.1.and 3.0.

## Prerequisites

-   OpenShift Nooba Cloud Object Store bucket must be configured
-   REDIS POD with Cluster with 3 master nodes and 3 fail over nodes, with 512 MB minimum memory and 8 GB Maximum memory each cluster member.
-   A SFTP pod instance.
-   A 300GB Random Access Filesystem available to be shared in between the SFTP pod and the ptc-purveyor pod.
-   Two docker images `ptc-ui` and `ptc-watchtower` \(polymorphic image for all backend components\).

## Required information

1.  OpenShift PostgreSQL database friendly Name: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
2.  OpenShift PostgreSQL database description: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
3.  OpenShift PostgreSQL database internal host name: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
4.  OpenShift PostgreSQL database internal port number: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
5.  OpenShift PostgreSQL database user id: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
6.  OpenShift PostgreSQL database user password: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
7.  OpenShift PostgreSQL database name: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
8.  OpenShift REDIS internal host name: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
9.  OpenShift REDIS TCPIP port number: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
10. OpenShift Redis Cluster Secret Key \(Password\) : \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
11. OpenShift Nooba based Cloud Object Store Endpoint Host name: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
12. OpenShift Nooba based Cloud Object Store Endpoint TCPIP Port number: \_\_\_\_\_\_\_\_\_
13. OpenShift Nooba based Cloud Object Store Endpoint Secret Key: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
14. OpenShift Nooba based Cloud Object Store Endpoint Access key: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
15. OpenShift Post Test Calculation ptc-svc internal host name: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
16. OpenShift Post Test Calculation ptc-svc external host name: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
17. Post Test Calculation Test Data Service Friendly name: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
18. Post Test Calculation Test Data Service description: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
19. Environment Designation \(Consult Configuration Manager Service Documentation for allowed values\): \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
20. Post Test Calculation application name \(“ptc” suggested\): \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
21. The keycloak\_realm: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
22. The keycloak\_url: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
23. The keycloak.ptcFrontendSecret: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
24. The KEYCLOAK\_CLIENT\_ID: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
25. The spring.cloud.config.username: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ \(set to the same as `func_un`\)
26. The spring.cloud.config.password: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ \(set to the same as `func_a`\)
27. Intelligent Design configuration manager service \( “2.1”, “3.0” , …\): \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
28. Intelligent design “security” environment variable \(“true” for ID 3.0+, “false” for 2.1 or below\): \_\_\_\_\_\_\_\_\_\_

**Note:** Registrations should be performed carefully and double checked at every step given that it they have to be precise and once in the system may not be possible to delete any of these registrations. Given that deletion, which is not available, may be required to correct any errors within the registration payloads themselves once set in the configuration manager service.

**Note:** For 2.2.1, if all these registrations are in place, they can remain so no change necessary other than the two environment variables in \(\#25 and \#26\).

-   **[Data source Registration](../../id_docs/post_test_calc/data_src_registration.md)**  
Register a Test Calculation data source using the Admin Console.
-   **[ptc-svc application service information](../../id_docs/post_test_calc/ptc_deploy_svc.md)**  
Use the following information to deploy the ptc-svc application service using the Admin Console.
-   **[Update PTC backend components environment](../../id_docs/post_test_calc/update_ptc_backend.md)**  

-   **[ptc-ui application service information](../../id_docs/post_test_calc/ptc_ui_svc.md)**  
Use the following information to deploy the ptc-ui application service using the Admin Console.
-   **[PTC Admin and User Role Permissions](../../id_docs/post_test_calc/ptc_role_permissions.md)**  
In the Intelligent Design application, user roles define user permissions. Each user has a defined set of permissions that allow or restrict the configuration actions an ID user can take. The Post Test Calculation application has its own set of permissions for PTC Admin and PTC User roles.

**Related information**  


[Admin Console Overview](../admin/admin_console_overview.md)

[Service Deployments](../admin/service_deployments.md)

