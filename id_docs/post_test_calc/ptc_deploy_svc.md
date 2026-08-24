# ptc-svc application service information

Use the following information to deploy the ptc-svc application service using the Admin Console.

[Instructions to add an application service in the Admin Console](../admin/service_deployments.md).

|Service name|Service type|Description|
|------------|------------|-----------|
|ptc-svc|Application|Post Test Calculation Backend Services|

|**Profile**|TEST|
|**Label**|1.0|
|**Context**|/api/v1/ptc|
|**Internal URL**|http://ptc-data-svc:7002|
|**External URL**|https://test.ifa.id1.sde.ibm.com|

|Key|Value|
|---|-----|
|COSBUCKET\_SECRET\_KEY| |
|PURVEYOR\_COS\_BUCKET\_NAME| |
|COSBUCKET\_ACCESS\_KEY| |
|COSBUCKET\_ENDPOINT\_PORT| |
|COSBUCKET\_ENDPOINT| |
|REDIS\_HOST| |
|REDIS\_SECRET| |
|REDIS\_PORT| |
|ENVIRONMENT|staging|
|PROJECT\_NAME|ptc|

## Datasource for deployment

-   jdbc:postgresql://<server URL\>:<port\>/<database\>?currentSchema=ptc
-   driverClass = org.postgresql.Driver

**Parent topic:**[Post Test Calculation deployment](../../id_docs/post_test_calc/ptc_deploy_overview.md)

