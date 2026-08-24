# Access Control Manager

Access Control Manager Code Block for Deployment.

```
{
      "label": "1.0",
      "profile": "UAT",
      "status": "Active",
      "servicecontext": "/api/v1/abls/accessctlmgr",
      "internalurl": "http://accessctlmgr-svc:7002",
      "externalurl": "https://intldsgn-dev.apps.id1.sde.sample.com",
      "securityon": false,
      "appid": {replace your appid},
      "appname": "accessctlmgr-svc",
      "props": {
        "feign.client.config.default.readTimeout": {
          "value": "180000",
          "secure": false
        },
        "com.ibm.iw.service.name": {
          "value": "accessctlmgr-svc",
          "secure": false
        },
        "com.ibm.iw.service.longDescription": {
          "value": "Access Control Manager Service",
          "secure": false
        },
        "com.ibm.iw.service.description": {
          "value": "Access Control Manager",
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

