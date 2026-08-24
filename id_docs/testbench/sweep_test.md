# Sweep Test

The Generic Sweep Test is designed to execute sweeps on any device terminal using any instrument terminal. The Generic Sweep Test will allow any sweep depth and any terminal property \(except lists\) to be swept. The flexibility of the Generic Sweep test allows for many standard characterization tests to be configured.

Below is an example list of tests that can be configured using the Generic Sweep Test:

-   **FET IgVg**

    Gate Current vs Gate Voltage sweeps.

-   **FET IdVg**

    Drain Current vs Gate Voltage to extract Vtlin, VtSat, SSlin, SSsat, Idsat, Idlin, Ioff etc.

-   **FET IdVd**

    Drain Current vs Drain Voltage at various gate biases to extract Ron etc.

-   **FET CV**

    Capacitance vs Voltage to extract Cinv, Q, Vt, etc.

-   **FET Charge Pumping**

    Extract Nit.

-   **FET Dit using Conductance**

    Extract Dot.

-   **FET Minority Carrier Mobility**

    Using a combination of IdVg and CV carrier mobility can be extracted.


-   **[Configure a Sweep Test](../../id_docs/testbench/configure_a_sweep_test.md)**  


**Parent topic:**[Available Tests](../../id_docs/testbench/available_tests.md)

