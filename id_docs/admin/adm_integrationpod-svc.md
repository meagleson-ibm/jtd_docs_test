# integrationpod-svc application service information

Use the following information to deploy the integrationpod-svc application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|integrationpod-svc|Application|Integration Pod for Kafka|

|**Profile**|DEV|
|**Label**|1.0|
|**Context**|/api/v1/ss/integration|
|**Internal URL**|http://integrationpod-svc|
|**External URL**|https://intldsgn-dev.apps.id1.sde.example.com|
|**Active**|Yes|
|**Use Datasource**|Yes|
|**Security Enabled**|Yes|

|Key|Value|
|---|-----|
|com.ibm.iw.service.usesPersistence|false|
|intldsgn.inter-connect.profile|DEV|
|com.ibm.iw.service.disableSecurity|true|
|com.ibm.iw.service.isSystemLevel|true|
|intldsgn.integration.pod.name|Pod3|
|com.ibm.iw.service.longDescription|Integration Pod for Kafka|
|server.port|7003|
|com.ibm.iw.service.name|`integrationpod-svc`|
|com.ibm.iw.service.version|1|
|com.ibm.iw.service.description|Integration Pod for Kafka|
|intldsgn.inter-connect.routing-type|internal|
|logging.level.feign|DEBUG|
|intldsgn.configmgr-service.url|intldsgn.configmgr-service.url|
|server.servlet.context-path|/api/v1/ss/integration|

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

