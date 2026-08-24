# macromgr-svc application service information

Use the following information to deploy the macromgr-svc application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|macromgr-svc|Application|Macro Manager Service|

|**Profile**| |
|**Label**| |
|**Context**|/api/v1/abls/macromgr|
|**Internal URL**|http://macromgr-svc:7002|
|**External URL**|https://intldsgn-dev.apps.id1.sde.sample.com|
|**Active**|On|
|**Use Datasource**|On|
|**Security Enabled**|Off|

|Key|Value|
|---|-----|
|server.compression.enabled|true|
|spring.servlet.multipart.max-request-size|10MB|
|spring.servlet.multipart.max-file-size|10MB|
|com.ibm.iw.service.name|`macromgr-svc`|
|com.ibm.iw.service.description|Macro and Device management service.|
|com.ibm.search.filter.eda.macros|`eyJmaWx0ZXJzIjpbeyJrZXkiOiJzdGF0dXMiLCJvcGVyYXRvciI6IklOIiwiZmllbGRfdHlwZSI6IlNUUklORyIsInZhbHVlIjoiTGF5b3V0VmVyaWZpZWQsVVBEQVRFX1JFUVVJUkVELFJlYWR5Rm9yQXNzZW1ibHksQXdhaXRpbmdXYWl2ZXIsTGF5b3V0Q29tcGxldGUsUmVxdWVzdENvbXBsZXRlLExheW91dEluUHJvZ3Jlc3MsQnVpbGRDb21wbGV0ZSxVcGRhdGVSZXF1aXJlZCxSZXF1ZXN0SW5jb21wbGV0ZSxSZXF1ZXN0VXBkYXRlZCIsImxvZ2ljYWxfb3BlcmF0b3IiOiJPUiJ9XX0=`|
|com.ibm.search.filter.eda.devices|`eyJmaWx0ZXJzIjpbeyJrZXkiOiJzdGF0dXMiLCJvcGVyYXRvciI6IklOIiwiZmllbGRfdHlwZSI6IlNUUklORyIsInZhbHVlIjoiTGF5b3V0VmVyaWZpZWQsVVBEQVRFX1JFUVVJUkVELFJlYWR5Rm9yQXNzZW1ibHksQXdhaXRpbmdXYWl2ZXIsTGF5b3V0Q29tcGxldGUsUmVxdWVzdENvbXBsZXRlLExheW91dEluUHJvZ3Jlc3MsQnVpbGRDb21wbGV0ZSxVcGRhdGVSZXF1aXJlZCxSZXF1ZXN0SW5jb21wbGV0ZSxSZXF1ZXN0VXBkYXRlZCIsImxvZ2ljYWxfb3BlcmF0b3IiOiJPUiJ9XX0=`|
|server.tomcat.max-swallow-size|-1|
|com.ibm.iw.service.datasource.maximum-pool-size|10|

## Datasource for deployment

Integration-DesignData

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

