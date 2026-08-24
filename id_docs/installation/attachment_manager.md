# Attachment Manager

Attachment Manager Code Block for Deployment.

```
{
      "label": "1.0",
      "profile": "UAT",
      "status": "Active",
      "servicecontext": "/api/v1/cass/attachmentmgr",
      "internalurl": "http://attachmentmgr-svc:7002",
      "externalurl": "https://intldsgn-dev.apps.id1.sde.sample.com",
      "securityon": false,
      "appid": {replace your appid},
      "appname": "attachmentmgr-svc",
      "props": {
        "spring.servlet.multipart.max-request-size": {
          "value": "10MB",
          "secure": false
        },
        "com.ibm.iw.service.name": {
          "value": "attachmentmgr-svc",
          "secure": false
        },
        "spring.servlet.multipart.max-file-size": {
          "value": "10MB",
          "secure": false
        },
        "com.ibm.iw.service.longDescription": {
          "value": "The Attachment Service for Intelligent Design",
          "secure": false
        },
        "com.ibm.iw.service.description": {
          "value": "The Attachment Service for Intelligent Design",
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

