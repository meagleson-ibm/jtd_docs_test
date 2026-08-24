# Defining Session timeouts

Ensure the following tool addresses are provided.

|Tool name|URL|
|---------|---|
|Keycloak Admin Console||
|ID Admin Console||
|Backend Swagger \(unified portal\)||

**Defining Session timeouts**

Keycloak sessions are maintained in a browser cookie that is created after login and destroyed after logout. However, you can define an implicit session timeout period to renew a session after a certain period of time. The session timeout period is defined in three parameters as shown in the following table.

|**Config name**|**Keycloak config**|**Default value**|
|Session timeout|SSO Session Max|1 Day \(24 hours\)|
|ID token|Access Token Life Span|12 hours \(Equal to Config Map/ `ID_BT_MAXAGE`\)|
|Refresh token|SSO Session Idle|1 Day \(24 hours\)|

1.  Log into the Keycloak Admin console and select the target realm in the navigation pane.

2.  Navigate to **Realm settings**.

3.  For each Keycloak config setting, navigate to the following paths:

    1.  To set the SSO Session Max, navigate to **Sessions** \> **SSO Session Settings** \> **SSO Session Max**.

    2.  To set the Access Token Life Span, navigate to **Tokens** \> **Access tokens** \> **Access Token Lifespan**.

    3.  To set the SSO Session Idle, navigate to **Sessions** \> **SSO Session Settings** \> **SSO Session Idle**.


