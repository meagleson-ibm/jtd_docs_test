# Die Wafer Manager

Die Wafer Manager Code Block for Deployment.

```
{
      "label": "1.0",
      "profile": "UAT",
      "status": "Active",
      "servicecontext": "/api/v1/abls/diewafermgr",
      "internalurl": "http://diewafermgr-svc:7002",
      "externalurl": "https://intldsgn-dev.apps.id1.sde.sample.com",
      "securityon": false,
      "appid": {replace your appid},
      "appname": "diewafermgr-svc",
      "props": {
        "com.ibm.iw.service.name": {
          "value": "diewafermgr-svc",
          "secure": false
        },
        "com.ibm.iw.service.longDescription": {
          "value": "Die Wafer Manager Service",
          "secure": false
        },
        "com.ibm.iw.service.description": {
          "value": "Die Wafer Manager Service",
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

Publish the deployment.

**Parent topic:**[Registering Config Services](../../id_docs/installation/registeringconfigservices.md)

