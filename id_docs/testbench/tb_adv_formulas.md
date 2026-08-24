# Formulas

Formulas can be used at many locations inside of TestBench, such as New Columns, Exit Conditions, and Test Properties. In each scenario, references to a parameter or column is made by placing its name within `#`.

You can reference items from previous tests or a different device or wafer. If no decorators are used, TestBench assumes the parameter is from the same device or test and look there for its value. For example, the function `#Gate_Current#/#Area_cm2#` will look in the current test and device for columns and parameters that match `Gate_Current and Area_cm2` to perform the calculation. However, if you wanted to use the `Gate_Current` from a different test, you could specify it as `#TEST=IgVg.Gate_Current#`. The fully qualified nomenclature is: `#WAFER=<waferID>.DEVICE=<deviceName>.TEST=<testName>.COL=<colName>#`

Notice that each level is separated by a period \(`.`\). If any reference item \(such as `<deviceName>`\) has a period in it, you must surround the name with quotes. For example, `#DEVICE=BTI_0.02_1.4.TEST=TDDB 1.1V.tbd#` will throw an error. Instead, use `#DEVICE=“BTI_0.02_1.4”.TEST=“TDDB 1.1V”.tbd#`

-   **[Supported functions](../../id_docs/testbench/tb_adv_supported_fn.md)**  
Any function in the `.NET` Math library can be used.
-   **[Additional functions](../../id_docs/testbench/tb_adv_additional_fn.md)**  


**Parent topic:**[TestBench Overview](../../id_docs/testbench/testbench_overview.md)

