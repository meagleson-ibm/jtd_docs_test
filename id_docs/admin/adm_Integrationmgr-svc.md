# integrationmgr-svc application service information

Use the following information to deploy the integrationmgr-svc application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|integrationmgr-svc|Application|User Manager Service|

|**Profile**|DEV|
|**Label**|1.0|
|**Context**|/api/v1/ss/integrationmgr|
|**Internal URL**|http://integrationmgr-svc:7002|
|**External URL**|https://intldsgn-dev.apps.id1.sde.example.com|
|**Active**|Yes|
|**Use Datasource**|Yes|
|**Security Enabled**|Yes|

|Key|Value|
|---|-----|
|com.ibm.iw.service.name|`integrationmgr-svc`|
|server.servlet.context-path|`/api/v1/ss/integrationmgr`|
|com.ibm.iw.service.longDescription|Integration Service Manager|
|com.ibm.iw.service.description|Integration Service Manager|

## Datasource for deployment

Test-Design Data - Inteligent Design Data for Test Database

-   Database type : `Postgresql`
-   Driver Class : `org.postgresql.Driver`
-   Database URL : jdbc:postgresql://intldsgn-db-rw.intldsgn-common.svc.cluster.local:5432/intldsgn\_test?currentSchema=intdsgndata

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

