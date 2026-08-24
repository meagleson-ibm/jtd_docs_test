# Groups

In the ABI application, groups are customized groupings of Lot IDs. Creating creating customized groups provides insights into wafer production during the manufacturing, claim, and PLY processes.

Creating groups in the ABI application is a way to gather and group Lot IDs and track and monitor the grouped Lot IDs as they travel thorough the overall manufacturing process. Groups are created with reports because when you define the parameters of a group in conjunction with a report, you are in essence creating a subset of the parameters that are defined in the report. The report type that you create with your groups depends on your intent. For example, WIP reports track wafer and lot status during manufacturing. If you intend to track the status of lots and wafers that are processed by a particular piece of equipment, you might create a group in conjunction with a WIP report as the parameters in the associated group would be a subset of the parameters in the WIP report. When you create a group, you name your group and it becomes known as a **labeled** group and displays in a tab in the report table. To learn more about different report types, see [Reports - Creating and Managing](abi_ug_wip_reports.md).

Groups can also be created using a spread sheet import. Using the spread sheet import creates a group that is not directly associated with an ABI report. See [Creating Wafer-Based Split Groups](abi_ug_creating_groups_using_import.md)

**Note:** MES systems can create automatic runs of experiments for specified lots and wafers. MES systems typically split the lots during experimentation and merge the lots back together when the experiment concludes. Data Warehouse also captures historical data from these events for particular lots and wafers.

Rules for creating groups.

-   Groups may not reference other groups.
-   All groups are public and are available for anyone in the application to view and use.
-   Group names must be unique across ALL defined groups.
-   Group names must not contain commas.
-   Foldering on the ABIDashboard separates Groups from non-Group items.
-   Groups are related to a report by using a Child/Parent relationship. This association is either as a Basis Group or labeled Group.
-   The same group cannot appear twice for a report.

-   **[Creating and Using Groups](../ABI_User_Guide/abi_ug_creating_and_using_groups.md)**  
You create groups in the ABI application and associate those groups with reports to establish the parent-child relationship. The parent-child relationship is not a contained relationship.
-   **[Creating Wafer-Based Split Groups](../ABI_User_Guide/abi_ug_creating_groups_using_import.md)**  
**Wafer‑Based Split** \(WBS\) Groups are a mixed grain group and can be composed of three different grains at the same time: Lot based, Wafer Based, and Lot and Wafer based. WBS Groups can be created directly in the ABI application, by importing an Excel spreadsheet, or importing a comma-separated text file that contains group parameters \(fields\) for a data view. Importing the spreadsheet or text file injects the data into the query. Each of the rows in a WBS group definition must be unique for the LotID/WaferID pairs, and at least one of the two needs to have a nonempty value. WBS groups cans be used to track processing outcomes by identifying associated experiments in the short and long description fields in imported spreadsheets.
-   **[Creating a Composite Group](../ABI_User_Guide/creating_a_composite_group.md)**  
Composite Groups are composed of one or more regular groups. The Composite Group represents the intersection of rows for each of the individual groups.

**Parent topic:**[Reports, Portfolios, and Groups](../ABI_User_Guide/reports_portfolios_and_groups.md)

