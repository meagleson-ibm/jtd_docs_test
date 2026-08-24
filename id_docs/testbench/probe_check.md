# Probe Check

The Probe Check test is used within a test structure. The Probe Check test verifies and measures the contact between probes and wafer. The on-wafer test structure consists of two parts. Part One of the Probe Check consists of a test that uses a set of probing pads that are shorted to each other for a continuity test between pads. Part Two of the Probe Check consists of testing the electrical state of the skate. The skate is a pad the connects to an optional metal line around the pads. This test checks that the probes don’t skate off the pads and short to nearby metal lines during probe contact.

Probe Check tests consist of two parts.

-   **Probe Short Check**

    The **Probe Short Check** performs a continuity check between shorted pads using either an SMU \(Source Measurement Unit\) and a GNDU \(Ground Terminal\) **OR** a pair of SMUs. This check applies current and measures voltage Resistance between the pads and registers a **Pass** or **Fail** result based on the calculated maximum pass resistance.

-   **Probe Skate Check**

    The **Probe Skate Check** is used if a skate pad has been defined \(a pad number greater than zero\). A leakage test between the skate pad and the rest of the pads that are not shorted to the skate pad is performed. This test applies a voltage to the skate pad \(using an SMU\) and grounding the rest of the pads \(using a GNDU - preferred or SMU\).


-   **[Configure a Probe Check](../../id_docs/testbench/configure_a_probe_check.md)**  
Probe check tests in TestBench do not require users to select a particular instrument terminal. For this test, TestBench automatically selects the instrument terminals necessary for the measurements.
-   **[Configure a Probe Skate Check](../../id_docs/testbench/configure_a_probe_skate_check.md)**  
Probe check tests in TestBench do not require users to select a particular instrument terminal. For this test, TestBench automatically selects the instrument terminals necessary for the measurements.
-   **[Probe Test Results](../../id_docs/testbench/probe_test_results.md)**  
When Probe tests complete, TestBench displays the Probe Check Test Results.

**Parent topic:**[Available Tests](../../id_docs/testbench/available_tests.md)

