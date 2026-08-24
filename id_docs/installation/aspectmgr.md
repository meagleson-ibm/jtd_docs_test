# Aspect Manager

The Aspect Manager is Aspect Manager Service Application. Use the steps outlined in the Registering Config Service topic to deploy this service.

```
{
      "label": "1.0",
      "profile": "UAT",
      "status": "Active",
      "servicecontext": "/api/v1/abls/aspectmgr",
      "internalurl": "http://aspectmgr-svc:7002",
      "externalurl": "https://intldsgn-dev.apps.id1.sde.sample.com",
      "securityon": false,
      "appid": {replace your appid},
      "appname": "aspectmgr-svc",
      "props": {
        "intldsgn.inter-connect.routing-type": {
          "value": "none",
          "secure": false
        },
        "com.ibm.iw.service.name": {
          "value": "aspectmgr-svc",
          "secure": false
        },
        "com.ibm.iw.service.longDescription": {
          "value": "Aspect Manager Service",
          "secure": false
        },
        "com.ibm.iw.service.description": {
          "value": "Aspect Manager",
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

