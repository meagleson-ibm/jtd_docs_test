# Integrationpod

Integrationpod Code Block for Deployment.

```
{
      "label": "1.0",
      "profile": "UAT",
      "status": "Active",
      "servicecontext": "/api/v1/ss/integration",
      "internalurl": "http://integrationpod-svc:7002",
      "externalurl": "https://intldsgn-dev.apps.id1.sde.sample.com",
      "securityon": false,
      "appid": {replace your appid},
      "appname": "integrationpod-svc",
      "props": {
        "com.ibm.iw.service.usesPersistence": {
          "value": "false",
          "secure": false
        },
        "intldsgn.integration.pod.name": {
          "value": "Pod3",
          "secure": false
        },
        "com.ibm.iw.service.longDescription": {
          "value": "Integration Pod for Kafka",
          "secure": false
        },
        "com.ibm.iw.service.name": {
          "value": "integrationpod-svc",
          "secure": false
        },
        "com.ibm.iw.service.description": {
          "value": "Integration Pod for Kafka",
          "secure": false
        },
        "logging.level.feign": {
          "value": "DEBUG",
          "secure": false
        },
        "server.servlet.context-path": {
          "value": "/api/v1/ss/integration",
          "secure": false
        },
        "com.ibm.iw.service.disableMultitenancy": {
          "value": "true",
          "secure": false
        },
      },
      "datasources": null
}

```

Publish the deployment.

**Parent topic:**[Registering Config Services](../../id_docs/installation/registeringconfigservices.md)

