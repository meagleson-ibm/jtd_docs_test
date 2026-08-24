# userdetail-svc application service information

Use the following information to deploy the `userdetail-svc` application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|userdetail-svc|Application|User Detail Service|

|**Profile**|DEV|
|**Label**|1.0|
|**Context**|/api/v1/ss/userdetail|
|**Internal URL**|http://userdetail-svc:7002|
|**External URL**|https://intldsgn-dev.apps.id1.sde.sample.com|
|**Active**|On|
|**Use Datasource**|On|
|**Security Enabled**|Off|

|Key|Value|
|---|-----|
|com.ibm.iw.service.name|userdetail-svc|
|com.ibm.iw.service.description|User Detail Service|
|com.ibm.iw.service.longDescription|User Detail Service|
|feign.client.config.default.readTimeout|180000|
|intldsgn.inter-connect.routing-type|none|
|intldsgn.design-service.url|http://design-svc:7002/api/v1/abls/design|
|intldsgn.notificationmgr-service.url|http://notificationmgr-svc:7002/api/v1/cass/notificationmgr|

## Datasource for deployment

UserAdmin- User Admin Data

`jdbc:postgresql://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn?currentSchema=useradmin`

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

