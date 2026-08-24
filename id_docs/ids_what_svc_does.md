# What This Service Does

The IntelliFab Database Service is a unified FastAPI-based backend that consolidates two critical database operations.

## 1. Data Migration Service

Migrates legacy data into the Intelligent Design Database, supporting:

-   **JSON Data Files**: Testsite, macros, devices, and associated attachments
-   **CSV Data Files**: Macro and device data****
-   **UserID-Email Mapping**: CSV-based user mapping data

## 2. Data Cleanup Service

Automatically removes old data based on your organization's retention policy:

-   Identifies records older than the configured retention period
-   Safely deletes data while respecting foreign key relationships
-   Processes deletions in dependency order \(children first, then parents\)
-   Maintains referential integrity throughout the cleanup process

**Why This Matters**: This consolidated service eliminates duplicate configuration, reduces maintenance overhead, and provides a single entry point for all database operations.

**Parent topic:**[IntelliFab Database Service](../id_docs/intellifab_database_svc.md)

