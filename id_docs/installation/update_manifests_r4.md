# Updating the deployment and configuration manifests

The hostnames specified in the configmap must be HTTPS. If you are specifying HTTP or not specifying the protocol at all, prepend HTTPS to the beginning of both KC\_HOSTNAME and KC\_HOSTNAME\_ADMIN.

1.  Remove the KC\_HOSTNAME\_STRICT and KC\_HOSTNAME\_STRICT\_BACKCHANNEL environment variable definitions from the deployment manifest.

2.  If running under a service mesh, add an environment variable definition for KC\_CACHE\_EMBEDDED\_MTLS\_ENABLED set to false, since TLS is provided via the mesh.

    **Note:** Keycloak 26 introduces a new management/health endpoint on port 9000, rather than port 8443. The existing readiness and liveness probes, if defined, must be changed from existing port 8443 to 9000. Without this change, the pods will never be marked ready.


**Parent topic:**[Updating to Keycloak 26 - ID Keycloak v4.0.0](../../id_docs/installation/updating_keycloak26_r4.md)

