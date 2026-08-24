# Deploying a stand-alone config service instance

For more information on filling out the Helm chart values and support parameters, see \(docs to be added\).

1.  Fill out the Helm values template as shown.

    `values.yaml`

    ```
    prefixOverride: Chart
     serviceMesh:
       enabled: true
       gateway: intldsgn-istio/intldsgn-apps-gw
       host: intldsgn-common.apps.id1.sde.ibm.com
    
     hostname:
     profile: DEV
     label: 1.0
    
     configService:
       enabled: true
       image:
         repository: registry.apps.id1.sde.ibm.com/intldsgn/semiconductor-config-service
         tag: develop@sha256:ee994b1c6578770829e38d6b3fffc5790b31747746dbbe42de14880b7efe8a4f
       replicas: 2
       databaseSecret: intldsgn-secrets
    
     webService:
       enabled: false
     adminConsole:
       enabled: false
     documentPortal:
       enabled: false
     userManager:
       enabled: false
     accessManager:
       enabled: false
     aspectManager:
       enabled: false
     listManager:
       enabled: false
     projectManager:
       enabled: false
     macroManager:
       enabled: false
     notificationManager:
       enabled: false
     attachmentManager:
       enabled: false
    ```

2.  Use the following instructions to deploy:

    -   [Installing with Helm](install_with_helm.md)
    -   [Installing with ArgoCD](install_with_argocd.md)

