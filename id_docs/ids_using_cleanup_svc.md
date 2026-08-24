# Using the Data Cleanup Service

## Step 1: Start a Cleanup Job

Execute the cleanup job using the API:

```
curl --location 'https://<FQDN>/api/v1/ss/database/cleanData' \
  --header 'Authorization: Bearer <YOUR_TOKEN>' | jq
```

-   **Response:**

    ```
    {
      "process_id": "a1b2c3d4-e5f6-7890-abcd-ef1234567890",
      "process_name": "cleanup",
      "message": "Cleanup pipeline (with mandatory preclean) started"
    }
    ```


**Important:** Save the process\_id - you'll need it to check the job status.

## Step 2: Monitor Job Progress

Check the status of your cleanup job:

```
curl --location 'https://<FQDN>/api/v1/ss/database/cleanupStatus/<process_id>' \
  --header 'Authorization: Bearer <YOUR_TOKEN>' | jq
```

-   **Response \(in progress\):**

    ```
    {
      "processid": "a1b2c3d4-e5f6-7890-abcd-ef1234567890",
      "processname": "cleanup",
      "status": "processing",
      "starttime": "2026-06-19T03:30:00.000Z",
      "endtime": null,
      "stdout": null,
      "stderr": null,
      "error": null
    }
    ```

-   **Response \(completed\):**

    ```
    {
      "processid": "a1b2c3d4-e5f6-7890-abcd-ef1234567890",
      "processname": "cleanup",
      "status": "completed",
      "starttime": "2026-06-19T03:30:00.000Z",
      "endtime": "2026-06-19T03:45:00.000Z",
      "stdout": "Cleanup completed successfully. Total records deleted: 15,234",
      "stderr": null,
      "error": null
    }
    ```


**Important:** Save the process\_id - you'll need it to check the job status.

**Parent topic:**[How to use the service](../id_docs/ids_how_to_use.md)

