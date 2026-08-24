# searchmgr-svc application service information

Use the following information to deploy the searchmgr-svc application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|searchmgr-svc|Application|Fuzzy Search Service|

|**Profile**| |
|**Label**|1.0|
|**Context**|/api/v1/abls/searchmgr|
|**Internal URL**|http://searchmgr-svc:7002|
|**External URL**|https://intldsgn-dev.apps.id1.sde.ibm.com|
|**Active**|On|
|**Use Datasource**|On|
|**Security Enabled**|Off|

|Key|Value|
|---|-----|
|com.ibm.iw.service.name|`searchmgr-svc`|
|server.servlet.context-path|`/api/v1/abls/searchmgr`|
|com.ibm.iw.service.description|Fuzzy Search Service|
|com.ibm.iw.service.longDescription|Fuzzy Search Service|

## Datasource for deployment

DesignData - Intelligent Design Data

jdbc:postgresql://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn?currentSchema=intdsgndata

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

