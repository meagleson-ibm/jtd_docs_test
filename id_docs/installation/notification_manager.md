# Notification Manager

Notification Manager Code Block for Deployment.

```
{
      "label": "1.0",
      "profile": "UAT",
      "status": "Active",
      "servicecontext": "/api/v1/cass/notificationmgr",
      "internalurl": "http://notificationmgr-svc:7002",
      "externalurl": "https://intldsgn-dev.apps.id1.sde.sample.com",
      "securityon": false,
      "appid": {replace your appid},
      "appname": "notificationmgr-svc",
      "props": {
        "intldsgn.inter-connect.routing-type": {
          "value": "none",
          "secure": false
        },
        "spring.mail.host": {
          "value": "{replace your SMTP server. Even if not exist, put dummy hostname.}",
          "secure": false
        },
        "management.health.mail.enabled": {
          "value": "false",
          "secure": false
        },
        "com.ibm.intldsgn.notificationmgr.sse_timeout": {
          "value": "3600000",
          "secure": false
        },
        "spring.mail.port": {
          "value": "25",
          "secure": false
        },
        "com.ibm.iw.service.name": {
          "value": "notificationmgr-svc",
          "secure": false
        },
        "com.ibm.iw.service.longDescription": {
          "value": "Notification Service",
          "secure": false
        },
        "com.ibm.iw.service.description": {
          "value": "Notification Service",
          "secure": false
        },
        "mail.smtp.ssl.enable": {
          "value": "true",
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

