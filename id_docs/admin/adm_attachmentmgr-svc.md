# attachmentmgr-svc application service information

Use the following information to deploy the attachmentmgr-svc application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|attachmentmgr-svc|Application|Attachment Manager Service|

|**Profile**| |
|**Label**| |
|**Context**|/api/v1/cass/attachmentmgr|
|**Internal URL**|http://attachmentmgr-svc:7002|
|**External URL**|https://intldsgn-dev.apps.id1.sde.sample.com|
|**Active**|On|
|**Use Datasource**|On|
|**Security Enabled**|Off|

|Key|Value|
|---|-----|
|com.ibm.iw.service.name|`attachmentmgr-svc`|
|com.ibm.iw.service.longDescription|The Attachment Service for Intelligent Design|
|com.ibm.iw.service.description|The Attachment Service for Intelligent Design|
|spring.servlet.multipart.max-file-size|10MB|
|spring.servlet.multipart.max-request-size|10MB|
|server.tomcat.max-swallow-size|-1|

## Datasource for deployment

Integration-DesignData

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

