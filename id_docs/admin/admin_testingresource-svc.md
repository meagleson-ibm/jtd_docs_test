# testingresource-svc application service information

Use the following information to deploy the `testingresource-svc` application service.

|Service name|Service type|Description|
|------------|------------|-----------|
|testingresource-svc|Application|Testing Resource Service|

|**Profile**|DEV|
|**Label**|1.0|
|**Context**|/api/v1/abls/testingresource|
|**Internal URL**|http://testingresource-svc:7002|
|**External URL**|https://dev.ifa.id1.sde.ibm.com|
|**Active**|On|
|**Use Datasource**|On|
|**Security Enabled**|Off|

|Key|Value|
|---|-----|
|com.ibm.iw.service.name|testingresource-svc|
|com.ibm.iw.service.description|Intellifab Testing Resource Service is the combination of diewafermgr and equipmentmgr|
|com.ibm.iw.service.longDescription|Intellifab Testing Resource Service is the combination of diewafermgr and equipmentmgr|
|ifa.inter-connect.routing-type|none|

## Datasource for deployment

DesignTest - Design and Test Datasource

`jdbc:postgresql://ifa-integration-db-rw.ifa-dev.svc.cluster.local:5432/ifa_integration?currentSchema=intdsgndata`

**Parent topic:**[Service Deployments](../../id_docs/admin/service_deployments.md)

