# Ptc-svc

Ptc-svc Code Block for Deployment.

```
{
    "label": "1.0",
    "profile": "UAT",
    "status": "Active",
    "servicecontext": "/api/v1/abls/ptc",
    "internalurl": "http://ptc-svc:7002",
    "externalurl": "https://intldsgn.apps.id1.sde.sample.com",
    "securityon": false,
    "appid": {replace your appid},
    "appname": "ptc-svc",
    "props": {
      "REDIS_HOST": {
        "value": "ptc-redis.intldsgn.svc.cluster.local",
        "secure": false
      },
      "COSBUCKET_SECRET_KEY": {
        "value": "{replace your secret key}",
        "secure": false
      },
      "COSBUCKET_ACCESS_KEY": {
        "value": "{replace your key}",
        "secure": false
      },
      "PURVEYOR_COS_BUCKET_NAME": {
        "value": "{replace your bucket name}",
        "secure": false
      },
      "REDIS_PORT": {
        "value": "6379",
        "secure": false
      },
      "REDIS_SECRET": {
        "value": "{replace your REDIS secret}",
        "secure": false
      },
      "COSBUCKET_ENDPOINT_PORT": {
        "value": "80",
        "secure": false
      },
      "ENVIRONMENT": {
        "value": "staging",
        "secure": false
      },
      "COSBUCKET_ENDPOINT": {
        "value": "{replace your s3 endpoint}",
        "secure": false
      },
      "PROJECT_NAME": {
        "value": "ptc",
        "secure": false
      }
    },
    "datasources": [
      {
        "id": 60,
        "version": 1737132306031,
        "lastModifiedBy": "SECURITY OFF",
        "lastModifiedDate": "2025-01-17T16:45:06.031Z",
        "createdBy": "SECURITY OFF",
        "createdDate": "2025-01-16T00:16:26.201Z",
        "sourceSystem": null,
        "sourceSystemId": null,
        "tenantid": "",
        "name": "Dev-PostTestCalculation",
        "description": "Intelligent Design Data for Post Test Caslculation Dev",
        "datasourceid": {replace your id of Dev-PostTestCalculation}
      }
    ]
}

```

Publish the deployment.

**Parent topic:**[Registering Config Services](../../id_docs/installation/registeringconfigservices.md)

