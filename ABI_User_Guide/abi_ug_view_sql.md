# View SQL

Structured Query Language \(SQL\) is the programming language that is used to access and retrieve defined parameters from the Data Warehouse tables for ABI reports. The **View SQL** control in the ABI UI opens a modal that shows how the SQL command ran and gathered the requested information for WIP, Claim and PLY Reports, and Lot Lists.

During Report creation,ABI users define the Lots and parameters they want to track and view within their Reports. Each Lot and category has a subset of parameters ABI users can use to learn more about during the manufacturing process. For example, an ABI User who wants to track Lot Status. The user selects the Lot status and any of the status parameters that are contained within Status, such as Priority Class, Hold State, and Location IDs. When a report is created, the ABI User can click **View SQL** to confirm the information sources for Reports. The SQL modal opens and shows how the SQL Command retrieved the requested data. A Scroll bar within the modal allows users to scroll through the full command run.

**Note:** The **View SQL** action is available throughout the ABI application.

![SQL Modal Displaying SQL Command Used in Query to retrieve the requested information.](images/WIP_Report_SQL_for_SQL%20Testing_Config.jpg "SQL Modal Displays SQL Command Path Used in Query")

ABI Users can click **Download.txt.file** to download the text file or click the **Copy SQL** icon to copy the SQL command text to their clipboard.

**Parent topic:**[Application elements](../ABI_User_Guide/abi_ug_navigation.md)

