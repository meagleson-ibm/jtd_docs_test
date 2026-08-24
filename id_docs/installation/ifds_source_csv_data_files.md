# Data Migration Steps to follow for source CSV data files

The .csv data loading is only for macro and device. The .csv file name should start with Macro for macro data and Device for device data \(e.g., Macro\_.csv and Device\_.csv.

1.  Upload .csv Data Files for Macro and Device:

    Copy/Upload Macro\_<Timestamp\>.csv and Device\_<Timestamp\>.csv data files in S3 Bucket under folder DATA/IN/NEW/

2.  Execute Datamigration using API:

    Using Curl command:

    -   Generate the Bearer Token by executing the following curl command:

        ```
        curl -X POST "https://<FQDN>/api/v1/ss/usermgr/user/authenticate" \
          -H "accept: application/json" -H "Content-Type: application/json" \
          -d "{\"username\":\"<USERNAME>\",\"password\":\"<PASSWORD>\"}" -k | jq
        
        ```

    -   Execute the CSV Data load job with the following curl command:

        ```
        curl --location 'https://<FQDN>/api/v1/ss/database/loadCSVData' \
          --header 'Authorization: Bearer <TOKEN>' | jq
        
        ```

    -   To see the status of the job, execute the following curl command:

        ```
        curl --location 'https://<FQDN>/api/v1/ss/database/datamigrationStatus/<processid>' \
          --header 'Authorization: Bearer <TOKEN>' | jq
        
        ```


**Parent topic:**[Data Migration Process](../../id_docs/installation/ifds_data_migration_proc.md)

