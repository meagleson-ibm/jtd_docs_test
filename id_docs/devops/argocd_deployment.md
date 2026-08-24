# ArgoCD Deployment

ArgoCD can be installed in the default namespace/project, or a custom one.

ArgoCD should manage resources by having the following label applied to its installation namespace:

```
argocd.argoproj.io/managed-by: <namespace where ArgoCD is installed>
```

In your desired namespace, install the Red Hat `OpenShift GitOps` Operator through the OpenShift OperatorHub.

**Note:** his is different from the ArgoCD operator, which is provided by the community rather than Red Hat.

The installation mode should be **All namespaces**. Choose your desired update approval method and optionally enable the console plugin. You can now use the default `openshift-gitops` ArgoCD instance or create your own.

## Creating a custom ArgoCD instance

If you are creating your own ArgoCD instance, you can use the following template: `argocd.yaml`

```
kind: ArgoCD
 apiVersion: argoproj.io/v1beta1
 metadata:
   name: argocd
   namespace: <1>
 spec:
   controller:
     resources:
       limits:
         cpu: 2000m
         memory: 2048Mi
       requests:
         cpu: 250m
         memory: 1024Mi
   ha:
     enabled: false
   rbac:
     defaultPolicy: ''
     # Adjust RBAC to meet your needs - see example below
     policy: |
       g, system:cluster-admins, role:admin
     scopes: '[groups]'
   redis:
     resources:
       limits:
         cpu: 500m
         memory: 256Mi
       requests:
         cpu: 250m
         memory: 128Mi
   repo:
     resources:
       limits:
         cpu: 1000m
         memory: 1024Mi
       requests:
         cpu: 250m
         memory: 256Mi
   resourceExclusions: |
     - apiGroups:
       - tekton.dev
       clusters:
       - '*'
       kinds:
       - TaskRun
       - PipelineRun
   server:
     resources:
       limits:
         cpu: 500m
         memory: 256Mi
       requests:
         cpu: 125m
         memory: 128Mi
     route:
       enabled: true
       tls:
         termination: reencrypt
     host: <2>
   sso:
     dex:
       openShiftOAuth: true
       resources:
         limits:
           cpu: 500m
           memory: 256Mi
         requests:
           cpu: 250m
           memory: 128Mi
     provider: dex
   disableAdmin: true
   # Enable ArgoCD notifications - optional
   notifications:
     enabled: true
   # Disable various metrics services if not needed
   prometheus:
     enabled: false
   monitoring:
     enabled: false
   grafana:
     enabled: false
```

1.  Namespace to install ArgoCD in

2.  Optional hostname to override the default


## Customizing ArgoCD RBAC permissions

You can customize roles and permissions by changing the values of your ArgoCD application’s `rbac` YAML section. The snippet below creates two groups \(admin and developer\) and maps them to OpenShift groups. It sets the admin group members to be ArgoCD admins and manually specifies a set of permissions that developers have. You may reference ArgoCD’s documentation for additional information.

```
[...]

rbac:
  defaultPolicy: ''
  policy: |
    g, openshift-admin-group, role:admin
    g, openshift-developer-group, role:developer
    p, role:developer, projects, get, namespace-*, allow
    p, role:developer, applications, get, namespace-*/*, allow
    p, role:developer, applications, update, namespace-*/*, allow
    p, role:developer, repositories, get, *, allow
  scopes: '[groups]'

[...]
```

