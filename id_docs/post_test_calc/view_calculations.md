# Viewing Calculations

Post Test Calculation automatically performs new aggregate calculations on new collections of parameter values so that a user can analyze the overall trends and characteristics of a dataset by combining multiple parameter values.

1.  Browse to **Intelligent Test** \> **Post Test Processor**. On the Test Results page, click on a Test Program to open the Test results details page, then select the **Calculations** tab.

    The Calculations tab displays an overview of the calculations performed by the system, including the following information for each parameter:

    -   **Parameter name**
    -   **Type** - the calculation type performed: **Yield** or **User defined**.
    -   **Multiplier** - the multiplier used in a mathematical calculation.
    -   True or False values for **All Censored Inputs**, **All Screened Inputs**, and **All Missing Inputs**.
2.  To edit the rules for a calculation, select the **More Options** icon in the row of the calculation you want to edit, then select **Edit**.

3.  To delete a calculation, select the **More Options** icon in the row of the calculation, then select **Delete**.

4.  To create a new ad-hoc calculation, click **Create calculation**.


-   **[Ad Hoc Calculations](../../id_docs/post_test_calc/ad_hoc_calculations.md)**  
The wafer calculations workflow has many levels of calculations that are performed as wafers pass through manufacturing. After canned calculations are made to calculate the average and chip perfect yield, a new set of calculations that are known as Ad Hoc Calculations are performed. When the enriched PNP \(PNP is the Part Number Program that is specified in the Disposition file.\) is released to the ISDW, Ad Hoc Calculations are the next step in the process. Ad Hoc Calculations can be User Defined or Yield. Each Calculation type has an operation sub-type that yields different results for different perspectives.
-   **[Reload data to recalculate test results](../../id_docs/post_test_calc/reload_teds_data.md)**  
You can select a lot and PNP combination within a technology and confirm the creation submission of the corresponding TEDs files for recalculation and retransmission to the ISDW database through its low priority ETL folder over SFTP.

**Parent topic:**[Post Test Calculation](../../id_docs/post_test_calc/ptc_overview.md)

