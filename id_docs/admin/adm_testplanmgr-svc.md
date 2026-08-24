# testplanmgr-svc application service information

Use the following information to deploy the testplanmgr-svc application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|testplanmgr-svc|Application|Test Plan Manager Service|

|**Profile**| |
|**Label**| |
|**Context**|/api/v1/abls/testplanmgr|
|**Internal URL**|http://testplanmgr-svc:7002|
|**External URL**|https://intldsgn-dev.apps.id1.sde.sample.com|
|**Active**|On|
|**Use Datasource**|On|
|**Security Enabled**|Off|

|Key|Value|
|---|-----|
|com.ibm.iw.service.name|`testplanmgr-svc`|
|com.ibm.iw.service.longDescription|Test Plan Manager Service|
|com.ibm.iw.service.description|Test Plan Manager Service|
|spring.servlet.multipart.max-request-size|10MB|
|spring.servlet.multipart.max-file-size|10MB|
|server.tomcat.max-swallow-size|-1|
|instrument.terminal.parallel|false|
|com.ibm.iw.service.datasource.maximum-pool-size|10|
|conflict.msg|This record has been updated by another user since you opened it. Refresh to ensure you’re working with the latest information before making changes.|

## Datasource for deployment

Integration-DesignData

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

