# Creating a ClientID for ID applications

Create a ClientID for the following applications.

For front-end application:

-   Intelligent Design Front End Application
-   Intelligent Design Admin Console Front End Application

For back-end application:

-   Intelligent Design Back End Applications with Application Role
-   Intelligent Design Back End Applications with Application Admin Role

Base URI for Intelligent Design services is defined, URIs are as follows:

|\(M\) Intelligent Design Front End Application|\{Base URI for Intelligent Design\}|
|\(M\) Intelligent Design Admin Console Front End Application|\{Base URI for Intelligent Design\}/console/|
|\(M\) Intelligent Design Back End Applications with Application Role|\{Base URI for Intelligent Design\}|
|\(M\) Intelligent Design Back End Applications with Application Admin Role|\{Base URI for Intelligent Design\}|

Configuration for ClientID creation:

|**Key**|**Value**|
|ClientID|\{ClientID\}|
|Name|\{ClientID\}|
|Description|\{Description\}|
|Root URL|\(M\)|
|Home URL|\(M\)|
|Valid redirect URIs|\(M\)|
|Valid post logout redirect URIs|\(M\)|
|Web origins|\(M\)|
|Client authentication|On|
|Authorization|On|
|Authentication flow|-   Standard flow
-   Direct access grants
-   Implicit flow
-   Service account roles
-   OAuth 2.0 Device Authorization Grant
-   OIDC CIBA Grant

|

Configuration for Client Credentials:

|**Key**|**Value**|
|Client Authenticator|Client Id and Secret|
|Client Secret|\{Client Secret\}|

1.  [Add a ClientID](kc_add_clientid.md).

2.  [Add a Client credential](kc_add_client_cred.md).


-   **[Adding a ClientID](../../id_docs/installation/kc_add_clientid.md)**  

-   **[Adding a Client Credential](../../id_docs/installation/kc_add_client_cred.md)**  
After **Client Authentication** and **Authorization** are turned on during ClientID Creation, each ClientID has a **Credentials** tab.

**Parent topic:**[Configuring Realm of keycloak - Manual](../../id_docs/installation/config_realm_keycloak_manual.md)

