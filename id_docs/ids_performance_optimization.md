# Performance Optimization Tips

1.  **Adjust Batch Size:**
    -   Larger batches \(5000-10000\) for faster processing
    -   Smaller batches \(100-1000\) if running out of memory
2.  **Schedule During Off-Peak Hours:**
    -   Run cleanup jobs when database load is low
    -   Avoid running during business hours
3.  **Monitor Database Resources:**
    -   *-- Check database size*
    -   SELECT pg\_size\_pretty\(pg\_database\_size\(current\_database\(\)\)\);
    -       -   *-- Check table sizes*
    -   SELECT schemaname, tablename,
    -   pg\_size\_pretty\(pg\_total\_relation\_size\(schemaname\|\|'.'\|\|tablename\)\)
    -   FROM pg\_tables
    -   WHERE schemaname = '<schema\_name\>'
    -   ORDER BY pg\_total\_relation\_size\(schemaname\|\|'.'\|\|tablename\) DESC;

**Parent topic:**[Troubleshooting](../id_docs/ids_troubleshooting.md)

