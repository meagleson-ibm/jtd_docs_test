# Registering Config Services

You can use **Swagger API** to register all services to ConfigMgr. You can also register and configure services using the **Admin Console**, after it is deployed.

**Note:** You must register and deploy the config-svc service before you can deploy the [Admin Console](../admin/admin_console_overview.md).

**ConfigServices Swagger URL** Please adjust these instructions to suit your environment. The following URL is used to register your services **http://configmgr-svc:7002/api/v1/ss/config/swagger-ui/index.html**. When you configure your environment, you can replace the specified input fields. The following fields can be ignored for creation, because the system creates them automatically. Alternatively, you can remove them at input time.

-   **Input Field to Ignore**

    **id**

    **version**

    **lastModifiedBy**

    **createdBy**

    **createdData**

    **sourceSystem**

    **sourceSystemId**


```

{
"id": 0,
"version": "2024-12-10T11:01:12.942Z",
"lastModifiedBy": "string",
"lastModifiedDate": "2024-12-10T11:01:12.942Z",
"createdBy": "string",
"createdDate": "2024-12-10T11:01:12.942Z",
"sourceSystem": "string",
"sourceSystemId": "string",
"name": "string",
"description": "string",
"servicetype": "string"
}

```

-   ****Common Settings****

    Profile: “UAT” \(Set your keyword.\)

    Label: “1.0


**Data Sources - Common Parameters**

```
}
"dbtype": "Postgresql",
"active": true,
"params": {
"username": "intldsgnapp"
"password": "set_your_password",
"driverClass": "org.postgresql.Driver",
}
```

**Schema Specific Parameters**

|Name|Description|Params url \(adjust your environment\)|
|----|-----------|--------------------------------------|
|DesignData|Intelligent Design Data|jdbc:postgresql://intldsgn-db-rw.intldsgnstaging.svc.cluster.local:5432/intldsgn\_staging?currentSchema=intdsgndata

|
|UserAdmin|User Admin Data|jdbc:postgresql://intldsgn-db-rw.intldsgnstaging.svc.cluster.local:5432/intldsgn\_staging?currentSchema=useradmin

|
|SystemConfig|System Configurtion Data|jdbc:postgresql://intldsgn-db-rw.intldsgnstaging.svc.cluster.local:5432/intldsgn\_staging?currentSchema=systemconfig

|
|ApplicationConfig|Application Configuration Data|jdbc:postgresql://intldsgn-db-rw.intldsgn- staging.svc.cluster.local:5432/intldsgn\_staging?currentSchema=appconfig

|
|PostTestCalculation|PostTest Calculation Data|postgresql+psycopg2://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn\_staging?currentSchema=ptc|
|IntegrationManager|Integration Manager Data|jdbc:postgresql://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn\_staging?currentSchema=integrationmgr|

## Swagger URL

http://configmgr-svc:7002/api/v1/ss/config/swagger-ui/index.html\#/data-source-controller/saveDataSource

Create DataSource one by one. Input sample is below. Replase the specific fields with the above table.

```

{
"name": "DesignData",
"description": "Intelligent Design Data",
"dbtype": "Postgresql",
"active": true,
"params": {
"password": "password",
"driverClass": "org.postgresql.Driver",
"url": "jdbc:postgresql://intldsgn-db-rw.intldsgnstaging.
svc.cluster.local:5432/intldsgn_staging?
currentSchema=intdsgndata",
"username": "intldsgnapp"
}
}

```

## Adding Applications

**Swagger URL**

http://configmgr-svc:7002/api/v1/ss/config/swagger-ui/index.html\#/app-service-controller/saveAppService\(POST /appservice\)

|Name|servicetype|Description|
|----|-----------|-----------|
|usermgr-svc|System|User Manager Service|
|projectmgr-svc|Application|projectmgr-svc|
|macromgr-svc|Application|Macro and Device Manager|
|aspectmgr-svc|Application|Aspect Manager Service|
|listvaluemgr-svc|Application|List Value Manager|
|attachmentmgr-svc|Application|Attachment Manager Service|
|accessctlmgr-svc|Application|Access Control Manager Service|
|config-svc|System|Intellifab Config Service|
|testplanmgr-svc|Application|Test Plan Manager Service|
|diewafermgr-svc|Application|Die Wafer Manager Service|
|equipmgr-svc|Application|Equipment Manager Service|
|web-ui|Application|Frontend Web Service|
|intellifabtest-svc|Application|intellifab-ui|
|0000-common-config|Application|Virtual service for common configuration|
|ptc-svc|Application|ptc-svc|
|ptc-ui|Application|ptc-ui|
|jobexecmgr-svc|Application|JobExecution Manager Service|
|jobresponsemgr-svc|Application|JobResponse Manager Service|
|integrationmgr-svc|Application|Integration Manager Service|
|integrationpod-svc|Application|Integration Pod Service|

