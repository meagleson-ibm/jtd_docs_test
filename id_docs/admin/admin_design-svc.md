# design-svc application service information

Use the following information to deploy the `design-svc` application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|design-svc|Application|Design Service|

|**Profile**|DEV|
|**Label**|1.0|
|**Context**|/api/v1/abls/design|
|**Internal URL**|http://design-svc:7002|
|**External URL**|https://intldsgn-dev.apps.id1.sde.sample.com|
|**Active**|On|
|**Use Datasource**|On|
|**Security Enabled**|Off|

|Key|Value|
|---|-----|
|com.ibm.iw.service.name|design-svc|
|com.ibm.iw.service.description|Design Service|
|com.ibm.iw.service.longDescription|Design Service|
|intldsgn.padset.aspecttemplate|Padset Aspect Template|
|com.ibm.search.filter.eda.project|`eyJmaWx0ZXJzIjpbeyJrZXkiOiJwcm9qZWN0U25hcHNob3RzLnN0YXR1cyIsIm9wZXJhdG9yIjoiSU4iLCJmaWVsZF90eXBlIjoiU1RSSU5HIiwidmFsdWUiOiJBc3BlY3RzIENvbXBsZXRlLFJlbGVhc2VkLERlc2lnbiBGaW5hbGl6ZWQsQ29uZmlnIFZlcmlmaWVkLEJ1aWxkLEF3YWl0aW5nIEFzcGVjdHMsU3RvcCBXb3JrLENyZWF0ZWQiLCJsb2dpY2FsX29wZXJhdG9yIjoiT1IifV19`|
|spring.servlet.multipart.max-request-size|10MB|
|spring.servlet.multipart.max-file-size|10MB|
|com.ibm.search.filter.eda.macros|`eyJmaWx0ZXJzIjpbeyJrZXkiOiJzdGF0dXMiLCJvcGVyYXRvciI6IklOIiwiZmllbGRfdHlwZSI6IlNUUklORyIsInZhbHVlIjoiTGF5b3V0VmVyaWZpZWQsVVBEQVRFX1JFUVVJUkVELFJlYWR5Rm9yQXNzZW1ibHksQXdhaXRpbmdXYWl2ZXIsTGF5b3V0Q29tcGxldGUsUmVxdWVzdENvbXBsZXRlLExheW91dEluUHJvZ3Jlc3MsQnVpbGRDb21wbGV0ZSxVcGRhdGVSZXF1aXJlZCxSZXF1ZXN0SW5jb21wbGV0ZSxSZXF1ZXN0VXBkYXRlZCIsImxvZ2ljYWxfb3BlcmF0b3IiOiJPUiJ9XX0=`|
|com.ibm.search.filter.eda.devices|`eyJmaWx0ZXJzIjpbeyJrZXkiOiJzdGF0dXMiLCJvcGVyYXRvciI6IklOIiwiZmllbGRfdHlwZSI6IlNUUklORyIsInZhbHVlIjoiTGF5b3V0VmVyaWZpZWQsVVBEQVRFX1JFUVVJUkVELFJlYWR5Rm9yQXNzZW1ibHksQXdhaXRpbmdXYWl2ZXIsTGF5b3V0Q29tcGxldGUsUmVxdWVzdENvbXBsZXRlLExheW91dEluUHJvZ3Jlc3MsQnVpbGRDb21wbGV0ZSxVcGRhdGVSZXF1aXJlZCxSZXF1ZXN0SW5jb21wbGV0ZSxSZXF1ZXN0VXBkYXRlZCIsImxvZ2ljYWxfb3BlcmF0b3IiOiJPUiJ9XX0=`|
|server.tomcat.max-swallow-size|-1|
|com.ibm.iw.service.datasource.maximum-pool-size|10|
|intldsgn.database.project.copy.integration.url|https://dev.ifa.id1.sde.ibm.com/api/v1/ss/database/copyProject|

## Datasource for deployment

DesignData - Intelligent Design Data

`jdbc:postgresql://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn?currentSchema=intdsgndata`

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

