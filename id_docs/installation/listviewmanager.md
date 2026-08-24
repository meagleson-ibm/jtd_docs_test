# List Value Manager

The List View Manager is the List view Manager Service Application. Use the steps outlined in the Registering Config Service topic to deploy this service.

```
{
      "label": "1.0",
      "profile": "UAT",
      "status": "Active",
      "servicecontext": "/api/v1/cass/listvaluemgr",
      "internalurl": "http://listvaluemgr-svc:7002",
      "externalurl": "https://intldsgn-dev.apps.id1.sde.sample.com",
      "securityon": false,
      "appid": {replace your appid},
      "appname": "listvaluemgr-svc",
      "props": {
        "com.ibm.iw.service.name": {
          "value": "listvaluemgr-svc",
          "secure": false
        },
        "com.ibm.iw.service.longDescription": {
          "value": "List Value Manager",
          "secure": false
        },
        "com.ibm.iw.service.description": {
          "value": "List Value Manager",
          "secure": false
        }
      },
      "datasources": [
        {
          "tenantid": "",
          "name": "Integration-ApplicationConfig",
          "description": "Application Configuration Data for Integration Database",
          "datasourceid": {replace your id of Integration-ApplicationConfig}
        }
      ]
}

```

Publish the deployment.

**Parent topic:**[Registering Config Services](../../id_docs/installation/registeringconfigservices.md)

