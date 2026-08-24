# ID Helm values reference

Intelligent Design Deployment Configuration Reference Table

|Parameter Name|Description|Default|
|--------------|-----------|-------|
|prefixOverride|Set the prefix prepended to all created resources. Can be Release for Helm release name, Chart for Helm Chart name, or a custom string.|Release|
|serviceAccount.create|Specifies whether a service account should be created|False|
|serviceAccount.name|The name of the service account to use|intldsgn|
|serviceMesh.enabled|Whether to enable Istio injection and use virtual services|True|
|serviceMesh.gateway|Service Mesh gateway to use for virtual services| |
|serviceMesh.version|Service Mesh version to use. Determines which label is injected.|2|
|serviceMesh.name|Service Mesh revision name. Used to set `istio.io/rev=`| |
|hostname|Base host name to serve the ID application at| |
|profile|Profile microservices should load config from \(DEV, TEST, UAT, PROD\)| |
|label|Label to load configuration from| |
|keycloak.loginURL|Keycloak login URL for redirects| |
|keycloak.adminURL|URL used to access the Keycloak admin console and API| |
|keycloak.internalURL|Internal URL for Keycloak if hosted within the cluster| |
|keycloak.realm|Keycloak authentication realm to use| |
|securityProxy.enabled|Whether to enable the ID security proxy|false|
|securityProxy.image.repository|Image for security proxy image|intellifab-security-proxy|
|securityProxy.image.tag|Tag for security proxy image|develop|
|securityProxy.allowedDomain|List of domains allowed to access the service via security proxy| |
|configService.enabled|Whether to deploy internal config service|false|
|configService.externalServiceURL|Config service URL to use if enabled=false| |
|configService.image.repository|Image for config service image|semiconductor-config-service|
|configService.image.tag|Tag for config service image|latest|
|configService.replicas|Instances of the service to run|1|
|configService.databaseSecret|Existing secret containing Intelligent Design database connection parameters|intldsgn-secrets|
|configService.security.enabled|Enable spring security for config and dependent services|false|
|configService.security.secretName|Secret name for config service security|intldsgn-secrets|
|baseFrontend.enabled|Whether to enable the base user interface|false|
|baseFrontend.image.repository|Image for base frontend image| |
|baseFrontend.image.tag|Tag for base frontend image|latest|
|baseFrontend.replicas|Instances of the service to run|1|
|baseFrontend.keycloakClientId|Keycloak client to use for base frontend user authentication| |
|baseFrontend.secret|Existing secret with keys keycloak.baseFrontendSecret and nextAuth.secret|intldsgn-secrets|
|testFrontend.enabled|Whether to enable the test frontend interface|false|
|testFrontend.image.repository|Image for test frontend image|intellifab-test-ui|
|testFrontend.image.tag|Tag for test frontend image|latest|
|testFrontend.replicas|Instances of the service to run|1|
|testFrontend.keycloakClientId|Keycloak client to use for test frontend user authentication| |
|testFrontend.secret|Existing secret with keys keycloak.testFrontend and nextAuth.secret|intldsgn-secrets|
|adminConsole.enabled|Whether to enable the admin console user interface|false|
|adminConsole.image.repository|Image for admin console image|semiconductor-admin-ui|
|adminConsole.image.tag|Tag for admin console image|latest|
|adminConsole.replicas|Instances of the service to run|1|
|adminConsole.keycloakClientId|Keycloak client to use for admin console user authentication| |
|adminConsole.managedEnvs|Additional managed environments|'\["DEV","TEST","LOCAL"\]'|
|documentPortal.enabled|Whether to enable the document portal|false|
|documentPortal.image.repository|Image for document portal image|intellifab-api-document-portal|
|documentPortal.image.tag|Tag for document portal image|latest|
|documentPortal.replicas|Instances of the service to run|1|
|userManager.enabled|Whether to enable the user manager|false|
|userManager.image.repository|Image for user manager image|intellifab-usermgr-service|
|userManager.image.tag|Tag for user manager image|latest|
|userManager.replicas|Instances of the service to run|1|
|userManager.keycloakFrontendClientId|Keycloak frontend client to use to manage| |
|userManager.keycloakClientId|Keycloak admin client to use to manage users| |
|userManager.keycloakClientSecret|Existing secret with keycloak.adminClientSecret, keycloak.baseFrontendSecret|intldsgn-secrets|
|accessManager.enabled|Whether to enable the access manager|false|
|accessManager.image.repository|Image for access manager image|intldsgn-accesscontrol-service|
|accessManager.image.tag|Tag for access manager image|latest|
|accessManager.replicas|Instances of the service to run|1|
|aspectManager.enabled|Whether to enable the aspect manager|false|
|aspectManager.image.repository|Image for aspect manager image|intldsgn-aspectmgr-service|
|aspectManager.image.tag|Tag for aspect manager image|latest|
|aspectManager.replicas|Instances of the service to run|1|
|listManager.enabled|Whether to enable the list manager|false|
|listManager.image.repository|Image for list manager image|intldsgn-listmgr-service|
|listManager.image.tag|Tag for list manager image|latest|
|listManager.replicas|Instances of the service to run|1|
|projectManager.enabled|Whether to enable the project manager|false|
|projectManager.image.repository|Image for project manager image|intldsgn-projectmgr-service|
|projectManager.image.tag|Tag for project manager image|latest|
|projectManager.replicas|Instances of the service to run|1|
|macroManager.enabled|Whether to enable the macro manager|false|
|macroManager.image.repository|Image for macro manager image|intldsgn-macromgr-service|
|macroManager.image.tag|Tag for macro manager image|latest|
|macroManager.replicas|Instances of the service to run|1|
|notificationManager.enabled|Whether to enable the notification manager|false|
|notificationManager.image.repository|Image for notification manager image|intldsgn-notificationmgr-service|
|notificationManager.image.tag|Tag for notification manager image|latest|
|notificationManager.replicas|Instances of the service to run|1|
|attachmentManager.enabled|Whether to enable the attachment manager|false|
|attachmentManager.image.repository|Image for attachment manager image|intldsgn-attachment-service|
|attachmentManager.image.tag|Tag for attachment manager image|latest|
|attachmentManager.replicas|Instances of the service to run|1|
|waferManager.enabled|Whether to enable the wafer manager|false|
|waferManager.image.repository|Image for wafer manager image|intldsgn-diewafermgr-service|
|waferManager.image.tag|Tag for wafer manager image|latest|
|waferManager.replicas|Instances of the service to run|1|
|equipmentManager.enabled|Whether to enable the equipment manager|false|
|equipmentManager.image.repository|Image for equipment manager image|intldsgn-equipmentmgr-service|
|equipmentManager.image.tag|Tag for equipment manager image|latest|
|equipmentManager.replicas|Instances of the service to run|1|
|testplanManager.enabled|Whether to enable the test plan manager|false|
|testplanManager.image.repository|Image for test plan manager image|intldsgn-testplanmgr-service|
|testplanManager.image.tag|Tag for test plan manager image|latest|
|testplanManager.replicas|Instances of the service to run|1|
|integrationManager.enabled|Whether to enable the integration manager|false|
|integrationManager.image.repository|Image for integration manager image|intellifab-integrationmgr-service|
|integrationManager.image.tag|Tag for integration manager image|latest|
|integrationManager.replicas|Instances of the service to run|1|
|drcManager.enabled|Whether to enable the DRC manager|false|
|drcManager.image.repository|Image for DRC manager image|intldsgn-drcmgr-service|
|drcManager.image.tag|Tag for DRC manager image|latest|
|drcManager.replicas|Instances of the service to run|1|
|jobExecManager.enabled|Whether to enable the job execution manager|false|
|jobExecManager.image.repository|Image for job execution manager image|intellifab-jobexecmgr-service|
|jobExecManager.image.tag|Tag for job execution manager image|latest|
|jobExecManager.replicas|Instances of the service to run|1|
|jobResponseManager.enabled|Whether to enable the job response manager|false|
|jobResponseManager.image.repository|Image for job response manager image|intellifab-jobresponsemgr-service|
|jobResponseManager.image.tag|Tag for job response manager image|latest|
|jobResponseManager.replicas|Instances of the service to run|1|
|ptc.image.repository|Image for PTC backend image|intldsgn-ptc-backend|
|ptc.image.tag|Tag for PTC backend image|latest|
|ptc.deploymentID|Deployment ID of the PTC service registration from config service| |
|ptc.watchtower.enabled|Whether to enable watchtower|false|
|ptc.watchtower.replicas|Instances of the watchtower service to run|1|
|ptc.delegator.enabled|Whether to enable delegator|false|
|ptc.delegator.replicas|Instances of the delegator service to run|1|
|ptc.functor.enabled|Whether to enable functor|false|
|ptc.functor.replicas|Instances of the functor service to run|1|
|ptc.initiator.enabled|Whether to enable initiator|false|
|ptc.initiator.replicas|Instances of the initiator service to run|1|
|ptc.processor.enabled|Whether to enable processor|false|
|ptc.processor.replicas|Instances of the processor service to run|1|
|ptc.purveyor.enabled|Whether to enable purveyor|false|
|ptc.purveyor.replicas|Instances of the purveyor service to run|1|
|ptc.purveyor.volumeClaimName|Existing PVC name for the purveyor service| |
|ptc.service.enabled|Whether to enable service|false|
|ptc.service.replicas|Instances of the service to run|1|
|ptcFrontend.enabled|Whether to enable the post-test calculation user interface|false|
|ptcFrontend.image.repository|Image for PTC frontend image|intldsgn-ptc-ui|
|ptcFrontend.image.tag|Tag for PTC frontend image|latest|
|ptcFrontend.replicas|Instances of the service to run|1|
|ptcFrontend.keycloakClientId|Keycloak client ID to use for PTC frontend interface| |
|ptcFrontend.secret|Existing secret specifying keycloak.ptcFrontendSecret and nextAuth.secret|intldsgn-secrets|
|integrationPodService.enabled|Whether to enable the integration pod service \(for development\)|false|
|integrationPodService.image.repository|Image for integration pod service image|intellifab-kafka-integration-service|
|integrationPodService.image.tag|Tag for integration pod service image|latest|
|integrationPodService.replicas|Instances of the service to run|1|
|integrationPodService.kafkaBootstrapServer|Kafka bootstrap server for integration pod service|intldsgn-kafka-kafka-bootstrap.intldsgn-common.svc:9092|

