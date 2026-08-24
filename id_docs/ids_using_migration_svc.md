# Using the Data Migration Service

## Loading UserID-Email Mapping

-   **Step 1: Upload Mapping File**

    Upload dmacs\_users\_\*.csv to DATA/IN/NEW/

-   **Step 2: Start Load Job**

    ```
    curl --location 'https://<FQDN>/api/v1/ss/database/loadUserIdEmailMapping' \
      --header 'Authorization: Bearer <YOUR_TOKEN>' | jq
    ```


## Migrating JSON Data \(Testsite, Macros, Devices\)

-   **Step 1: Upload Files to S3**

    Upload your JSON files to the appropriate S3 bucket folders:

    -   Testsite data: DATA/IN/NEW/TESTSITE/
    -   Macro-Device data: DATA/IN/NEW/MACRO\_DEVICE/
-   **Step 2: Start Testsite Migration**

    ```
    curl --location 'https://<FQDN>/api/v1/ss/database/loadLegacyData?data_type=testsite' \
      --header 'Authorization: Bearer <YOUR_TOKEN>' | jq
    ```

-   **Step 3: Check Migration Status**

    ```
    curl --location 'https://<FQDN>/api/v1/ss/database/datamigrationStatus/<process_id>' \
      --header 'Authorization: Bearer <YOUR_TOKEN>' | jq
    ```

-   **Step 4: Start Macros-Devices Migration \(after testsite completes\)**

    ```
    curl --location 'https://<FQDN>/api/v1/ss/database/loadLegacyData?data_type=macros-devices' \
      --header 'Authorization: Bearer <YOUR_TOKEN>' | jq
    ```


## Migrating CSV Data \(Macros and Devices\)

-   **Step 1: Upload CSV Files to S3**

    Upload files to DATA/IN/NEW/:

    -   Macro data: Macro\_<Timestamp\>.csv
    -   Device data: Device\_<Timestamp\>.csv
-   **Step 2: Start CSV Migration**

    ```
    curl --location 'https://<FQDN>/api/v1/ss/database/loadCSVData' \
      --header 'Authorization: Bearer <YOUR_TOKEN>' | jq
    ```

-   **Step 3: Monitor Progress**

    ```
    curl --location 'https://<FQDN>/api/v1/ss/database/datamigrationStatus/<process_id>' \
      --header 'Authorization: Bearer <YOUR_TOKEN>' | jq
    ```


**Parent topic:**[How to use the service](../id_docs/ids_how_to_use.md)

