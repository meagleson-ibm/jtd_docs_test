# Creating Wafer Based Split Group Reports

ABI users can use Wafer Based Split \(WBS\) Groups to create reports. WBS Groups are designed to track manufacturing experiments and ensure that processes follow an established Process of Record \(POR\). A POR includes the process recipes and parameters requirements that a chip must meet during the manufacturing process. Reports created with WBS groups are able to use charting to visually display manufacturing results.

1.  Click the **Reports** tab on the ABILanding page and then click the drop down arrow on the **Create Reports** control and click **PLY** to select a PLY report type.

    ![Click PLY Report on the Create Report Tab.](images/PLY_Report_Click.jpg "Clicking PLY Report on the Create Report
    Tab")

2.  Click **Create with Basis \(Lot level\)**, **Create with Basis \(Lot& Wafer\)**, or **Create with Groups**.

    ![Complete the fields in Defining Parameters for the PLY Report in the Modal.](images/PLY_Define_Parameters.jpg "Defining Parameters for the PLY Report in the Modal ")

3.  Click **Create with Groups**.

    ![Creating WBS Report with Groups](images/abi_reports_create_wbs_w_groups_3.jpg "Creating WBS Report with Groups")

4.  Click **Add Basis Group** and select a **Wafer Based Split** group. Click **Add**.

    ![Selecting a Basis Group](images/abi_reports_create_wbs_select%20group_4.jpg "Selecting a Basis Group ")

    The selected group is added to the report.

    ![Creating the WBS Report with Groups](images/abi_reports_create_wbs_rpt_creted_5.jpg "Creating the WBS Report with WBS Groups")

5.  Click **Create** to create the report.

    ![Creating the Basis Report with Groups](images/abi_reports_create_wbs_rpt_created_6.jpg "Creating the Basis Report with WBS Groups ")

    **Note:** When the Report is created, you can change the key of the report using the **Default drop down**, you can use the **Groups** filter, and you can change the display of the report using Single, Key, Group, or Pivot.

6.  Click the **Chart** tab to view the chart generated from this report data. The Default Chart is a PLY Density Chart.

    ![PLY Densityr Chart](images/abi_reports_wbs_rpt_chart_9.jpg "Default PLY Density Chart")

7.  Click **Chart Editor** tab. Set the report type to **Grouped Combo** to view the different groups in the WBS group. In the Encoding column, Accept the X and Y axis as Lot ID and Lot Count, and Drag the POR flag to the Color section. Click **Refresh**.

    The Chart now displays the Lots in relation to the POR. **YES \(Y\)** for lots that passed the POR and **NO \(N\)** for lots that did not pass.

    ![View WBS Report Chart with POR Defined](images/abi_reports_wbs_rpt_chart_11.jpg "View WBS Report Chart with POR Defined ")


**Parent topic:**[Reports - Creating and Managing](../ABI_User_Guide/abi_ug_wip_reports.md)

