# Configure a Sweep Test

Upon test creation, a configuration box is created for each device terminal present consisting of an instrument terminal and a text box detailing the setting of each instrument terminal property. Each box must be configured before use as follows.

1.  To associate an instrument terminal with a device terminal, click the dropdown box and select the instrument terminal to associate with the device terminal. If TestBench detects a switch matrix- meaning that both the instrument terminal selected and the device terminal are present in the Switch Matrix configuration map - TestBench will automatically perform the switch matrix connection. If the switch matrix is not configured to use either the instrument terminal or device terminal then a hard connection between the instrument terminal and device terminal is required.

2.  To configure instrument terminal properties, double click on the text box immediately below the instrument terminal selection dropdown box after an instrument terminal has been selected. This opens a dialog box where the instrument terminal properties are configured. Make any changes to the terminal properties and close the dialog box. The dialog box is dynamic and show relevant instrument properties as properties are selected. The text box will update to show the instrument terminal properties changes that were selected.

3.  To select an instrument terminal property to sweep, right click on the property name and select **Sweep** in the context menu. The form will change showing additional options to control the sweep.

4.  Remove a sweep by right-clicking on the instrument property name and selecting **Remove Sweep.**

5.  There are Several Sweep Options that can be configured, such as:

    **Sweep Types**:

    -   **Linear**

        A simple linear sweep from Start to Stop at a given Step increment. It is not guaranteed that the sweep will perform the last step. For example, if Start=0 and Stop=0.1 but Step=2 only one point will be executed, that of 0. The Stop value of 0.1 will not be executed due to rounding and the Step size. Look carefully at the number of steps to ensure the sweep covers the values of interest.

    -   **Log**

        A logarithmic sweep. In addition to positive value sweep moving from small to large values, TestBench also support negative value sweeps moving from large to small values. For example, a sweep from ‑1 to ‑0.001. Anytime the sweep is moving from a large magnitude to small magnitude you will notice the PPD \(points per decade\) change to a negative value indicating the direction of the sweep.

    -   **List**

        A comma separated list of values to use. Dual Ramp option is not supported for this type of sweep.

    **Dual Ramp**: This option is available for Linear and Log sweep types. When this option is enabled, the sweep will make a loop, moving from Start to Stop then back to Start.

    **Sweep Level**: If more than one sweep is configured you can decide if you want both sweeps to occur together or if you would like an inner loop and outer loop.

    -   **Inner and outer loops**

        The first property that is marked for a sweep is automatically assigned a sweep level of 1. When the next property is marked for a sweep, it is assigned the next sweep level which in this case would be 2. The lowest sweep level is the inner most loop. An arbitrary number of sweep levels are supported. You can change the order of the loop by adjusting the sweep level.

    -   **Sweeping more than one property together**

        If two or more properties are assigned the same sweep level then they will be swept together. TestBench does not enforce that the number of Steps of each sweep be the same. TestBench will stop the sweep when the number of steps executed reaches the sweep with the fewest number of steps.

6.  
**Parent topic:**[Sweep Test](../../id_docs/testbench/sweep_test.md)

