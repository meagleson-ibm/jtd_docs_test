# masterdata-svc application service information

Use the following information to deploy the `masterdata-svc` application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|masterdata-svc|Application|Master Data Service|

|**Profile**|DEV|
|**Label**|1.0|
|**Context**|/api/v1/abls/masterdata|
|**Internal URL**|http://masterdata-svc:7002|
|**External URL**|https://intldsgn-dev.apps.id1.sde.sample.com|
|**Active**|On|
|**Use Datasource**|On|
|**Security Enabled**|Off|

|Key|Value|
|---|-----|
|com.ibm.iw.service.name|masterdata-svc|
|com.ibm.iw.service.description|Master Data Service|
|com.ibm.iw.service.longDescription|Master Data Service|

## Datasource for deployment

ApplicationConfig - Application Configuration Data

`jdbc:postgresql://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn?currentSchema=appconfig`

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

