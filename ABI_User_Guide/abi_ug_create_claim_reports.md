# Creating Claim Reports

Claim reports in the ABI application are reports that typically address quality factors that might occur during semiconductor manufacturing. Claim reports display the SiView Claim history for a lot including detailing which Process, Measurement, PLY and Electrical test steps the lot has been through with a timestamp. The details of each step are collected - the equipment used, the recipe and the operator who performed the action. The Claim reports can contain information on defects, process deviations, and any other factors that might impact wafer production. You can configure your Claim report to track specific parameters and save your claim reports to your categorized folders. You can view the parameters \(basis\) for each saved claim report, share it, copy it, and export the claim report to .csv, .xlts, or .pdf formats.

On the Reports section of the ABI application, you can create a claim report and define the parameters for that report. Like other ABI reports, you can designate visibility \(public or private\) and you can share your report.

Claim reports can be created using two different **Report Definitions** that define all the parameters in a report. The first step to create a Claim Report is the same, but when you select a **Report Definitions**, the report creation process varies. Step 1 in the following procedure is the same for both report types . After Step 2, the procedure links you to create a report using the **Report Definitions** you select.

**Note:** Folders on the ABIlanding are accessible throughout the ABI application. When you create a new report, you designate a folder location for your report. See [Creating and Organizing with Folders](abi_ug_folder_management_procedure.md) for more information on foldering.

1.  Click the **Reports** tab and then click the drop down arrow on the **Create Reports** control to select the **Claim Report.**

    ![Click the Claim Report Option on the Drop-down Menu to Select the Report Type](images/Claim_Report_Create_Select_Claim.jpg "Clicking the Claim Report Option to
    Select the Report Type")

    The Create New Claim Reportpage opens.

2.  Select the **Report Definition** option that you want to use to create your report. Links to each Report Definition Type follow this table. Click the **Report Definition** type link and create your Claim Report.

    ![Create your claim report and select define the report parameters in this modal.](images/Claim_Reports_Define_Parameters_2.jpg "Creating and Naming a Claim Report and Defining Its
    Parameters")

    |Report Definition Type|Description|
    |----------------------|-----------|
    |Define Lots & Parameters|Use this option to define lots and parameters for your Claim Report.|
    |Claim Completes Report|The Claim Completes Report can track all Lots that pass through a specific Equipment Tool. Some filters that might be used in these reports might be a set time frame or a specific category of Lots that have a status of Complete. **Claim Completes Report** use the specific OPE variables as a default, **ForceComp** and **OperationComplete**.

|

    Claim Reports can be created using either the **Define Lots & Parameters** outlined here in [Creating a Claim Report - Define Lots ＆ and Parameters](abi_ug_creating_a_claim_report_define_lots_parameters.md)or the **Claim Completes Report** outlined here in [Creating Claim Reports - Claim Completes Report](abi_ug_creating_claim_reports_claim_completes_report.md).


-   **[Creating Claim Reports - Claim Completes Report](../ABI_User_Guide/abi_ug_creating_claim_reports_claim_completes_report.md)**  
**Claim Completes Report** use the specific OPE variables, **ForceComp** and **OperationComplete** when creating a claim report.
-   **[Creating a Claim Report - Define Lots ＆ and Parameters](../ABI_User_Guide/abi_ug_creating_a_claim_report_define_lots_parameters.md)**  
This topic shows users how to create a Claim Report using the Report Definition **Define Lots & Parameters**.

**Parent topic:**[Reports - Creating and Managing](../ABI_User_Guide/abi_ug_wip_reports.md)

