# Setting up SmartContact

TestBench supports automatically adjusting the prober chuck height to facilitate SmartContact.

1.  Create a test to check if the probes are touching a device.

    For example, using the ProbeCheck macros and a generic test where current is passed between shorted pads.

2.  Create an Exit Condition called `zStep` that when "false" indicates that contact is not made and "true" when contact is made.

3.  Click **Options** \> **Test Options** \> **Max Prober chuck z step height** to set the maximum allowed amount to adjust the prober chuck height to make contact by \(with the test highlighted\).

4.  Enter the maximum amount to adjust the chuck in order to pass the `zStep` Exit Condition.

    **Tip:** Chuck height is adjusted in steps of 5um. Enter a value of zero to disable chuck height adjustments.

    The height found to pass `zStep` will be used on all subsequent prober movements until another test is encountered where **Max Prober chuck z step height** is not zero. You may have a test which detects if the prober has been overdriven too much \(probe skate test, for example\). You can create an Exit Condition called `zHeightDisable`, which if true, will disable adjustment of the chuck height.


**Parent topic:**[TestBench Overview](../../id_docs/testbench/testbench_overview.md)

