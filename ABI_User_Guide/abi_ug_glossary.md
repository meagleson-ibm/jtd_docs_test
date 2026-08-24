# Glossary of terms

-   **Bank**

    A bank in the semiconductor manufacturing process is a place to release, prepare for shipment, or hold product.


-   **BASIS**

    The Basis feature captures all the parameters that are identified during the configuration of ABI Reports. This section represents the WHERE clause in the SQL submitted to Data Warehouse. Report Parameters identify what you want to track during the semiconductor manufacturing process. For example, you might want to track specific Lot IDs and their status, wafers within a Lot, and the equipment \(tools\) used during wafer manufacturing.

    When viewing Reports, you can select the Basis to view configuration parameters that are used to generate the report. See [Reviewing WIP Reports Results](abi_ug_wip_reports_results.md).


-   **CDF**

    CDF stands for Cumulative Distribution Function. In probability theory and statistics, the cumulative distribution function \(CDF\) of a real-valued random variable. ABI supports CDF charts.


-   **Data View**

    A view of a data table that can be customized to present a subset of data from a data table. It contains metadata and instructions for receiving data but it does not store the data values.


-   **Data Warehouse**

    The Data Warehouse \(Data Warehouse\), is a complex star schema database that is designed and built with IBM Db2® technologies. The star schemas consist of FACT tables that are associated with DIMENSION \(DIM\) tables in a star format. FACT tables hold measurable, quantitative data about processes and are associated with specific DIM tables that contain attributes \(reference information\) about the data in the FACT tables.


-   **Dataset**

    Abstraction of a query on a data source. A dataset contains both the metadata and the data values. A dataset can use physical, virtual, and custom resolvers to access the data.


-   **Dimension Tables \(DIM\)**

    Tables in the Data Warehouse \(Data Warehouse\) that are associated with FACT tables and contain attributes \(reference information\) about the data in the FACT tables. DIM tables categorize and describe the data in the FACT tables.


-   **ERD**

    Entity Relationship Diagrams \(ERD\) diagrams show the association between FACT and DIM tables and from the star of the star schema in Data Warehouse.


-   **ETL**

    ETL stands for Extraction, Transform, and Load. ETL is a process that extracts, transforms, and loads data from multiple sources to a data warehouse or other unified data repository.


-   **EWR**

    Experiment Work Request


-   **FACT**

    FACT tables in the Data Warehouse store measurements, metrics, or other information related to an IC database operation. FACT tables contain all the primary keys for associated dimensions. FACT tables hold measurable, quantitative data about processes and are associated with specific DIM tables that contain attributes \(reference information\) about the data in the FACT tables. The following are some examples of FACT tables. CLAIM\_FACT, WIP\_FACT, MEASUREDFACT, PLY\_RAWDEFECT\_FACT, CHIPPARMFACT.


-   **Front Opening Universal Pod \(FOUP\)**

    Specialized plastic carrier designed to hold silicon wafers securely and safely in a controlled manufacturing environment. The FOUP transports wafers to and from equipment stations throughout the manufacturing process.


-   **IC**

    IC is the abbreviation for Information Center. IC refers to the Data Warehouse database documentation. Formerly, these ICs were referred to as wikis.


-   **KERF**

    KERF refers to the area in a silicone wafer that is used to separate individual dies at the end of wafer processing. KERF can also be referred to as the width of material removed from a silicon wafer. In manufacturing, this is where test structures for inline testing can be created.

    In Data Warehouse, KERF also refers to information about the testing of a KERF.


-   **POR**

    Plan of Record.


-   **PSM**

    Process Split Merge.


-   **PLY**

    Process Limited Yield \(PLY\) is a system that controls daily manufacturing operations and collects data about the manufacturing process at a site. The PLY system collects the raw defect data and forwards this information to Data Warehouse for analysis. Defect data in Data Warehouse includes raw defect size and location, wafer summaries, and overlay of defects to diagnostic callouts from electrical test data.


-   **STAR SCHEMA**

    The term Star Schema describes the data format of the FACT and DIM tables within the Data Warehouse. The STAR schema diagram represents a STAR image with the FACT table as the center of the star surrounded by all its associated DIM tables. Each FACT table joins to multiple DIM dimension tables that describe the information that is contained within the FACT table.


-   **WBS**

    Wafer Based Split


-   **WIP**

    A work in progress \(WIP\) report is used in the semiconductor industry to track wafer development during the semiconductor manufacturing process. WIP reports are user configurable and can be configured to collect data \(parameters\) about wafers.