**Confirm Results by List**

http://configmgr-svc:7002/api/v1/ss/config/swagger-ui/index.html\#/app-servicecontroller/getAppServiceList \(GET /appservice\)

## Adding Deployments

**Swagger URL**

http://configmgr-svc:7002/api/v1/ss/config/swagger-ui/index.html\#/app-service-controller/addDeployment\(POST /appservice/addDeployment\)

1.  Copy “datasources” - “datasouce” section from Data Source step above.

2.  Replace other fields.

    **Note:**

    -   “appid” should be the one which was created by Adding Applications section.
    -   “datasourceid” should be the same as the target Data Source.

**ProjectMgr**

```
{
      "label": "1.0",
      "profile": "UAT",
      "status": "Active",
      "servicecontext": "/api/v1/abls/projectmgr",
      "internalurl": "http://projectmgr-svc:7002",
      "externalurl": "https://intldsgn-dev.apps.id1.sde.sample.com",
      "securityon": false,
      "appid": {replace your appid},
      "appname": "projectmgr-svc",
      "props": {
        "com.ibm.iw.service.name": {
          "value": "projectmgr-svc",
          "secure": false
        },
        "intldsgn.padset.aspecttemplate": {
          "value": "Padset Aspect Template",
          "secure": false
        },
        "com.ibm.search.filter.eda.project": {
          "value": "eyJmaWx0ZXJzIjpbeyJrZXkiOiJwcm9qZWN0U25hcHNob3RzLnN0YXR1cyIsIm9wZXJhdG9yIjoiSU4iLCJmaWVsZF90eXBlIjoiU1RSSU5HIiwidmFsdWUiOiJBc3BlY3RzIENvbXBsZXRlLFJlbGVhc2VkLERlc2lnbiBGaW5hbGl6ZWQsQ29uZmlnIFZlcmlmaWVkLEJ1aWxkLEF3YWl0aW5nIEFzcGVjdHMsU3RvcCBXb3JrLENyZWF0ZWQiLCJsb2dpY2FsX29wZXJhdG9yIjoiT1IifV19",
          "secure": false
        },
        "com.ibm.iw.service.description": {
          "value": "This is the Project Management service.",
          "secure": false
        }
      },
      "datasources": [
        {
          "tenantid": "",
          "name": "Integration-DesignData",
          "description": "Intelligent Design Data for Integration Database",
          "datasourceid": {replace your id of Integration-DesignData}
        }
      ]
}

```

Publish the Deployment

**Swagger URL**

http://configmgr-svc:7002/api/v1/ss/config/swagger-ui/index.html\#/deployment-controller/publishConfig

1.  Copy the string between “\{“ and “\}” just after “data: “.
2.  /. Put it in parentheses, “\[“ and “\]”.

    For example,


```
[
{
"id": 3,
"version": 1723707673017,
"lastModifiedBy": "SECURITY OFF",
"lastModifiedDate": "2024-08-15T07:41:13.017Z",
"createdBy": "SECURITY OFF",
"createdDate": "2024-08-15T07:41:13.017Z",
"sourceSystem": null,
"sourceSystemId": null,
"label": "1.0",
"profile": "UAT",
"status": "Active",
"servicecontext": "/api/v1/abls/projectmgr",
"internalurl": "http://projectmgr-svc",
"externalurl": "https://intldsgn.apps.id1.sde.sample.com",
"securityon": false,
"appid": 3,
"appname": "projectmgr-svc",
"lastpublshedby": null,
"lastpublisheddate": null,
"props": {
"com.ibm.iw.service.isSystemLevel": {
"value": "false",
"secure": false
},
"intldsgn.aspecttemplatemgr-service.url": {
"value":
"https://intldsgn.apps.id1.sde.sample.com/api/v1/abls/aspectmgr",
"secure": false
},
"intldsgn.macromgr-service.url": {
"value":
"https://intldsgn.apps.id1.sde.sample.com/api/v1/abls/macromgr",
"secure": false
},
"server.port": {
"value": "7002",
"secure": false
},
"com.ibm.iw.service.disableSecurity": {
"value": "true",
"secure": false
},
"com.ibm.iw.service.name": {
"value": "projectmgr-svc",
"secure": false
},
"com.ibm.iw.service.longDescription": {
"value": "This is the Project Management service.",
"secure": false
},
"com.ibm.iw.service.version": {
"value": "1.0",
"secure": false
},
"intldsgn.padset.aspecttemplate": {
"value": "Padset Aspect Template",
"secure": false
},
"com.ibm.iw.service.description": {
"value": "This is the Project Management service.",
"secure": false
}
},
"datasources": [
{
"id": 1,
"version": 1723108046079,
"lastModifiedBy": "SECURITY OFF",
"lastModifiedDate": "2024-08-15T07:41:13.024Z",
"createdBy": "SECURITY OFF",
"createdDate": "2024-08-15T07:41:13.024Z",
"sourceSystem": "string",
"sourceSystemId": "string",
"tenantid": "",
"name": "DesignData",
"description": "Intelligent Design Data",
"datasourceid": 1,
"datasource": {
"id": 1,
"version": 1723706233258,
"lastModifiedBy": "SECURITY OFF",
"lastModifiedDate": "2024-08-15T07:17:13.258Z",
"createdBy": "SECURITY OFF",
"createdDate": "2024-08-15T07:17:13.258Z",
"sourceSystem": null,
"sourceSystemId": null,
"name": "Staging-DesignData",
"description": "Intelligent Design Data",
"dbtype": "Postgresql",
"active": true
}
}
]
}
]
```

