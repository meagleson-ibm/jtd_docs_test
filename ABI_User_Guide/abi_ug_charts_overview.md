# Charts Overview

The ABI application offers charting options that give users deeper insights into their reports and the chip manufacturing process. ABI **Chart Administrator** users can create global level customized charts and standard report charts. Global customized charts are global in the sense that administrators can create them and save them as public charts available to all ABI users. Report charts differ from global charts in that global customized charts are created independently from actual, live reports and use values that correspond to a particular report type. Report charts differ in that report charts are created **within** live reports. Charts Overview introduces global and report charts that are created in the application.

**Note:** Visibility and Access to the Top-Level Chart tab is only available to **Chart Administrators**.

-   **Global Level Charts**

    Global Level Charts are considered stand-alone because they are not connected to any reports in the ABI application when they are created. **Chart Admin** users can create these customized charts to track and visualize interactions between parameters during the manufacturing process over defined time frames. For example, a chart might be configured with filters based on the parameters available in the data set.

    A chart can be made public or private similar to a report and the **Chart Admin** user accessing the chart can make point in time non-destructive operations on it. Customized user-created charts are considered private to the **Chart Admin** users who created them. However,**Chart Admin** creators can designate the charts public and elevate the charts as templates to be present in reports of the same data type for that individual user. **Chart Admins** can create, elevate, and share global and report type charts.


-   **Report Charts**

    Report Charts are created within reports. The ABI application supports two types of report charts: Report-Type Default and Report-Specific Customized charts.

    **Report-Type Default** For each report type that is created the ABI system generates default reports for that specific report type. For example, because WIP reports track wafer and lot status during manufacture, the default WIP report charts are **WIP at Photolayer** and **WIP at Tool**. Both of these charts reflect the processing status of lots \(actual and inventory\) and wafers.

    **Report-Specific Customized** Users have two options when creating a custom chart in a report. One options is to create a totally new chart in the chart editor and the second is to edit an existing chart and save it as a new chart. This customized chart differs from the Global Level chart in that the variables used to create the report-specific customized chart are the variables that pertain directly to each report type. For example, the variables that the ABI application generates for use in a WIP report-specific-customized chart, are the variables that pertain to Lots and Wafers. The origin of the variables that are generated for this report-specific customized chart is listed as **Data Origin - WIP - LotsWIPView**. ABI users can create **Global Customized** and **Report-Specific Customized** charts and elevate those charts or template use. **Chart Admins** must also have the **Admin** user role. When **Chart Admins** create a **Report-Specific Customized** chart, the **Manage Chart** control becomes active and can be used to create a template of the chart and elevate the public chart to the **Global Level** or assign it as a standard chart to any ABI report.

    For **Report-level** charts, the following table outlines available report chart types.

    |Chart Type|Analysis View|Description|
    |----------|:------------|-----------|
    |**Bar**|Grouped Bar

 Stacked Bar

|Bar charts enable users to track Lot IDs, defect rates, and performance metrics.|
    |**Combo**

|Group Combo

 Stacked Combo

|Combo charts enable users to view the relationships between parameters in separate groups, showing each group as a combo. These charts can also be stacked to view the variations between groups.|
    |**Line**|Discrete Line

 Continuous Line

 CDF

 Parallel Axes

 Parallel Axes Values

|Line charts are used to monitor trends over set time periods.|
    |**Area**|Area

|Area charts can be used for data visualization that combines data line and cumulative yields values over time.|
    |**Grid**|Scatter

 Simple Scatter

 Single Axis Scatter

|Scatter charts can be used for visualizing device performance on a graph. Heatmaps can provide insight into a die's location on a chip.|
    |**Distribution**|Box Plot

 Histogram

 Stacked Histogram

|Box plots give a summary of data distribution between different processes. **Note:** **Boxplot Calculations** The Interquartile range \(IQR\) consists of the central 50% of the data, and contains the majority of the data points. Values above Q3 + 1.5xIQR or below Q1 - 1.5xIQR are considered as outliers, and define the whisker boundaries. Values above Q3 + 3xIQR or below Q1 - 3xIQR are considered as extreme points \(or extreme outliers\). No special representation is made for extreme outliers today.

|


To Learn more about Creating Customized Charts see [Creating Global Customized Charts](abi_ug_top_level_charts.md). To Learn more about creating report charts see [Creating Report Charts](abi_ug_create_report_chart.md)

-   **[Creating Global Customized Charts](../ABI_User_Guide/abi_ug_top_level_charts.md)**  
Global customized charts are charts that ABI **Chart Administrators** can configure for any report in the ABI application. **Chart Administrators** can create, save, and elevate customized charts for global use in reports as standard charts and as templates.
-   **[Creating Report Charts](../ABI_User_Guide/abi_ug_create_report_chart.md)**  
The ABI application supports different report types and each report type has a pre-defined set of corresponding default standard charts and an option to create customized report charts. Report charts differ from global charts in that global customized charts are created independently from actual, live reports and use values that correspond to a particular report type.
-   **[Viewing Report Charts - Advanced Options](../ABI_User_Guide/viewing_charts_advanced_options.md)**  
The ABI application offers users advanced chart view options, **Chart Grid**, and **Chart By** for Global Customized Charts and Report Charts.

