# Loading UserID-Email Mapping

1.  Upload Legacy csv Data Files:

    Upload dmacs\_users\_\*.csv to DATA/IN/NEW/

2.  Execute data loading using API:

    Using Curl command:

    -   Generate the Bearer Token by executing the following curl command:

        ```
        curl -X POST "https://<FQDN>/api/v1/ss/usermgr/user/authenticate" \
          -H "accept: application/json" -H "Content-Type: application/json" \
          -d "{\"username\":\"<USERNAME>\",\"password\":\"<PASSWORD>\"}" -k | jq
        
        ```

    -   Execute the UserID-Email job with the following curl command:

        ```
        curl --location 'https://<FQDN>/api/v1/ss/database/loadUserIdEmailMapping' \
          --header 'Authorization: Bearer <TOKEN>' | jq
        
        ```


**Parent topic:**[Data Migration Process](../../id_docs/installation/ifds_data_migration_proc.md)

