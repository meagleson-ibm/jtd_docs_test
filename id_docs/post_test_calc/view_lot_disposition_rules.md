# View Lot Disposition Rules

Simple steps for viewing Lot disposition rules.

**Note:** The following are some example scenarios to show how lot dispositioning works, as well as the behavior in some edge cases:

-   A lot disposition rule is created with a limit of 2 wafers failing SCRAP, or 10% fail. If a lot comes with two wafers, one of which fails a SCRAP rule, there is a 50% fail rate, so the lot disposition rule will fail even though less than 2 wafers failed SCRAP.
-   If a single wafer fails multiple rules under the same category, it is only counted under that category once. So, if a wafer fails two wafer disposition rules for SCRAP, the SCRAP counter is only incremented by one for the lot.
-   A wafer can count under multiple fail categories, if it fails multiple wafer disposition rules for different categories. If a wafer fails a SCRAP and HOLD rule, both of those counters will be incremented.

1.  On the Test Results page, click the **More** icon in any Test Program row, and select **View lot data**.

2.  Select the **Lot Disposition** tab.

    The Lot Disposition tab displays details of the disposition rules, including the Test Level, Family Code, creator, updater, creation and update dates, and enabled status.

3.  To see more information, click the **Down Arrow** next to the test level name. This expands the disposition rule.

4.  When expanded, the disposition rule shows additional including the rule's threshold actions, the number of wafers that can fail each action before failing the entire lot, and the percentage of failures per action that can occur before failing the lot.


-   **[Create a Lot Disposition Rule](../../id_docs/post_test_calc/create_a_lot_disposition_rule.md)**  
The steps for creating Lot Disposition Rules
-   **[Edit a Lot Disposition Rule](../../id_docs/post_test_calc/edit_a_lot_disposition_rule.md)**  

-   **[Default Lot Disposition Rules](../../id_docs/post_test_calc/default_lot_disposition_rule.md)**  
Default Lot Disposition Rules apply to all test levels and family codes within a specific technology.

**Parent topic:**[Navigating to Disposition Pages](../../id_docs/post_test_calc/navigating_to_disposition_pages.md)

