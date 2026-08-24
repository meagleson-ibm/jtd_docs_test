# Keithley TSP

The Generic Keithley TSP tests are performed via TSP Lua programming scripts downloaded to Keithley 2600 series instruments. Test control itself is done on the Keithley 2600 which allows for fast execution as little to no communication overhead is needed during the test. User written TSP scripts can be executed by TestBench and the data retrieved and stored using the standard data file format of other TestBench tests.

A standard TSP is HCI.tsp. This test is used to measure FET degradation due to hot-carrier-injection. Changes in the FET parameters Vt, Ioff, Idsat, Igsat, Idlin, Iglin, Ieff, Ioff are measured during stress.

-   **[Configure a TSP](../../id_docs/testbench/configure_a_tsp.md)**  
The process of configuring a TSP test to be run via TestBench

**Parent topic:**[Available Tests](../../id_docs/testbench/available_tests.md)

