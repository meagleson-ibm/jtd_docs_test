# 0000-common-config

0000-common-config Code Block for Deployment.

```
{
      "label": "1.0",
      "profile": "UAT",
      "status": "Active",
      "servicecontext": "NA",
      "internalurl": "NA",
      "externalurl": "NA",
      "securityon": false,
      "appid": {replace your appid},
      "appname": "0000-common-config",
      "props": {
        "com.ibm.iw.service.isSystemLevel": {
          "value": "false",
          "secure": false
        },
        "spring.jpa.generate-ddl": {
          "value": "false",
          "secure": false
        },
        "intldsgn.inter-connect.routing-type": {
          "value": "internal",
          "secure": false
        },
        "com.ibm.iw.service.disableSecurity": {
          "value": "true",
          "secure": false
        },
        "intldsgn.servicePassword": {
          "value": "{replace your password of backendservice user}",
          "secure": false
        },
        "com.ibm.iw.service.version": {
          "value": "1.0",
          "secure": false
        },
        "com.iw.ibm.service.usesPersistence": {
          "value": "true",
          "secure": false
        },
        "spring.jpa.hibernate.ddl-auto": {
          "value": "validate",
          "secure": false
        },
        "spring.jpa.show-sql": {
          "value": "true",
          "secure": false
        },
        "intldsgn.serviceUser": {
          "value": "backendservice",
          "secure": false
        },
        "intldsgn.global-var.ilt-device-code-var-lookup-name": {
          "value": "iltDeviceCodeVarLookup",
          "secure": false
        },
        "com.ibm.iw.service.datasource.url": {
          "value": "http://config-svc:7002/api/v1/ss/config/deployment/getDataSources",
          "secure": false
        },
        "server.port": {
          "value": "7003",
          "secure": false
        },
        "spring.jpa.properties.org.hibernate.envers.store_data_at_delete": {
          "value": "true",
          "secure": false
        },
        "intldsgn.inter-connect.profile": {
          "value": "UAT",
          "secure": false
        },
        "intldsgn.inter-connect.label": {
          "value": "1.0",
          "secure": false
        },
        "intldsgn.configmgr-service.url": {
          "value": "http://config-svc:7002/api/v1/ss/config",
          "secure": false
        },
        "intldsgn.usermgr-service.url": {
          "value": "http://usermgr-svc:7002/api/v1/ss/usermgr",
          "secure": false
        }
      },
      "datasources": null
}

```

Publish the deployment.

**Parent topic:**[Registering Config Services](../../id_docs/installation/registeringconfigservices.md)