**Repeat the same steps for each service.**

**Note:** After deployment and publish operations, restart the target service's pod. OpenShift's rollout command is recommended.

```
> oc rollout restart deployment <deployment name\>
```

-   **[config-svc](../../id_docs/installation/config_svc.md)**  
config-svc Code Block for Deployment.
-   **[0000-common-config](../../id_docs/installation/0000-common-config.md)**  
0000-common-config Code Block for Deployment.
-   **[Macro Manager](../../id_docs/installation/macromgr.md)**  
The Macro Manager is the Macro and Device Manager Application. Use the steps outlined in the Registering Config Service topic to deploy this service.
-   **[Aspect Manager](../../id_docs/installation/aspectmgr.md)**  
The Aspect Manager is Aspect Manager Service Application. Use the steps outlined in the Registering Config Service topic to deploy this service.
-   **[List Value Manager](../../id_docs/installation/listviewmanager.md)**  
The List View Manager is the List view Manager Service Application. Use the steps outlined in the Registering Config Service topic to deploy this service.
-   **[Attachment Manager](../../id_docs/installation/attachment_manager.md)**  
Attachment Manager Code Block for Deployment.
-   **[User Manager](../../id_docs/installation/user_manager.md)**  
User Manager Code Block for Deployment.
-   **[Access Control Manager](../../id_docs/installation/access_control_manager.md)**  
Access Control Manager Code Block for Deployment.
-   **[Test Plan Manager](../../id_docs/installation/test_plan_manager.md)**  
Test Plan Manager Code Block for Deployment.
-   **[Die Wafer Manager](../../id_docs/installation/die_wafer_manager.md)**  
Die Wafer Manager Code Block for Deployment.
-   **[Equipment Manager](../../id_docs/installation/equipment_manager.md)**  
Equipment Manager Code Block for Deployment.
-   **[Notification Manager](../../id_docs/installation/notification_manager.md)**  
Notification Manager Code Block for Deployment.
-   **[Project Manager](../../id_docs/installation/project_manager.md)**  
Project Manager Code Block for Deployment.
-   **[Web-ui](../../id_docs/installation/web-ui.md)**  
Web-ui Code Block for Deployment.
-   **[Intellifabtest-UI](../../id_docs/installation/intellifabtest-ui.md)**  
Front End Webservice Code Block for Deployment.
-   **[Ptc-svc](../../id_docs/installation/ptv-svc.md)**  
Ptc-svc Code Block for Deployment.
-   **[Ptc-ui](../../id_docs/installation/ptc-ui.md)**  
Ptc-ui Code Block for Deployment.
-   **[Jobexecmgr](../../id_docs/installation/jobexecmgr.md)**  
Jobexecmgr Code Block for Deployment.
-   **[Jobresponsemgr](../../id_docs/installation/jobresponsemgr.md)**  
Jobresponsemgr Code Block for Deployment.
-   **[Integrationpod](../../id_docs/installation/integrationpod.md)**  
Integrationpod Code Block for Deployment.
-   **[OpenShift deployment update](../../id_docs/installation/openshift_deploy_update.md)**  
Update deployment/intldsgn-ptc-svc.

