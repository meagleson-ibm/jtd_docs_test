# Keycloak admin client Configuration

Ensure the following tool addresses are provided.

|Tool name|URL|
|---------|---|
|Keycloak Admin Console||
|ID Admin Console||
|Backend Swagger \(unified portal\)||

## Configuring Keycloak admin-cli

The backend services require 2 system users: one for EDA integration and another for intra-backend integration.

|`Username`|`firstName`|`lastName`|`email`|`Password`|`Role`|
|----------|-----------|----------|-------|----------|------|
|eda|eda system user|eda system user|eda@example.com|passw0rd|IntegrationRead|
|backendservice|backendservice|integration|backendservice@example.com|passw0rd|N/A|

1.  Log in into the Keycloak Admin console and select the target realm in the navigation pane.

2.  Click **Clients**.

3.  Click **admin-cli**.

4.  Select the **Client scopes**tab and click **admin-cli-dedicated**.

5.  Select the **Scope** tab, and enable **Full scope allowed**.

    **Note:** There is no **Save** button. The change is affected immediately.


