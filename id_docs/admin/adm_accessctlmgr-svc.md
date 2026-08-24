# accessctlmgr-svc application service information

Use the following information to deploy the accessctlmgr-svc application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|accessctlmgr-svc|Application|Access Control Manager Service|

|**Profile**| |
|**Label**| |
|**Context**|/api/v1/abls/accessctlmgr|
|**Internal URL**|http://accessctlmgr-svc:7002|
|**External URL**|https://intldsgn-dev.apps.id1.sde.sample.com|
|**Active**|On|
|**Use Datasource**|On|
|**Security Enabled**|Off|

|Key|Value|
|---|-----|
|com.ibm.iw.service.name|`accessctlmgr-svc`|
|com.ibm.iw.service.longDescription|Access Control Manager Service|
|com.ibm.iw.service.description|Access Control Manager|
|feign.client.config.default.readTimeout|180000|

## Datasource for deployment

Integration-DesignData

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

