# How to use the service

## Prerequisites

Before using the service, ensure:

1.  **Configuration is Complete**: Service is registered in the [Admin Console](admin/admin_console_overview.md) with all required properties.
2.  **Authentication Token**: You have valid credentials to generate a Bearer token.
3.  **S3 Bucket Access**: \(For migration\) S3 bucket is configured with proper folder structure.

## Authentication

All API calls require a Bearer token. Generate one using:

```
curl -X POST "https://<FQDN>/api/v1/ss/usermgr/user/authenticate" \
  -H "accept: application/json" \
  -H "Content-Type: application/json" \
  -d '{"username":"<USERNAME>","password":"<PASSWORD>"}' -k | jq
```

-   **Response**

    ```
    {
      "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
      "expires_in": 3600
    }
    ```


Save the token value - you'll need it for all subsequent API calls.

-   **[Using the Data Cleanup Service](../id_docs/ids_using_cleanup_svc.md)**  

-   **[Using the Data Migration Service](../id_docs/ids_using_migration_svc.md)**  


**Parent topic:**[IntelliFab Database Service](../id_docs/intellifab_database_svc.md)

