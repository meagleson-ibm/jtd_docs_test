# Post data migration steps

When data is migrated, the data is not linked to a team for access control. Use the following steps to assign access permissions to the data.

Create a team and assign associated members to the team. Make sure that at least one Project Administrator user is assigned. See [Team definition](team_definitions.md) and [Keycloak admin client Configuration](keycloak_admin_client.md) for more information.

1.  [Obtain a Bearer token](obtain_bearer_token.md).

2.  [Access the database to get the project ID of deployed data](access_db_proj_id.md).

3.  [Open Access Control Manager Swagger to get the team ID to use](access_crtl_team_id.md).

4.  [Create the access control entity using Swagger](create_access_control_entity.md).


-   **[Obtaining a Bearer token](../../id_docs/installation/obtain_bearer_token.md)**  

-   **[Accessing the database to get the project ID of deployed data](../../id_docs/installation/access_db_proj_id.md)**  
Access the database to get the project ID of deployed data. Services' API, including Swagger, cannot obtain the data, so you must access the DB directly.
-   **[Using Access Control Manager Swagger to get the team ID](../../id_docs/installation/access_crtl_team_id.md)**  
Open Access Control Manager Swagger to get the team ID you want to use.
-   **[Creating the access control entity](../../id_docs/installation/create_access_control_entity.md)**  
Create the access control entity by using the Access Control Manager's Swagger.

