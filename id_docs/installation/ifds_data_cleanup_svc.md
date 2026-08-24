# intellifab-data-cleanup-service

Purpose: To cleanup the data based on the retention policy configured.

## Execute data cleanup using API:

-   **Using Curl command:**

    -   Generate Bearer Token by executing below curl command:

        ```
        curl -X POST "https://<FQDN>/api/v1/ss/usermgr/user/authenticate" \
          -H "accept: application/json" -H "Content-Type: application/json" \
          -d "{\"username\":\"<USERNAME>\",\"password\":\"<PASSWORD>\"}" -k | jq
        
        ```

    -   Execute the datacleanup job by using the following curl command:

        ```
        curl --location 'https://<FQDN>/api/v1/ss/database/cleanData' \
          --header 'Authorization: Bearer <TOKEN>' | jq
        
        ```

    -   To see the status of the job, execute the following curl command:

        ```
        curl --location 'https://<FQDN>/api/v1/ss/database/cleanupStatus/<processid>' \
          --header 'Authorization: Bearer <TOKEN>' | jq
        
        ```

-   **Swagger:**

    Swagger URL: < FQDN \>/api/v1/ss/database/docs


**Parent topic:**[intellifab-database-service](../../id_docs/installation/intellifab_db_svc.md)

