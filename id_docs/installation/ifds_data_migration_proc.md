# Data Migration Process

Purpose: To migrate legacy data into the Intelligent Design Database when required.

-   **Objectives:**

    The following content outlines the prerequisites and step-by-step procedures for migrating legacy data.

-   **JSON Data File Loads:**

    -   testsite
    -   macros
    -   devices
    -   Associated attachments
-   **CSV Data File Loads:**

    -   macros
    -   devices
-   **Prerequisite**

    1.  S3 Bucket
        1.  Create an object bucket claim named “database-services” via OpenShift console.
        2.  Connect to Object Storage bucket “database-services” using any S3 compatible terminal. \(e.g., MinIO client\). `./mc.exe alias set <ALIAS-NAME> <S3 BUCKET ENDPOINT URL> <ACCESS KEY> <SECRET KEY>`
        3.  Create the following folder structure in S3 bucket:

            ```
            DATA/
                  └── IN/
                 ├── NEW/
                 │          ├── TESTSITE/     # Stores testsite JSON files from legacy system
                 │           └── MACRO_DEVICE/ # Stores macro-device JSON files from legacy
                 └── PROCESSED/
                             ├── TESTSITE/         # Stores processed testsite files
                              └── MACRO_DEVICE/     # Stores processed macro-device files
            
            ```


-   **[Loading UserID-Email Mapping](../../id_docs/installation/ifds_load_uid_email_map.md)**  

-   **[Data Migration Steps to follow for source JSON data files](../../id_docs/installation/ifds_json_data_files.md)**  

-   **[Data Migration Steps to follow for source CSV data files](../../id_docs/installation/ifds_source_csv_data_files.md)**  


**Parent topic:**[intellifab-database-service](../../id_docs/installation/intellifab_db_svc.md)

