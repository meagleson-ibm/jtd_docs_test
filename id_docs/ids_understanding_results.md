# Understanding the Results

-   **Cleanup Logs**

    After a successful cleanup, review the cleanuplog table to see what was deleted:

    ```
    SELECT * 
    FROM <schema_name>.cleanuplog
    ORDER BY createddate DESC
    LIMIT 50;
    
    ```

-   **Sample Output:**

    ```
    | id | logentry                                                          | createddate         |
    |----|-------------------------------------------------------------------|---------------------|
    | 1  | {"schema_name":"ptc","table":"devicereports","deleted_count":523} | 2026-06-19 03:45:00 |
    | 2  | {"schema_name":"ptc","table":"sublotreports","deleted_count":89}  | 2026-06-19 03:45:00 |
    | 3  | {"schema_name":"ptc","table":"lotreports","deleted_count":12}     | 2026-06-19 03:45:00 |
    
    ```

-   **Key Information:**

    -   **schema\_name**: Which database schema was cleaned.
    -   **table**: Which table had records deleted.
    -   **deleted\_count**: How many records were removed.
    -   **timestamp**: When the deletion occurred.
-   **Error Logs**

    If issues occurred, check the errorlog table:

    ```
    SELECT * 
    FROM <schema_name>.errorlog
    ORDER BY createddate DESC
    LIMIT 20;
    ```

-   **Sample Output:**

    ```
    | id | stepname              | filename                    | errormessage                          | createddate         |
    |----|-----------------------|-----------------------------|---------------------------------------|---------------------|
    | 1  | perform_deletions     | datacleanup_helper.py       | Foreign key violation on table X      | 2026-06-19 03:40:00 |
    | 2  | process_date_2026-03-15| preclean_stage_inputs.py   | Connection timeout during propagation | 2026-06-19 03:35:00 |
    ```

-   **Key Information:**

    -   **stepname**: Which operation failed.
    -   **filename**: Which script encountered the error.
    -   **errormessage**: Detailed error description.
    -   **createddate**: When the error occurred.

## Interpreting Deletion Counts

-   **Normal Patterns:**

    -   Child tables typically have higher deletion counts than parent tables.
    -   Deletion counts should align with your retention policy.
    -   Zero deletions for a table means no old records existed.
-   **Warning Signs:**

    -   Unexpectedly low deletion counts \(may indicate data not being captured\).
    -   Very high deletion counts \(verify retention policy is correct\).
    -   Deletions in parent tables but not child tables \(may indicate orphaned records\).

**Parent topic:**[IntelliFab Database Service](../id_docs/intellifab_database_svc.md)

