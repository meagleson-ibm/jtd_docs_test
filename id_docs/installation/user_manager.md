# User Manager

User Manager Code Block for Deployment.

```
{
      "label": "1.0",
      "profile": "UAT",
      "status": "Active",
      "servicecontext": "/api/v1/ss/usermgr",
      "internalurl": "http://usermgr-svc:7002",
      "externalurl": "https://intldsgn-dev.apps.id1.sde.sample.com",
      "securityon": false,
      "appid": {replace your appid},
      "appname": "usermgr-svc",
      "props": {
        "com.ibm.iw.service.name": {
          "value": "usermgr-svc",
          "secure": false
        },
        "com.ibm.iw.service.longDescription": {
          "value": "Provides functionality to manage Users, groups and authorizations.",
          "secure": false
        },
        "com.ibm.iw.service.description": {
          "value": "This is the User Management service.",
          "secure": false
        }
      },
      "datasources": [
        {
          "tenantid": "",
          "name": "Integration-UserAdmin",
          "description": "User Admin Data for Integration Database",
          "datasourceid": {replace your id of Integration-UserAdmin}
        }
      ]
}

```

Publish the deployment.

**Parent topic:**[Registering Config Services](../../id_docs/installation/registeringconfigservices.md)

