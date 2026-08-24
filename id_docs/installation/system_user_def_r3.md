# System User definition

Ensure the following tool addresses are provided.

|Tool name|URL|
|---------|---|
|Keycloak Admin Console||
|ID Admin Console||
|Backend Swagger \(unified portal\)||

## Creating System Users and Assigning them to a role

The backend services require 2 system users: one for EDA integration and another for intra-backend integration.

|`Username`|`firstName`|`lastName`|`email`|`Password`|`Role`|
|----------|-----------|----------|-------|----------|------|
|eda|eda system user|eda system user|eda@example.com|passw0rd|IntegrationRead|
|backendservice|backendservice|integration|backendservice@example.com|passw0rd|N/A|

1.  Create Role “IntegrationRead” and “IntegrationWrite” in Keycloak.

2.  Create user “eda” and assign to “IntegrationRead”.

3.  Create user “backendservice” and do not assign a role.

    **Note:** The “IntegrationWrite” role will be used in future updates.


