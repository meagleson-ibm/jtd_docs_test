# Configuration Reference

|**Property**|**Description**|**Example**|
|------------|---------------|-----------|
|RETENTION\_DAYS|Number of days to retain data|90|
|BATCH\_SIZE|Records per batch for deletion|5000|
|SCHEMA\_NAME|Database schema for cleanup|ptc|
|DEPENDENCY\_JSON|Base64-encoded table dependency JSON|\(base64 string\)|
|S3\_BUCKET|S3 bucket name|database-services|
|S3\_ENDPOINT\_URL|S3 endpoint URL|[https://s3.example.com](https://s3.example.com/)|
|S3\_ACCESS\_KEY\_ID|S3 access key|\(secret\)|
|S3\_SECRET\_ACCESS\_KEY|S3 secret key|\(secret\)|
|NEW\_FILE\_BASE\_PATH|Path for new files|DATA/IN/NEW/|
|PROCESSED\_FILE\_BASE\_PATH|Path for processed files|DATA/IN/PROCESSED/|
|SERVER\_PORT|Service port|7003|

**Parent topic:**[Troubleshooting](../id_docs/ids_troubleshooting.md)

