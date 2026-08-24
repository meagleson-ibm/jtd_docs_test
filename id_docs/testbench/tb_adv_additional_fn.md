# Additional functions

-   **`BestDieEstimate(<parameterReference>, <default value>, <percentile>, <screenLo>, <screenHi>)`**

    Returns the filtered value for test property `<parameterReference>`.

        |Description|This function returns a curated value of a test property that can be referenced in subsequent formulas. The test property is validated against low and high screening limits. If the value is not valid, all previous test properties across the wafer are used estimate a valid value. If no valid values are found, a default value is used.|
    |Inputs|    -   `<parameterReference>`: The name of the test parameter of interest to filter.

**Note:** This parameter name should be contained within quotes. For example, to return a filter value for test property Resistance, use `“Resistance”`, not `#Resistance#`.

    -   `<default value>`: The value to return if no valid value was found.
    -   `<percentile>`: If more than one valid parameter is found, return the value at this percentile \(linearly interpolated\).
    -   `<screenLo>`: Filter values that are below this value.
    -   `<screenHi>`: Filter values that are above this value.
|
    |Output|A double value.|
    |Example|To subtract out a parasitic resistance, the parasitic resistance is measured on a specifically design DUT. However, if the DUT is bad, the median of valid resistances that was measured is used. ![Example setup of BestDieEstimate to validate a Test Property named Meas_Res against a Device Property named Rs_ohms.](../_images/data_setup_test_props.jpg "Example setup of BestDieEstimate to validate a
Test Property named Meas_Res against a Device Property named Rs_ohms. Values ranging from half to
double the expected value are valid. If no valid value is found the default Device Property Rs_ohms
is returned.")

Place a test voltage across the DUT and calculate the resistance as a Test Property as shown.     ```
Meas_Res = #high_Voltage#[0]/#high_Current#[0]
    ```

Create a validated version of this Meas\_Res Test Property and store as another Test Property to be used by subsequent tests as shown     ```
Est_Res = BestDieEstimate(“Meas_Res”, #Rs_ohms#, 50, #Rs_ohms#/2, #Rs_ohms#*2)
    ```

 The design value of the parasitic resistance is a device parameter called `Rs_ohms`. The `Meas_Res` is validated against the design resistance. The value must be between half and double the design resistance. In the example shown below, the current DIE didn’t have a valid value, so the median of previous measured values is returned. If a valid value was not found using all previous tests, then the default design resistance would have been returned \(in this example 15kΩ\). ![Example output of BestDieEstimate where the measured resistance wasn’t valid.](../_images/data_setup_best_die_est.jpg "Example output of BestDieEstimate where the measured
resistance wasn’t valid so a median value from previous measurements is returned. In this example
the Device Property Rs_ohms was 15k.")

**Note:** We don’t have to place `Est_Res` as a Test Property. We could use `BestDieEstimate` directly in a subsequent column calculation, for example. However, by placing it as a Test Property, it only needs to be calculated once. If used many times, it would be calculated each time, reducing performance.

|

-   **`ExtractXatY(<x column>, <y column>, <y value>, <interpolation>, <project>, <closest>)`**

    Returns the x value that corresponds to the `<y value>`. Input:

    -   `<interpolation>`: a string value for how to interpolate between points.
        -   “lin”: x=linear y=linear
        -   “loglin”: x=log y=linear
        -   “linlog”: x=linear y=log
        -   “log”: x=log y=log
    -   `<project>`: Project point past the dataset – used only if point is not bound by dataset “true” or “false.”
    -   `<closest>`: Return the closest point – used only if point is not bound by dataset.
-   **`ExtractYatX(<x column>, <y column>, <x value>, <interpolation>, <project>, <closest>)`**

    Returns the y value that corresponds to the `<x value>`. Input:

    -   `<interpolation>`: a string value for how to interpolate between points.
        -   “lin”: x=linear y=linear
        -   “loglin”: x=log y=linear
        -   “linlog”: x=linear y=log
        -   “log”: x=log y=log
    -   `<project>`: Project point past the dataset – used only if point is not bound by dataset “true” or “false.”
    -   `<closest>`: Return the closest point – used only if point is not bound by dataset.
-   **`Max(<column>)`**

    Returns the max value in column `<column>`.

        |Input|`<column>`: A reference value to a column from which to return the max value|
    |Output|A double value.|
    |Example|`Max(#drain_Current#)`|

-   **`Max(<column>, <column2>)`**

    Returns the max value at each index between the two columns.

        |Input|    -   `<column>`: A reference value to a column.
    -   `<column2>`: A reference value to another column.
|
    |Output|A list of doubles - the list length will be the shorter of `<column1>` and `<column2>`.|
    |Example|`Max(#colname#,#differentcolname#)`|

-   **`Min(<column>)`**

    Returns the min value in column `<column>`.

        |Input|`<column>`: A reference value to a column from which to return the max value|
    |Output|A double value.|
    |Example|`Min(#drain_Current#)`|

-   **`Min(<column>, <column2>)`**

    Returns the min value at each index between the two columns.

        |Input|    -   `<column>`: A reference value to a column.
    -   `<column2>`: A reference value to another column.
|
    |Output|A list of doubles - the list length will be the shorter of `<column1>` and `<column2>`.|
    |Example|`Min(#colname#,#differentcolname#)`|

-   **`Vt(<Gate Voltage Column>, <Drain Current Column>, <target current>)`**

    The threshold voltage of a `MOSFET` is returned given the gate voltage, drain current, and target threshold current. This function returns the `<Gate Voltage>` at which the `<target current>` was found in the `<Drain Current>`. Prior to extracting the gate voltage the curves are first interpolated using a cubic spline.

    **Example Syntax:** `Vt(#Gate_Voltage#,#Drain_Current#,(#TotalWidth#/#Length#)*100e-9)`


**Parent topic:**[Formulas](../../id_docs/testbench/tb_adv_formulas.md)

