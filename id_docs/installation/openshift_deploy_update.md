# OpenShift deployment update

Update deployment/intldsgn-ptc-svc.

```
spec:
containers:
- command:
- python3
- ./service/testdataapi.pyc
env:
- name: cfg_service_url
value: http://config-svc.intldsgn-common.svc.cluster.local:7002
- name: deployment_id
value: "86"
```

Replace the value of "deployment\_id" with the id of `ptc-svc` on `Config-svc`.

The following deployment settings also need to be updated.

-   intldsgn-ptc-delegator
-   intldsgn-ptc-functor
-   intldsgn-ptc-initiator
-   intldsgn-ptc-processor
-   intldsgn-ptc-purveyor
-   intldsgn-ptc-watchtower

**Parent topic:**[Registering Config Services](../../id_docs/installation/registeringconfigservices.md)

