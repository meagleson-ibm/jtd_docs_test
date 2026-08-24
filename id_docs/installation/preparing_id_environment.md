# Preparing the ID environment

Preparing the ID environment requires multiple steps.

Make sure that your environment meets the following requirements.

1.  External PostgreSQL database server
    1.  Database created for config service
    2.  Database user/role credentials with sufficient permission to the database
2.  Red Hat OpenShift project/namespace and namespace-level admin privileges
3.  \(Optional\) Red Hat OpenShift Service Mesh / Istio deployed
4.  Access to Intelligent Design container images \(pull secret\)
5.  Customized Helm chart values file for your environment

There are three steps to fully prepare your ID environment.

-   Creating the Required Secrets
-   Associating the Pull Secret Service with a Service Account
-   Creating the Helm Values file

## Creating the Required Secrets

You must have a pull secret \(credentials of K8s secret\) provided by the registry that is hosting the Intelligent Design container images.

1.  Navigate to your target namespace in the Red Hat OpenShift console.

2.  In the **Administrator** view, select **Secrets** under the **Workloads** menu in the sidebar.

3.  Click the drop-down arrow in the **Create** button and select **Image Pull Secret**.

4.  Enter a secret name, such as **intldsgn-pull-secret** and complete the **Registry server address**, **username**, and **password** with the provided values.

    If you were provided a **YAML** containing the secret, apply it to your target namespace.

    ```
    oc apply -n <target namespace> -f pull_secret.yaml
    ```


## Associating the Pull Secret with a Service Account

If you are using the default service account to deploy the ID services, associate the pull secret with that account.

## ID App Secret

**Note:** The values for secret should be encoded by base64.

For the configuration service to access the database, you must create a Kubernetes secret resource containing the database connection parameters and a valid username and password. You might use the following **YAML** template. Replace the values in the chevrons with your corresponding values. See the accompanying list after the codeblock.

intldsgn-secrets.yaml

```
 kind: Secret
 apiVersion: v1
 metadata:
 name: intldsgn-secrets
 namespace: <your namespace>
 labels:
   app: intelligent-design
   app.kubernetes.io/name: intldsgn
   app.kubernetes.io/part-of: intelligent-design
 data:
   KEYCLOAK_CLIENT_SECRET: (1)
   NEXTAUTH_SECRET:  (2)
   keycloak.adminClientId:  (3)
   keycloak.adminClientSecret:  (4)
   spring.datasource.password:  (5)
   spring.datasource.url:  (6)
   spring.datasource.username:  (7)
 type: Opaque
```

The following list outlines the values to use in the **YAML** template. Numbered values in the template correspond to list items.

-   \(1\) Client secret obtained from Keycloak instance.
-   \(2\) Random string used to encrypt data. This can be generated with the following command.

    ```
    openssl rand -base64 32
    ```

-   \(3\) Client ID from Keycloak for admin console authentication.
-   \(4\) Client secret from Keycloak for admin console authentication.
-   \(5\) PostgreSQL server password.
-   \(6\) PostgreSQL server connection string. The following code is an example.

    ```
    jdbc:postgresql://<db_url>:5432/intldsgn_config?currentSchema=systemconfig
    ```

-   \(7\) PostgreSQL username

1.  Create the resource to the cluster in the target namespace.

    ```
    oc apply -n <target namespace> -f intldsgn-secrets.yaml
    ```


## Creating the Helm Values File

1.  Use the provided Helm values template and parameter documentation to create a customized values file to fit your environment requirements.

    See [Helm values](../reference/id_ref_helm_values.md) reference for information on creating a values file. After you create your helm values, you can proceed to deploying with Helm \(client - manual\) or by using ArgoCD.


