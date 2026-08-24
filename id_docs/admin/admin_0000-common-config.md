# 0000-common-config application service information

Use the following information to deploy the `0000-common-config` application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|0000-common-config|Application|Virtual service for common configuration|

|**Profile**| |
|**Label**| |
|**Context**|N/A|
|**Internal URL**|N/A|
|**External URL**|N/A|
|**Active**|On|
|**Use Datasource**|Off|
|**Security Enabled**|Off|

|Key|Value|
|---|-----|
|com.ibm.iw.service.isSystemLevel|false|
|spring.jpa.generate-ddl|false|
|intldsgn.inter-connect.routing-type|internal|
|com.ibm.iw.service.disableSecurity|true|
|intldsgn.servicePassword|\{your password of backendservice user\}|
|com.ibm.iw.service.version|1.0|
|com.iw.ibm.service.usesPersistence|true|
|spring.jpa.hibernate.ddl-auto|validate|
|spring.jpa.show-sql|true|
|intldsgn.serviceUser|backendservice|
|intldsgn.global-var.ilt-device-code-var-lookup-name|`iltDeviceCodeVarLookup`|
|com.ibm.iw.service.datasource.url|http://config-svc:7002/api/v1/ss/config/deployment/getDataSources|
|server.port|7003|
|spring.jpa.properties.org.hibernate.envers.store\_data\_at\_delete|true|
|intldsgn.inter-connect.profile|UAT|
|intldsgn.inter-connect.label|1.0|
|intldsgn.configmgr-service.url|http://config-svc:7002/api/v1/ss/config|
|intldsgn.macro.editable-clone-keys.attribute|iltCLName|
|intldsgn.macro.editable-clone-keys.aspect|xPos,yPos,outlineXPos,outlineYPos,orient|
|intldsgn.device.editable-clone-keys.attribute|iltDeviceCode|
|intldsgn.device.editable-clone-keys.aspect| |
|com.ibm.iw.service.datasource.maximum-pool-size|3|
|server.compression.enabled|true|
|intldsgn.userdetail-service.url|http://userdetail-svc:7002/api/v1/ss/userdetail|
|logging.level.org.zalando.logbook|TRACE|
|logbook.write.max-body-size|0|
|logbook.obfuscate.headers|Authorization,Cookie,Set-Cookie|

|Key|Default value|Description|
|---|-------------|-----------|
|intldsgn.pcell.aspect-template-group-name|pcell|Set the aspect template group's name for PCELLs.|

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

