# Best Practices

## For Data Cleanup

1.  **Test First:** Run cleanup on a test environment before production
2.  **Monitor Regularly:** Check cleanup logs after each run
3.  **Backup Before Cleanup:** Ensure database backups are current
4.  **Review Retention Policy:** Periodically verify retention period is appropriate
5.  **Schedule Consistently:** Run cleanup jobs on a regular schedule \(weekly/monthly\)

## For Data Migration

1.  **Validate Files:** Check file format and content before uploading
2.  **Process in Order:** Complete testsite migration before macros-devices
3.  **Monitor S3 Usage:** Regularly clean up processed files
4.  **Keep Logs:** Retain migration logs for audit purposes
5.  **Test Mappings:** Verify UserID-Email mappings are correct

**Parent topic:**[Troubleshooting](../id_docs/ids_troubleshooting.md)

