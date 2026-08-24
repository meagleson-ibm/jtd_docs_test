# Data Migration Steps to follow for source JSON data files

1.  Upload Legacy JSON Data Files:

    -   Copy/Upload testsite data JSON files from legacy system in S3 Bucket under folder DATA/IN/NEW/TESTSITE/
    -   Copy/Upload macro-device data JSON files from legacy system in S3 Bucket under folder DATA/IN/NEW/MACRO\_DEVICE/
2.  Execute Datamigration using API:

    Using Curl command:

    -   Generate the Bearer Token by executing the following curl command:

        ```
        curl -X POST "https://<FQDN>/api/v1/ss/usermgr/user/authenticate" \
          -H "accept: application/json" -H "Content-Type: application/json" \
          -d "{\"username\":\"<USERNAME>\",\"password\":\"<PASSWORD>\"}" -k | jq
        
        ```

    -   Execute the testsite job with the following curl command:

        ```
        curl --location 'https://<FQDN>/api/v1/ss/database/loadLegacyData?data_type=testsite' \
          --header 'Authorization: Bearer <TOKEN>' | jq
        
        ```

    -   To see the status of the job, execute the following curl command:

        ```
        curl --location 'https://<FQDN>/api/v1/ss/database/datamigrationStatus/<processid>' \
          --header 'Authorization: Bearer <TOKEN>' | jq
        
        ```

    -   After the testsite data migration job status is completed, proceed with macros-devices data migration by executing the following curl command:

        ```
        curl --location 'https://<FQDN>/api/v1/ss/database/loadLegacyData?data_type=macros-devices' \
          --header 'Authorization: Bearer <TOKEN>' | jq
        
        ```

    -   To see the status of the job, execute the following curl command:

        ```
        curl --location 'https://<FQDN>/api/v1/ss/database/datamigrationStatus/<processid>' \
          --header 'Authorization: Bearer <TOKEN>' | jq
        
        ```


**Parent topic:**[Data Migration Process](../../id_docs/installation/ifds_data_migration_proc.md)

