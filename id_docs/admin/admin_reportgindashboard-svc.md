# reportingdashboard-svc application service information

Use the following information to deploy the reportingdashboard-svc application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|reportingdashboard-svc|System|Intelligent Design Reporting Dashboard Service|

|**Profile**|DEV|
|**Label**|1.0|
|**Context**|/api/v1/abls/reportingdashboard|
|**Internal URL**|http://reportingdashboard-svc:7002|
|**External URL**|https://intldsgn-dev.apps.id1.sde.example.com|
|**Active**|Yes|
|**Use Datasource**|Yes|
|**Security Enabled**|Yes|

|Key|Value|
|---|-----|
|com.ibm.iw.service.name|`reportingdashboard-svc`|
|server.servlet.context-path|`/api/v1/abls/reportingdashboard`|
|com.ibm.iw.service.description|Intelligent Design Reporting Dashboard Service|
|com.ibm.iw.service.longDescription|Intelligent Design Reporting Dashboard Service|

## Datasource for deployment

Integration-ReportConfig - Report Configuration Data for Integration Database

"D

-   Database type : `Postgresql`
-   Driver Class : `org.postgresql.Driver`
-   Database URL : jdbc:postgresql://intldsgn-db-rw.intldsgn-common.svc.cluster.local:5432/intldsgn\_integration?currentSchema=intdsgnrpt

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

