# Monitoring Your Cleanup Jobs

## Understanding Job Statuses

|Status|Description|What to Do|
|------|-----------|----------|
|queued|Job is waiting to start.|Wait - it will start automatically.|
|processing|Job is currently running.|Monitor progress by checking status periodically.|
|completed|Job finished successfully.|Review cleanup logs for details.|
|failed|Job encountered an error.|Check error logs and troubleshooting guide.|

## Checking Process Logs Directly

You can also query the database directly:

-   Check current status:

    ```
    SELECT processid, processname, status, starttime, endtime, error
    FROM <schema_name>.processlog
    WHERE processid = '<your_process_id>';
    ```

-   View all recent cleanup jobs:

    ```
    SELECT processid, processname, status, starttime, endtime
    FROM <schema_name>.processlog
    WHERE processname = 'cleanup'
    ORDER BY starttime DESC
    LIMIT 10;
    ```


**Parent topic:**[IntelliFab Database Service](../id_docs/intellifab_database_svc.md)

