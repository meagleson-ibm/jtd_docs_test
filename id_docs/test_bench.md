# Test Bench

Test Bench is a new feature in Intelligent Test that integrates the TestBench tool test functions with Intelligent Test.

**Note:** Only users who are on teams assigned to the project that is referenced in a TestBench job can view, edit, delete, or download that TestBench job.

TestBench is a wafer-level semiconductor characterization software control program for Windows™. It is designed to control electrical test equipment such as source-measurement-units, pulse generators, and probers, and to create custom tests and execute those tests on semiconductor wafers. Used with Intelligent Test, Test Bench can accept TestBench Jobs \(which contain Test Plans\) that are created in IT, execute those test plans and return test results to the TestBench IT application.

**Note:** When running TestBench in simulation mode, some ID-related features are disabled, notably View Job Queue, Current Probecard, and Register Test Cell.

-   **[Creating a Test Bench Job](../id_docs/create_a_test_bench_test_plan.md)**  
The IT and TestBench \(TB\) tool integration is a seamless process where Test Plans configured in IT are sent to the TestBench tool for execution.
-   **[Uploading Test Definitions to Intelligent Design](../id_docs/uploading_test_definitions_to_intelligent_design.md)**  
Supported Tests within TestBench can be uploaded as **Test Definitions** to the Intelligent Design system. Supported tests are **Generic Sweep Test**, **Generic Constant Stress Test**, **Generic Pulse Test**, **Generic Keithley TSP**, **Generic Keithley TSP Parallel**, **Generic Ramp Stress**, **Probe Check**, and **WGFMU BTI /HCI DC/AC**. **Generic Constant Stress Testnsubtests** are **NOT**supported and uploaded test definitions do not include the subtests even if they are present in the TestBench test.
-   **[Uploading Test Plans to Intelligent Design](../id_docs/uploading_test_plans_to_intelligent_design.md)**  

-   **[Downloading results of a Test Bench job](../id_docs/testbench/download_tb_results.md)**  
You can download the results of a Test Bench job in JSON or .csv format.

**Parent topic:**[Intelligent Test](../id_docs/intelligent_test_intro.md)

