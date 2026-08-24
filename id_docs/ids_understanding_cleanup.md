# Understanding the Cleanup Process

## Two-Stage Cleanup Architecture

The cleanup process uses a sophisticated two-stage approach:

-   **Stage 1: Pre-Clean \(Identification & Staging\)**

    -   Identifies all records older than retention period
    -   Builds a complete dependency graph
    -   Stages IDs in temporary tables \(temp\_delete\_ids, temp\_frontier\_ids\)
    -   Propagates through relationships to find all dependent records
    -   Uses topological sorting to determine deletion order
-   **Stage 2: Deletion \(Actual Removal\)**

    -   Deletes records in child→parent order
    -   Processes in configurable batches
    -   Maintains transaction safety
    -   Logs all deletions
    -   Cleans up staging tables

## Why this approach?

1.  **Safety:** Identifies all records before deleting anything
2.  **Integrity:** Respects foreign key relationships
3.  **Resumability:** Can recover from failures
4.  **Transparency:** Clear logging of what will be deleted
5.  **Performance:** Batch processing for large datasets

For the latest updates and additional documentation, visit the project repository.

**Parent topic:**[IntelliFab Database Service](../id_docs/intellifab_database_svc.md)

