# Probe Test Results

When Probe tests complete, TestBench displays the Probe Check Test Results.

The following test results table is generated from a simulated Probe Check test. Each table column is described in the list following the table.

![Testbench Simulated Test Results Table](../_images/testbench_probe_check_results_table_sim_probe_test.jpg "Testbench
Simulated Test Results Table ")

1.  **Pads**

    This column identifies two pads that are tested for continuity. Test results are shown in Columns **MaxVoltage\_V**, **Resistance\_Ohms**, and **ShortCheckResult**. The value is the concatenation of each pad ID. For example, tests between Pad 1 and Pad 2 are shown as value **12**. For Pad 9 and Pad 10, the value is **910**.

2.  **MeasVoltage\_V**

    The measured voltage in Volts from applying the current from the configuration parameter **Probe Short Test Current \[A\]**.

3.  **Resistence Ohms**

    This value is the calculated resistance in Ohms derived from the target applied current \(not actual current\) and the measured voltage.

4.  **ShortCheckResult 1 \(pass\)**

    If the measured resistance is less than the configuration parameter **Probe Short Max Pass Resistance \[Ohms\]** the integer **1** indicates a **pass**. If the measured resistance is greater than the configuration parameter **Probe Short Max Pass Resistance \[Ohms\]**, the integer **0** indicates a **fail**.

5.  **SkateCurrent\_A**

    The measured current between the skate pad and the rest of the pads when applying the **Skate Test Voltage \[V\]** value.

    **Note:** If no Skate pad is defined, then this column is not present in the results

6.  **SkateCheckResult**

    If the measured current is less than the configuration parameter **Skate Max Pass Current \[A\]** the integer **1** indicates a **pass**. If the measured resistance is greater than the configuration parameter **Skate Max Pass Current \[A\]**, the integer **0** indicates a **fail**.

    **Note:** If no Skate pad is defined, then this column is not present in the results

7.  **OverallResult**

    Integer **1** indicates all check results pass. Integer **0** displays if any of the tests failed.


**Parent topic:**[Probe Check](../../id_docs/testbench/probe_check.md)

