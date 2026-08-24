# Common Issues and Solutions

## Issue 1: Job Status Shows "Failed"

-   **Symptoms:**

    ```
    {
      "status": "failed",
      "error": "Cleanup exit code 1"
    }
    ```

-   **Solutions:**

    1.  **Check Error Logs:**
        -   SELECT \* FROM <schema\_name\>.errorlog
        -   WHERE createddate \> NOW\(\) - INTERVAL '1 hour'
        -   ORDER BY createddate DESC;
    2.  **Review Process Log Details:**
        -   SELECT stdout, stderr, error
        -   FROM <schema\_name\>.processlog
        -   WHERE processid = '<your\_process\_id\>';
    3.  **Common Causes:**
        -   Database connection timeout → Increase connection timeout settings
        -   Foreign key violations → Check dependency JSON configuration
        -   Out of memory → Reduce BATCH\_SIZE in configuration

## Issue 2: Job Stuck in "Processing" Status

-   **Symptoms:**

    -   Status remains "processing" for hours
    -   No updates to cleanup logs
-   **Solutions:**

    1.  **Check Database Locks:**
        -   SELECT pid, usename, application\_name, state, query
        -   FROM pg\_stat\_activity
        -   WHERE state = 'active' AND query LIKE '%DELETE%';
    2.  **Review Application Logs:**
        -   Check container/pod logs for the database service
        -   Look for timeout or connection errors
    3.  **If Necessary, Cancel the Job:**
        -   *-- Find the backend process*
        -   SELECT pg\_cancel\_backend\(pid\)
        -   FROM pg\_stat\_activity
        -   WHERE application\_name = 'database-service';

## Issue 3: No Records Being Deleted

-   **Symptoms:**

    -   Job completes successfully
    -   All deletion counts are zero
-   **Possible causes:**

    1.  **No Old Data:** Records may not be older than retention period
        -   *-- Check oldest records*
        -   SELECT MIN\(createdate\) as oldest\_record
        -   FROM <schema\_name\>.lotreports;
    2.  **Incorrect Retention Configuration:**
        -   Verify RETENTION\_DAYS in deployment properties
        -   Check that createdate column exists and is populated
    3.  **Schema Mismatch:**
        -   Verify SCHEMA\_NAME matches your actual schema
        -   Check that tables exist in the specified schema

## Issue 4: Foreign Key Violations

-   **Symptoms:**

    Error: update or delete on table "parent\_table" violates foreign key constraint.

-   **Solutions:**

    1.  **Verify Dependency JSON:**
        -   Ensure all parent-child relationships are correctly defined
        -   Check that fk\_column names match actual foreign key columns
    2.  **Regenerate Dependency JSON:**
        -   *-- Run the Dependency\_JSON\_Generator\_Query.sql*
        -   *-- Update the DEPENDENCY\_JSON property with new base64-encoded result*
    3.  **Check for Orphaned Records:**
        -   *-- Find child records without parents*
        -   SELECT c.id
        -   FROM <schema\_name\>.child\_table c
        -   LEFT JOIN <schema\_name\>.parent\_table p ON c.parent\_fk = p.id
        -   WHERE p.id IS NULL;

## Issue 5: Authentication Errors

-   **Symptoms:**

    ```
    {
      "detail": "Not authenticated",
      "error_code": "UNAUTHORIZED"
    }
    ```

-   **Solutions:**

    1.  **Token Expired:** Generate a new token
    2.  **Invalid Token:** Check that you copied the complete token string
    3.  **Wrong Endpoint:** Verify you're using the correct FQDN

## Issue 6: S3 Connection Errors \(Migration\)

-   **Symptoms:**

    -   Migration job fails immediately
    -   Error mentions S3 or bucket access
-   **Solutions:**

    1.  **Verify S3 Configuration:**
        -   Check S3\_ENDPOINT\_URL, S3\_ACCESS\_KEY\_ID, S3\_SECRET\_ACCESS\_KEY
        -   Ensure bucket name is correct
    2.  **Check File Paths:**
        -   Verify files are in correct folders \(DATA/IN/NEW/TESTSITE/, etc.\)
        -   Ensure file naming conventions are followed
    3.  **Test S3 Connectivity:**
        -   *\# Using MinIO client*
        -   ./mc.exe ls <ALIAS-NAME\>/database-services/DATA/IN/NEW/

**Parent topic:**[Troubleshooting](../id_docs/ids_troubleshooting.md)

