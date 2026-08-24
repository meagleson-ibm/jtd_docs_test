# Reports, Portfolios, and Groups

The ABI application is an interactive user application that interfaces with the Data Warehouse \(Data Warehouse\). The Data Warehouse is the front-end database that supports, receives, and stores data from Intelligent Fab throughout the semi-conductor chip manufacturing process. The ABI user interface gives users visual access into all aspects of wafer manufacturing data as wafers are processed in Data Warehouse. Using the ABI application, users can create and design various report types and associated charts using Data Warehouse data. ABI's **Portfolio** feature gives ABI users an organizational tool for their reports and charts. ABI's **Group** feature gives users the ability to create a report for customized groups.

This table is an overview and introduction to ABI features. Each high-level topic described here is discussed further in detail in the subsequent chapters.

**Note:** Use this short cut to view data in a new window for any data column \(if hyperlinked\) in an ABI table. For example:

-   On a **Windows** platform, use **Ctrl + Shift + Click** to open the data for any hyperlinked column in any ABI table in a new window.
-   On a **Mac** platform, use **Shift** \> **Option** to open the PLY Tool Recipe details in a new Window.

|**Reports**|**Top Level Reports Types/ Categories**| |
| |Admin

 ILT

 Logistics

 Measured

 Module Test

 PLY

 Processed

 Wafer Test

 Correlation

|Each top-level report represents a report category. Each category contains a subset of related reports. Report subsets that further delineate the report type contents. See [Reports - Creating and Managing](abi_ug_wip_reports.md) to learn more about view Reports for each report category.

 For example, the top level ILT report contains two reports subsets: one to create an ILT report and one to create a raw ILT report.

 Each report category subset contains reports that are related to the top-level category.

|
|**Creating Report Types**|**Ways to Create Reports**| |
| |**Basis**|Creating reports by using Basis means that a user can select a particular set of parameters to create a report. Parameters can be manufacturing identifiers such as Lot IDs, cassette \(wafer\) status, and equipment \(tools\), and other variables used during wafer manufacturing.

 The Basis set of parameters are saved with the report and are accessible after report creation.

|
| |**By Groups**|Creating a report by using Groups is similar to the Basis except that you can group parameters together.

 For example, you might group Lot IDs and add the equipment parameter to view the success of Lot IDs going through a particular piece of equipment.

|
|**Report Views**|**What does a report show me**?|Users configure report parameters that define the information they want to see. ABI then presents reports that visually format the requested information.

 Users can generate a report that is a temporary visualization \(drafts\) or save their reports for later viewing. Users can share their reports with other ABI users.

|
|**Charts**|**What kind of charts can I create**?|Users can create various charts from their generated reports. This list contains available report types.

-   Bar
-   Combo
-   Line
-   Area
-   Grid
-   Distribution

Chart authors can display charts in grid mode or chart by views.

|
|**Portfolios**|**What is an**ABI **Portfolio**?|The ABI portfolio feature is an organizational tool where users can compile their saved reports and charts. Content can be displayed in a table view or select a **Grid** to view your portfolios in grid view. Portfolios can also be shared.

|

-   **[Reports - Creating and Managing](../ABI_User_Guide/abi_ug_wip_reports.md)**  
On the ABI Landing page, you can create and configure interactive reports to track the manufacturing of wafers throughout the manufacturing process. Using these reports you gain access to data from the Data Warehouse \(Data Warehouse\) as wafers are being processed. Users can create, save, and review reports. During report creation, **Field Validation** validates lots that are chosen for the report against existing lots in Data Warehouse to verify data integrity.
-   **[Groups](../ABI_User_Guide/abi_ug_creating_groups.md)**  
In the ABI application, groups are customized groupings of Lot IDs. Creating creating customized groups provides insights into wafer production during the manufacturing, claim, and PLY processes.
-   **[Portfolios](../ABI_User_Guide/abi_ug_portfolios_overview.md)**  
The Portfolio feature is an organizational tool that can be used to compile and organize ABI assets in the ABI application. Assets within the application include reports, charts, objects, and tracked objects. Each asset that you put into a portfolio contains source content. For example, a report gathers multiple sources of information \(source content\) and presents that information in a structured display. If the source content of an asset changes or is updated outside of the portfolio, the source content in the portfolio updates. The only exception to this rule is the standard chart asset because standard chart assets are copied into the portfolio.
-   **[Filter Sets](../ABI_User_Guide/abi_ug_filer_sets.md)**  
Filter Sets are sets of filter settings that are created and stored per report but are savable, editable, and transferable between reports in ABI.

