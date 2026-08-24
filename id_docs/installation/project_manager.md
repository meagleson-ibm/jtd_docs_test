# Project Manager

Project Manager Code Block for Deployment.

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

Publish the deployment.

**Parent topic:**[Registering Config Services](../../id_docs/installation/registeringconfigservices.md)

