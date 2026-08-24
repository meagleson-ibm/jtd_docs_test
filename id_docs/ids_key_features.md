# Key features

## Automated Data Cleanup

-   **Retention Policy-Based**: Automatically deletes data older than your configured retention period \(e.g., 90 days, 180 days\).
-   **Date-Based Processing**: Processes deletions by date, allowing for controlled, incremental cleanup.
-   **Transaction Safety**: Each date is processed in its own transaction - if one fails, others continue.

## Comprehensive Logging

-   **Cleanup Logs**: Tracks how many records were deleted from each table.
-   **Error Logs**: Captures any issues encountered during deletion with full context.
-   **Process Tracking**: Monitor job status in real-time through the processlog table.

## Safe & Reliable

-   **Two-Stage Process**:
    1.  **Pre-clean Stage**: Identifies and stages all records to be deleted.
    2.  **Deletion Stage**: Performs actual deletions in the correct order.
-   **Batch Processing**: Handles large datasets efficiently, using configurable batch sizes.
-   **Rollback Protection**: Failed operations are rolled back, leaving your data consistent.

## Flexible Data Migration

-   **Multiple Data Formats**: Supports JSON and CSV file formats.
-   **S3 Integration**: Automatically processes files from S3 buckets.
-   **File Management**: Moves processed files to separate folders for tracking.

## RESTful API

-   **Background Processing**: Jobs run asynchronously, so you get immediate responses.
-   **Status Monitoring**: Check job progress at any time using the process ID.
-   **Swagger Documentation**: Interactive API documentation at /api/v1/ss/database/docs.

**Parent topic:**[IntelliFab Database Service](../id_docs/intellifab_database_svc.md)

