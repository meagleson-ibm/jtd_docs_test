# API Reference Summary

|Endpoint|Method|Purpose|Process Name|
|--------|------|-------|------------|
|/api/v1/ss/database/cleanData|GET|Start data cleanup job|cleanup|
|/api/v1/ss/database/cleanupStatus/\{process\_id\}|GET|Check cleanup job status|-|
|/api/v1/ss/database/loadLegacyData?data\_type=\{type\}|GET|Load JSON data \(testsite or macros-devices\)|legacy:\{type\}|
|/api/v1/ss/database/loadCSVData|GET|Load CSV data|csv|
|/api/v1/ss/database/loadUserIdEmailMapping|GET|Load UserID-Email mapping|userid-email|
|/api/v1/ss/database/datamigrationStatus/\{process\_id\}|GET|Check migration job status|-|

**Parent topic:**[Troubleshooting](../id_docs/ids_troubleshooting.md)

