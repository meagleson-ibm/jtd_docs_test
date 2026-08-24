# Data Setup

-   **Registering Config Services**

    You can register and configure services using the [Admin Console](../admin/admin_console_overview.md).


1.  Remove the services and datadeployment for the following services as these services are merged in one service \(database-svc\).

    -   dataretention-svc
    -   datamigration-svc
2.  JSON format \(Sample JSON for ptc\) The JSON format should follow the below structure. This is the example of ptc data cleanup.

    ```
    [{
            "table": "appattemptlistreports",
            "parents": [{
                    "parent": "appreports",
                    "fk_column": "appfk"
                }
            ]
        }, {
            "table": "appcontactlistreports",
            "parents": [{
                    "parent": "appattemptlistreports",
                    "fk_column": "appfk"
                }
            ]
        }, {
            "table": "apptesterchannelsreports",
            "parents": [{
                    "parent": "appreports",
                    "fk_column": "appfk"
                }
            ]
        }, {
            "table": "arraydatareports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "atsureports",
            "parents": [{
                    "parent": "sublotreports",
                    "fk_column": "subfk"
                }
            ]
        }, {
            "table": "arrayinstancedefinition",
            "parents": [{
                    "parent": "arraydefinitionsreports",
                    "fk_column": "adeffk"
                }
            ]
        }, {
            "table": "binfreports",
            "parents": [{
                    "parent": "sublotreports",
                    "fk_column": "subfk"
                }
            ]
        }, {
            "table": "blockdatasets",
            "parents": [{
                    "parent": "fbreports",
                    "fk_column": "fbfk"
                }, {
                    "parent": "fbsreports",
                    "fk_column": "fbsfk"
                }
            ]
        }, {
            "table": "buildinformationreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }, {
                    "parent": "sublotreports",
                    "fk_column": "subfk"
                }
            ]
        }, {
            "table": "conditionreferencereports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "conditionsets",
            "parents": [{
                    "parent": "conditionreports",
                    "fk_column": "condfk"
                }
            ]
        }, {
            "table": "contextdefinitions",
            "parents": [{
                    "parent": "cntxreports",
                    "fk_column": "cntxfk"
                }
            ]
        }, {
            "table": "eblreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "ecidreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "devicereports",
            "parents": [{
                    "parent": "sublotreports",
                    "fk_column": "subfk"
                }
            ]
        }, {
            "table": "ecvlreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "imgireports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "fbsreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "endlotreports",
            "parents": [{
                    "parent": "lotreports",
                    "fk_column": "lotfk"
                }
            ]
        }, {
            "table": "fbreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "fwreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "lotreports",
            "parents": [{
                    "parent": "cntlreports",
                    "fk_column": "cntlfk"
                }
            ]
        }, {
            "table": "inforeports",
            "parents": [{
                    "parent": "lotreports",
                    "fk_column": "lotfk"
                }
            ]
        }, {
            "table": "operreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "pinsets",
            "parents": [{
                    "parent": "fwreports",
                    "fk_column": "fwfk"
                }
            ]
        }, {
            "table": "pbreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "ppreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "prreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "ruleinstances",
            "parents": [{
                    "parent": "atsureports",
                    "fk_column": "atsufk"
                }
            ]
        }, {
            "table": "rulesets",
            "parents": [{
                    "parent": "atsureports",
                    "fk_column": "atsufk"
                }
            ]
        }, {
            "table": "pnrdirectivesreports",
            "parents": [{
                    "parent": "cntlreports",
                    "fk_column": "cntlfk"
                }
            ]
        }, {
            "table": "sdefreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "sdrreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "setupattachmentreports",
            "parents": [{
                    "parent": "setupreports",
                    "fk_column": "setupreportfk"
                }
            ]
        }, {
            "table": "sortreports",
            "parents": [{
                    "parent": "sublotreports",
                    "fk_column": "subfk"
                }
            ]
        }, {
            "table": "setupreports",
            "parents": [{
                    "parent": "lotreports",
                    "fk_column": "lotfk"
                }
            ]
        }, {
            "table": "telemetry",
            "parents": []
        }, {
            "table": "threports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "ssrtreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "testexecutionreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "testoutput",
            "parents": []
        }, {
            "table": "testmodes",
            "parents": [{
                    "parent": "pinreports",
                    "fk_column": "pinfk"
                }
            ]
        }, {
            "table": "syldrreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "stringreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "adaptivetesteventreports",
            "parents": [{
                    "parent": "sublotreports",
                    "fk_column": "subfk"
                }
            ]
        }, {
            "table": "adaptivetestperformancesummaryreports",
            "parents": [{
                    "parent": "endsublotreports",
                    "fk_column": "esubfk"
                }
            ]
        }, {
            "table": "addresssets",
            "parents": [{
                    "parent": "fdreports",
                    "fk_column": "fdfk"
                }
            ]
        }, {
            "table": "appreports",
            "parents": [{
                    "parent": "setupreports",
                    "fk_column": "setfk"
                }, {
                    "parent": "sublotreports",
                    "fk_column": "subfk"
                }
            ]
        }, {
            "table": "arraydefinitionsreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "chreports",
            "parents": [{
                    "parent": "sublotreports",
                    "fk_column": "subfk"
                }
            ]
        }, {
            "table": "cmprreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "cntlreports",
            "parents": [{
                    "parent": "tedsinput",
                    "fk_column": "tedsinputmodelfk"
                }
            ]
        }, {
            "table": "cntxreports",
            "parents": [{
                    "parent": "lotreports",
                    "fk_column": "lotfk"
                }
            ]
        }, {
            "table": "conditionreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "waferaggregate",
            "parents": [{
                    "parent": "tedsinput",
                    "fk_column": "tedsinputmodelfk"
                }
            ]
        }, {
            "table": "enddevicereports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "endsublotreports",
            "parents": [{
                    "parent": "sublotreports",
                    "fk_column": "subfk"
                }
            ]
        }, {
            "table": "fdreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "parameterx",
            "parents": [{
                    "parent": "adaptivetesteventreports",
                    "fk_column": "atevfk"
                }
            ]
        }, {
            "table": "pinreports",
            "parents": [{
                    "parent": "sublotreports",
                    "fk_column": "subfk"
                }
            ]
        }, {
            "table": "setupfehreports",
            "parents": [{
                    "parent": "setupreports",
                    "fk_column": "setfk"
                }, {
                    "parent": "sublotreports",
                    "fk_column": "subfk"
                }
            ]
        }, {
            "table": "sprmrreports",
            "parents": [{
                    "parent": "devicereports",
                    "fk_column": "devfk"
                }
            ]
        }, {
            "table": "sublotreports",
            "parents": [{
                    "parent": "lotreports",
                    "fk_column": "lotfk"
                }
            ]
        }, {
            "table": "tedsinput",
            "parents": [{
                    "parent": "testoutput",
                    "fk_column": "testoutputmodelfk"
                }
            ]
        }
    ]
    
    ```

