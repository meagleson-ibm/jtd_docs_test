# usermgr-svc application service information

Use the following information to deploy the usermgr-svc application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|usermgr-svc|Application|User Manager Service|

|**Profile**|DEV|
|**Label**|1.0|
|**Context**|/api/v1/ss/usermgr|
|**Internal URL**|http://usermgr-svc:7002|
|**External URL**|https://intldsgn-dev.apps.id1.sde.example.com|
|**Active**|Yes|
|**Use Datasource**|Yes|
|**Security Enabled**|Yes|

|Key|Value|
|---|-----|
|com.ibm.iw.service.name|`usermgr-svc`|
|server.servlet.context-path|`/api/v1/ss/usermgr`|
|com.ibm.iw.service.longDescription|Provides functionality to manage Users, groups and authorizations.|
|com.ibm.iw.service.description|This is the User Management service.|

## Datasource for deployment

Integration-UserAdmin - User Admin Data for Integration Database

-   Database type : `Postgresql`
-   Driver Class : `org.postgresql.Driver`
-   Database URL : jdbc:postgresql://intldsgn-db-rw.intldsgn-common.svc.cluster.local:5432/intldsgn\_integration?currentSchema=useradmin

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

