# Wafer Maps

The main goal of the Metrology wafer maps is to show all the measurement points on a wafer, which are measured by a measurement tool at a specific measurement timestamp.

A Metrology wafer map is composed of several cells \(rectangular boxes\) made by intersection of vertical and horizontal lines. By default, the number of lines is 40 rows and columns. Notice the cells or grid lines in the Metrology wafer map has nothing to do with actual geographical wafer map entities such as chips, kerfs, or recticles.

Each cell is drawn with a color representing relevance among measurement points. The algorithm to determine the color of a cell is based on weighted average calculations of all the measurement points in the wafer map. All the weighted average calculations are performed on the server side, transformed into the wafer map data structure, and transferred to the client side, where the wafer map is rendered using the wafer map components.

The **Wafer Maps** tab displays a thumbnail gallery of wafer maps representing the measurements performed on each wafer it the lot at the specified time. From this gallery, you can:

-   select which wafers are displayed
-   [view the SQL query used to fetch the data currently visible.](abi_ug_view_sql.md)
-   export an image of the maps
-   click the measurement name to analyze the measurement
-   click a thumbnail to [drill down into an individual wafer map](abi_ug_view_wafermaps.md)

-   **[Viewing Wafer Maps](../ABI_User_Guide/abi_ug_view_wafermaps.md)**  
From the Wafer Map gallery, you can select a specific map to drill down into the measurements taken of the wafer.

**Parent topic:**[Metrology Data](../ABI_User_Guide/abi_ug_lot_metrology.md)

**Related information**  


[View SQL](abi_ug_view_sql.md)