3.  Dependency JSON generator query: Update the sql "Dependency\_JSON\_Generator\_Query.sql" to adjust the schema and tables list which to be considered for deletion. This sql query is in this repository.

4.  Encode the JSON with base64.

    |Name|Description|Param URL \(adjust to your environment\)|
    |----|-----------|----------------------------------------|
    |Database cleanup and migration process|Data Migration and Cleanup Data Configuration|jdbc:postgresql://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn?currentSchema=intdsgndata|

    |Name|Service Type|Description|
    |----|------------|-----------|
    |database-svc|Application|Database Service|

    -   **Adding Deployment**

        ```
            label: 1.0
            profile: UAT, (Set your keyword.)
            status: Active
            servicecontext: /api/v1/ss/database
            internalurl: (Set your internal url)
            externalurl: (Set your external url)
            use datasource: True
            securityon: True
        
        ```

    |Properties Name|Value|
    |---------------|-----|
    |BATCH\_SIZE|Set the batch size \(e.g., 100, 1000, 5000\).|
    |RETENTION\_DAYS|Set number of days based on the retention policy.|
    |DEPENDENCY\_JSON|Set the Base64 encode of the JSON.|
    |SCHEMA\_NAME|Set the schema name from where the data will be purged.|
    |NEW\_FILE\_BASE\_PATH|DATA/IN/NEW/|
    |PROCESSED\_FILE\_BASE\_PATH|DATA/IN/PROCESSED/|
    |S3\_BUCKET|Replace with your bucket name.|
    |S3\_ACCESS\_KEY\_ID|Replace with your S3 access key ID.|
    |S3\_ENDPOINT\_URL|Replace with your S3 endpoint URL.|
    |S3\_SECRET\_ACCESS\_KEY|Replace with your S3 secret access key.|
    |SERVER\_PORT|7003|

    -   **Select Datasource:**

        Database cleanup and migration process.


**Parent topic:**[intellifab-database-service](../../id_docs/installation/intellifab_db_svc.md)

