# TestBench Overview

TestBench is a wafer-level semiconductor characterization software control program for Windows. It is designed to control electrical test equipment such as source-measurement-units, pulse generators, and probers, allowing the user to create custom tests and execute those tests on semiconductor wafers.

TestBench interfaces with instruments over GPIB, USB, or TCP/IP communication interfaces. It also controls instruments that have their own drivers to interface correctly.

**Note:** When running TestBench in simulation mode, some ID-related features are disabled, notably View Job Queue, Current Probecard, and Register Test Cell.

-   **[Installing TestBench](../../id_docs/testbench/installing_testbench.md)**  
To enable instrument control in TestBench however the following software should be installed in this order.
-   **[TestBench Components](../../id_docs/testbench/test_bench_components.md)**  
TestBench is a characterization software program for Windows™ that allows users to create and configure customized WaferTestPlans and DeviceTestPlans. A test plan defines a test's scope; wafers to be tested \(wafer test\), devices to be used \(device test\), and instruments to use for probing. TestBench test plans are fully customizable. TestBench can be used in Active Mode or Simulation Mode. This document focuses on the TestBench in Simulation Mode.
-   **[TestBench Plan Configuration](../../id_docs/testbench/testbench_plan_configuration.md)**  
Configuration of a TestBench Test Plan requires users to name their Test Plans and then define the wafers, devices, and tests to include within each Test Plan. Each BenchTest TestPlan can be configured to run multiple tests on multiple devices simultaneously. Selecting a testsite for a TestBench Plan requires that users select a **Local** testsite or an **Intelligent Design** testsite. The **Local** designation is for testsites that are saved locally and the **Intelligent Design** designation is for testsites from Intelligent Design. Test results are collected and are stored locally and are visible in the Data Viewer. You can view Test Plans by clicking **View** \> **Simple Data Viewer** \> **** on the file menu within the BenchTest application to view the Simple Data Viewer.
-   **[TestBench Instruments](../../id_docs/testbench/benchtest_instruments.md)**  
TestBench in simulator mode supports several instruments and probers that are used to test electrical devices on wafers.
-   **[TestBench Error Messages](../../id_docs/testbench/testbench_error_messages.md)**  
During normal operations errors sometimes occur during TestPlan execution due to configuration issues. This topic addresses potential errors that might occur using TestBench in Simulation mode.
-   **[TestBench Troubleshooting](../../id_docs/testbench/testbench_troubleshooting.md)**  
TestBench in simulation mode must be set up correctly to deliver the correct results. Most unexpected results from TestBench can be diagnosed by verifying that the Switch Matrix is set up properly and by performing probe checks.
-   **[Intelligent Design Jobs in TestBench](../../id_docs/testbench/viewing_intelligent_design_jobs_in_testbench.md)**  
Intelligent Design \(ID\), Intelligent Test \(IT\), and TestBench work together in processing IT test plans. IT testers can send test plans to TestBench for execution. As the test plans run in TestBench, IT users in ID can view the status of all tests plans as they run. In the TestBench app, the Job queue displays details of each job that it received from IT. Test plans ID sends to TestBench are view only and cannot be modified.
-   **[Available Tests](../../id_docs/testbench/available_tests.md)**  
TestBench supports numerous test types.

