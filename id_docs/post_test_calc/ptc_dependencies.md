# Dependencies

Dependencies you need to be aware of when installing Post Test Calculation.

|Dependency|Component|Rationale|Provides Datums|
|----------|---------|---------|---------------|
|Random Access POSIX file system|SFTP, Purveyor|Incoming TEDS files shared file system|Target mount point on the PTC SFTP service. On the purveyor, it should be mounted under /opt/idem/ptc-backend.|
|S3 compliant Cloud Object Store|Purveyor, Processor|TEDS file lifecycle management|-   COS Bucket Access key
-   COS Bucket Secret key
-   COS Bucket name
-   COS Endpoint URL
-   COS Bucket Endpoint port

|
|In Memory Database Cluster \(REDIS/VALKEY\)|Purveyor, Processor, Initiator, etc.|Inter-component state persistence for resiliency|-   REDIS/VALKEY Secret
-   REDIS/VALKEY Host name
-   REDIS/VALKEY port

|
|PostgreSQL RDBMS persistence|Test Data Service|TEDS and post calculated data persistence|PostgreSQL connection parameters and credentials|

|Services|Data provided by the dependency|Dependencies provided datum mapping|
|--------|-------------------------------|-----------------------------------|
|Online UI backing service|-   POSTGRES\_SERVER
-   POSTGRES\_PORT
-   POSTGRES\_USER
-   POSTGRES\_PASSWORD
-   POSTGRES\_DB
-   POSTGRES\_DB\_SCHEMA

|PostgreSQL connection parameters and credentials|
|Purveyor|-   REDIS\_HOST
-   REDIS\_PORT
-   REDIS\_SECRET
-   COSBUCKET\_ENDPOINT: str
-   COSBUCKET\_ENDPOINT\_PORT: int
-   COSBUCKET\_ACCESS\_KEY: str
-   COSBUCKET\_SECRET\_KEY: str
-   PURVEYOR\_COS\_BUCKET\_NAME

|-   REDIS/VALKEY Secret
-   REDIS/VALKEY Host name
-   REDIS/VALKEY port
-   COS Bucket Access key
-   COS Bucket Secret Key
-   COS Bucket name

|
|Processor|-   REDIS\_HOST
-   REDIS\_PORT
-   REDIS\_SECRET

|-   REDIS/VALKEY Secret
-   REDIS/VALKEY Host name
-   REDIS/VALKEY port
-   COS Bucket Access key
-   COS Bucket Secret Key
-   COS Bucket name

|
|Delegator|-   REDIS\_HOST
-   REDIS\_PORT
-   REDIS\_SECRET

|-   PostgreSQL connection parameters and credentials
-   REDIS/VALKEY Secret
-   REDIS/VALKEY Host name
-   REDIS/VALKEY port

|
|Initiator|-   REDIS\_HOST
-   REDIS\_PORT
-   REDIS\_SECRET

|-   REDIS/VALKEY Secret
-   REDIS/VALKEY Host name
-   REDIS/VALKEY port

|
|Functor|-   REDIS\_HOST
-   REDIS\_PORT
-   REDIS\_SECRET

|-   REDIS/VALKEY Secret
-   REDIS/VALKEY Host name
-   REDIS/VALKEY port

|

**Parent topic:**[Post Test Calculation design architecture](../../id_docs/post_test_calc/ptc_architecture.md)

