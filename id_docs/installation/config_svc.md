# config-svc

config-svc Code Block for Deployment.

**Important:** You must register and deploy the config-svc service before you can deploy the [Admin Console](../admin/admin_console_overview.md).

```
{
      "label": "1.0",
      "profile": "UAT",
      "status": "Active",
      "servicecontext": "/api/v1/ss/config",
      "internalurl": "http://config-svc:7002",
      "externalurl": "https://intldsgn-common.apps.id1.sde.ibm.com",
      "securityon": false,
      "appid": {replace your appid},
      "appname": "config-svc",
      "props": {
        "com.ibm.iw.service.isSystemLevel": {
          "value": "false",
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
          "value": "config-svc",
          "secure": false
        },
        "com.ibm.iw.service.longDescription": {
          "value": "Intellifab Config Service",
          "secure": false
        },
        "com.ibm.iw.service.version": {
          "value": "1.0",
          "secure": false
        },
        "com.ibm.iw.service.description": {
          "value": "Intellifab Config Service",
          "secure": false
        }
      },
      "datasources": null
    }

```

Publish the deployment.

**Parent topic:**[Registering Config Services](../../id_docs/installation/registeringconfigservices.md)

