# Ad Hoc Calculations

The wafer calculations workflow has many levels of calculations that are performed as wafers pass through manufacturing. After canned calculations are made to calculate the average and chip perfect yield, a new set of calculations that are known as Ad Hoc Calculations are performed. When the enriched PNP \(PNP is the Part Number Program that is specified in the Disposition file.\) is released to the ISDW, Ad Hoc Calculations are the next step in the process. Ad Hoc Calculations can be User Defined or Yield. Each Calculation type has an operation sub-type that yields different results for different perspectives.

**Note:** Calculation names cannot contain tilde \(~\), semicolon \(;\), or back-tick characters: \(\`\).

On the Post Test Calculation \(Post Test Processor\) landing page, you can assign Ad Hoc Calculations to the wafers. The calculation table outlines the calculation types, operations, and variables that can be used with each calculation type.

|Calculations|Calculation Types|Operation Sub-Types|
|------------|-----------------|-------------------|
|User Defined|Custom Calculations|This is some calculation that you can type out into the box. You can choose the number of input parameters. Example of a user-defined calculation: ```
def user_function(v1, v2, v3):
    <user entered input, possibly spanning multiple lines>
```

Post Test Calculation uses Python to evaluate the expressions you enter here, and this comes with some caveats: -   You must check the syntax by clicking the **Check syntax** button before you can create or modify the calculation. This will catch simple formatting mistakes.
-   You have access to all of the functions and constants in Python’s math library, but these must be typed in prefixed by `math.`. So to use the square root function, you must type `math.sqrt(v1)`.
-   All variables you use must be entered in the format `v1`, `v2`, etc. \(lower-case\).

Some additions in release 7.0:

-   Users can now also use the `statistics` package, like `statistics.median([v1, v2, v3])`, in addition to the `math` package.
-   Wafer-level aggregate values are available. For example, to find the normalized distance from the wafer mean, you can define a calculation such as `return (v1 - v1.mean) / v1.sigma`, where `v1.mean` and `v1.sigma` would be the wafer-level average and standard deviation of the parameter `v1`. Available aggregate parameters are:
    -   numinspec
    -   numfail
    -   numcensored
    -   numscreened
    -   numspeclow
    -   numspechigh
    -   nummissing
    -   numtotal
    -   min
    -   percentile02
    -   percentile05
    -   percentile10
    -   percentile25
    -   median
    -   percentile75
    -   percentile90
    -   percentile95
    -   percentile98
    -   max
    -   mean
    -   sigma
    -   numobs
    -   yieldpct
    -   wacyieldpct
    -   censoredyieldpct
    -   screenyieldpct

|
|Yield| |These are used to evaluate the number of passing parameters among the input parameters you select. There are a few different options that behave slightly differently. For all of them \(except **Average**\), each of the input parameters are put into one of these three categories: -   OK \(the input is in spec\)
-   Fail \(Input is speclow, spechigh, or censored\)
-   Not Available \(Input is missing or screened\).

 The yield types are: -   **Average**

\(\# passing values\) / \(\# not screened and not missing\)

-   **Chip Perfect**

1.0 “Pass” if all available inputs are OK, 0.0 “Fail” if any inputs are in fail category, Missing “Fail” if all inputs are not available.

-   **Chip Perfect No Incomplete Chips**

1.0 “Pass” if there are no “not available” inputs and all inputs are OK, 0.0 “Fail” if there are no “not available” inputs and any inputs are in Fail category, Missing “Fail” if any inputs are not available.

-   **Chip Perfect No Incomplete Perfect**

1.0 “Pass” if there are no “not available” inputs and all inputs are OK, 0.0 “Fail” if any inputs are in Fail category \(even if some inputs are missing\), Missing “Fail” if any inputs are “not available” and all available inputs are OK.


|

Some other things to note about the calculations:

-   You cannot repeat input parameters, meaning have the same parameter used for input parameters 1 and 2. Doing so will cause the calculation to always fail or possibly cause other bugs.
-   Be careful not to create cyclic dependencies, meaning a situation like parameter A having parameter B as an input while parameter B also has parameter A as an input \(This can happen when editing calculations.\)
-   While the interface will let you select parameters from different PNPs, PTC does not currently support cross-PNP calculations. If you use a parameter from a different PNP while creating a calculation, that input will always act as if it is missing.
-   To edit an existing calculation, press the overflow menu \(three vertical dots\) on the far right of the table for the row corresponding to the calculation you want to edit. The option to delete calculations is also here.

-   **[Assigning Ad Hoc Calculations](../../id_docs/post_test_calc/assigning_ad_hoc_calculations_to_wafers.md)**  
On the Post Test Calculation \(Post Test Processor\) landing page, you can assign Ad Hoc Calculations to the wafers. The calculation table outlines the calculation types, operations, and variables that can be used with each calculation type.
-   **[Editing Ad Hoc Calculations](../../id_docs/post_test_calc/editing_ad_hoc_calculations.md)**  
When Ad Hoc Calculations complete, the test team reviews the yield, which predicts the percentage of prime wafers available for clients at manufacturing completion. If the test team estimates that the test results do not reflect a high percentage of prime wafers, the test team then edits the Ad Hoc Calculations.

**Parent topic:**[Viewing Calculations](../../id_docs/post_test_calc/view_calculations.md)

