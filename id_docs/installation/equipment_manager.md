# Equipment Manager

Equipment Manager Code Block for Deployment.

```
{
      "label": "1.0",
      "profile": "UAT",
      "status": "Active",
      "servicecontext": "/api/v1/abls/equipmentmgr",
      "internalurl": "http://equipmentmgr-svc:7002",
      "externalurl": "https://intldsgn-dev.apps.id1.sde.ibm.com",
      "securityon": false,
      "appid": {replace your appid},
      "appname": "equipmentmgr-svc",
      "props": {
        "intldsgn.inter-connect.routing-type": {
          "value": "none",
          "secure": false
        },
        "com.ibm.iw.service.name": {
          "value": "equipmentmgr-svc",
          "secure": false
        },
        "com.ibm.iw.service.longDescription": {
          "value": "Equipment Manager Service",
          "secure": false
        },
        "com.ibm.iw.service.description": {
          "value": "Equipment Manager Service",
          "secure": false
        }
      },
      "datasources": [
        {
          "id": 53,
          "version": 1733957886118,
          "lastModifiedBy": "SECURITY OFF",
          "lastModifiedDate": "2024-12-11T22:58:06.118Z",
          "createdBy": "SECURITY OFF",
          "createdDate": "2024-10-17T13:53:23.301Z",
          "sourceSystem": "string",
          "sourceSystemId": "string",
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

