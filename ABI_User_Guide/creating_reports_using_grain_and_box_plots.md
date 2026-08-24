# Using Grain in Reports

Using Grain in an ABI Report Chart allows users to separate out data points for enhanced granularity. Putting a particular data field reformat the chart to show distinct nodes for each data point of that field.. The reports shown below are non exhaustive examples of how to use Grain when using the **Chart Builder**

1.  Click the **Reports** tab on the ABI Landing page, Create or Select a report. In this demonstration, an existing report, Grain Example, is used. Click the **Report Name** to open it..

    ![Creating an Operation Summary Report](images/GrainChartsReportSelect.png "Selecting a report ")

2.  Once the report opens, click the **Chart Builder** tab. To use Grain, you will need to use the **Chart Drop down** to select a chart with access to Grain. Currently those are Grid and Distribution type charts. For this example, select a Box Plot chart. Populate the **X** and **Y**axis with Parent Lot ID \(SC\) and Avg Dcitem Value \(M\) Add Wafer ID to the **Color** field. Click **Refresh** to render the chart.

    ![](images/GrainChartsBoxPlotSiteNoGrainWaferColorSettings.png "Create the chart without grain")

3.  Populate the Grain with Site X Coord and click **Refresh** again. The chart updates to show a more granular look based on the Raw Number and Wafer ID.-/

    ![](images/GrainChartsBoxPlotSiteGrainWaferColorSettings.png "Grain changes the chart's presentation")

4.  Grain does not filter, change, or perform calculations on data. It takes each data point in the selected column and separates them out for better display. To demonstrate this. The same report is shown in a scatter plot, with no grain or color applied. It has been averaged to a single point.

    ![](images/GrainChartsScatterNoGrain.png "The report as a scatter plot with no grain")

5.  Here is the same chart with Wafer ID in the **Grain** field. Note that each wafer is displayed independently of the others.

    ![](images/GrainChartsScatterGrain.png "With Grain, multiple points are visible.")

6.  The **Color** field also has a similar function to **Grain**. Here is the same chart with Wafer ID in the **Color** field rather than **Grain**.

    ![](images/GrainChartsScatterNoGrainColor.png "The same Chart with Color instead of Grain")

7.  **Grain** and **Color** can be used together for further separation, as shown in the Box Plot above.


**Parent topic:**[Reports - Creating and Managing](../ABI_User_Guide/abi_ug_wip_reports.md)

