# jobresponsemgr-svc application service information

Use the following information to deploy the jobresponsemgr-svc application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|jobresponsemgr-svc|Application|Job Response Manager Services|

|**Profile**|DEV|
|**Label**|1.0|
|**Context**|/api/v1/abls/jobresponsemgr|
|**Internal URL**|http://jobresponsemgr-svc:7002|
|**External URL**|https://intldsgn-dev.apps.id1.sde.example.com|
|**Active**|Yes|
|**Use Datasource**|Yes|
|**Security Enabled**|Yes|

|Key|Value|
|---|-----|
|com.ibm.iw.service.name|`jobresponsemgr-svc`|
|server.servlet.context-path|`/api/v1/abls/jobresponsemgr`|
|com.ibm.iw.service.longDescription|Job Response Manager|
|com.ibm.iw.service.description|Job Response Manager|
|s3.access.key|`wRe7hxzUrnLdMMju9OJh`|
|s3.secret.key|`Wpugbmfmx6ZpmQkSrUQDJNLhqW+Te5borWFoc/VK`|
|s3.service.endpoint|https://s3-openshift-storage.apps.id1.sde.ibm.com|
|s3.bucket.name|`testbench-report-b2ea31f2-9631-49f7-963e-ee12e24022c5`|

## Datasource for deployment

Integration-DesignData - Intelligent Design Data for Integration Database

-   Database type : `Postgresql`
-   Driver Class : `org.postgresql.Driver`
-   Database URL : jdbc:postgresql://intldsgn-db-rw.intldsgn-common.svc.cluster.local:5432/intldsgn\_integration?currentSchema=intdsgndata

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

