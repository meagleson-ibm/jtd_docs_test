# View Wafer Disposition Rules

Simple steps for opening a wafer disposition rule, selecting a different one, and closing the rule pane.

A wafer disposition rule is defined as a condition on some wafer-aggregated parameter value and an associated disposition action to take if the condition fails. Each wafer disposition rule is defined under the PNP which the associated parameter is defined.

This page shows all wafer disposition rules defined in PNPs that were tested on this wafer, and shows the status of each of them, using this wafer’s data. The overall wafer disposition status \(pass if all rules pass, fail if any fail\) is also displayed near the top of the page.

To create a new rule, click the blue box near the top right corner, and to edit or delete a rule click on the overflow menu for the corresponding row \(three vertical dots\). When creating or editing a rule, you must give it a name and a description and decide whether it will be enabled. Only enabled rules are used when making disposition decisions, but all rules are displayed on this page. You then select the parameter to reference \(ensure that this is in the desired PNP\) which property \(i.e. type of aggregated parameter\) to use for the condition, as well as the condition itself. You must also choose the associated SiView action to take if the rule fails.

**Note:** Currently, this SiView action is not actually used, it is just put into different buckets when making lot disposition decisions. See the lot summary page for further explanation.

**Note:** If you select a parameter in a PNP not tested by the wafer you are currently viewing, the rule is still created but will not appear on this screen. Only rules that are defined for PNPs tested by this wafer are displayed.

**Note:** If a wafer disposition rule references a parameter that was not tested on this wafer, the disposition rule fails.

The following is an explanation of the aggregated parameters you can choose from:

-   `NumValidObs`: Number of observations excluding screened and censored values.
-   `YieldPct`: percent of “valid” observations which are passing
-   `WACYieldPct`: percent of all observations which are passing
-   `CensoredYieldPct`: percent of observations which are not censored
-   `ScreenYieldPct`: percent of observations which are not screened
-   `NumInSpec`: number of passing observations
-   `NumNotInSpec`: Number of valid observations which are not passing
-   `Cp`: abs\(spechigh – speclow\) / \(6 \* standard deviation\)
-   `Cpk`: Cp \* \(1 – k\)
    -   k = abs\(mean – target\) / \(abs\(spechigh – speclow\) / 2\)
-   `Average/median/min/max/standard deviation/percentiles`: Standard mathematical operations. Only calculated on values which are not screened or censored.

1.  While on a Wafer Disposition Page, click on the **Disposition Rule Name** or another part of the disposition rule. This opens the Details pane for that disposition rule.

2.  The Disposition Rule Detail Pane shows all the vital information for that disposition rule, including its ID, Status, the full parameters and rule statement, the related test program, and its date of creation and last modification.

3.  To view a different disposition rule's details, click that rule and its details will fill the Detail Pane.

4.  To close the Detail Plan, click the **X Icon** at the top of the pane.


-   **[Create a Wafer Disposition Rule](../../id_docs/post_test_calc/create_a_wafer_disposition_rule.md)**  
The steps for creating Wafer Disposition Rules
-   **[Edit a Wafer Disposition Rule](../../id_docs/post_test_calc/edit_a_wafer_disposition_rule.md)**  


**Parent topic:**[Navigating to Disposition Pages](../../id_docs/post_test_calc/navigating_to_disposition_pages.md)

