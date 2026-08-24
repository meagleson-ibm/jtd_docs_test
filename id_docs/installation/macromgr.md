# Macro Manager

The Macro Manager is the Macro and Device Manager Application. Use the steps outlined in the Registering Config Service topic to deploy this service.

```
SyntaxError: JSON.parse: expected property name or '}' at line 9 column 17 of the JSON data

{
      "label": "1.0",
      "profile": "UAT",
      "status": "Active",
      "servicecontext": "/api/v1/abls/macromgr",
      "internalurl": "http://macromgr-svc:7002",
      "externalurl": "https://intldsgn-dev.apps.id1.sde.sample.com",
      "securityon": false,
      "appid": {replace your appid},
      "appname": "macromgr-svc",
      "props": {
        "server.compression.enabled": {
          "value": "true",
          "secure": false
        },
        "com.ibm.search.filter.eda.devices": {
          "value": "eyJmaWx0ZXJzIjpbeyJrZXkiOiJzdGF0dXMiLCJvcGVyYXRvciI6IklOIiwiZmllbGRfdHlwZSI6IlNUUklORyIsInZhbHVlIjoiTGF5b3V0VmVyaWZpZWQsVVBEQVRFX1JFUVVJUkVELFJlYWR5Rm9yQXNzZW1ibHksQXdhaXRpbmdXYWl2ZXIsTGF5b3V0Q29tcGxldGUsUmVxdWVzdENvbXBsZXRlLExheW91dEluUHJvZ3Jlc3MsQnVpbGRDb21wbGV0ZSxVcGRhdGVSZXF1aXJlZCxSZXF1ZXN0SW5jb21wbGV0ZSxSZXF1ZXN0VXBkYXRlZCIsImxvZ2ljYWxfb3BlcmF0b3IiOiJPUiJ9XX0=",
          "secure": false
        },
        "spring.servlet.multipart.max-request-size": {
          "value": "10MB",
          "secure": false
        },
        "com.ibm.iw.service.name": {
          "value": "macromgr-svc",
          "secure": false
        },
        "spring.servlet.multipart.max-file-size": {
          "value": "10MB",
          "secure": false
        },
        "com.ibm.iw.service.description": {
          "value": "Macro and Device management service.",
          "secure": false
        },
        "com.ibm.search.filter.eda.macros": {
          "value": "eyJmaWx0ZXJzIjpbeyJrZXkiOiJzdGF0dXMiLCJvcGVyYXRvciI6IklOIiwiZmllbGRfdHlwZSI6IlNUUklORyIsInZhbHVlIjoiTGF5b3V0VmVyaWZpZWQsVVBEQVRFX1JFUVVJUkVELFJlYWR5Rm9yQXNzZW1ibHksQXdhaXRpbmdXYWl2ZXIsTGF5b3V0Q29tcGxldGUsUmVxdWVzdENvbXBsZXRlLExheW91dEluUHJvZ3Jlc3MsQnVpbGRDb21wbGV0ZSxVcGRhdGVSZXF1aXJlZCxSZXF1ZXN0SW5jb21wbGV0ZSxSZXF1ZXN0VXBkYXRlZCIsImxvZ2ljYWxfb3BlcmF0b3IiOiJPUiJ9XX0=",
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

