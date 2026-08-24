# TestBench System Test

The TestBench System Test verifies the Switch Matrix Configuration by checking the connections through the switch matrix.

The TestBench System Test verifies the Switch Matrix Configuration by checking the connections through the switch matrix. The system test requires that a custom harness is added to the Switch Matrix and the harness configuration is in the TestBench.ini file. The system test detects if the Source Measure Units \(SMU\) force the correct current \(voltage\) and if the guard operates as expected.

## Before You Start

To Prepare for the System Test you need to gather

-   A special cable harness that separates the guard and the signal of a Triax connection is required. To connect this cable to the switch matrix, the guard \(of the switch matrix\) must be dropped by using Triax to BNC \(standard\) adapters that float the guard. A shorting plug is also used for signal path verification.

    **Note:** SMUs can have what is a triax connector instead of BNC. A triax connector is composed of three sections. Signal, Guard, and Shield. A BNC \(coaxial\) cable connects only has two parts: Signal and shield. This test checks that the voltage applied to the guard is correct.

    The following is a list of required items:

    -   1x TRB Male to Dual BNC w/ shields tied together cable \([eBay](https://www.ebay.com/itm/286045010866?_trksid=p2332490.c101875.m1851&itmprp=cksum%3A28604501086602fbb61768614c7ca828f6d0591b9858%7Cenc%3AAQAKAAABYHKEKKNMUePryBh1zZl0qrjonWK6%252Bbjh8v6%252FxTRbw1Loxqx736BoO2V7ozv6W4xuOBJjwGhPLWk9lnRB2teM6PFgOrZGVcTwpTth7MW79p066SWQrB1VasW1Di58xl1RMBXsH%252BaNxpzil0t8bdqbPkgJlZgvtHVYNSkxo5xG%252Bq21fR58PrKVkPu4o3XzVubLGuYuFTsDUtDT5BIm3O5FFkWbhJc2pallGR%252FYJgAyZsKy%252FlZsmCJmWH405gCLb2UgSWIQ6c9c%252BiseuSsk2An2VqNt88pNjaWoVuNWb6hnGB6JVeRXhz12YFKv2E7j6Q6buprGMGJq%252FYB2pFK4c4kIsd4TsEI%252FocEjQmK9b0%252BMcHUIAvJT8cRaV0JWMvLWAug2Fn5h%252BqTb84%252BtwSx5EmeBctrKZI%252B5ytfj2iAINN%252FSJIIzrfOWlErA3DrdAd6jTKAPjzwoDVTiA3FYHOEY%252FXdVMkw%253D%7Campid%3APL_CLK%7Cclp%3A2332490&itmmeta=01JPN4DMCP8AFYX9CTQDFE2F9M)\)
    -   3x Traix to BNC adapter that floats the guard \(P/N\# ADBJ20-E2-PL75\)
    -   1x BNC shorting cap

## System Test Configuration

The harness and adapters need to be added to the columns \(same as used for probecard pins\) of the switch matrix as shown in the following figure.

![Switch Matrix Cable Harness](../_images/testbench_switchmatrixcableharness.jpg "Switch Matrix Cable
Harness ")

The following figure shows the System Test Configuration of the cable harness and shorting plug.

**System Test Cable Connections**

```
systestTriaxOutputPort=Triax Side of Triax to bnc cable (blue cable (9) in picture)
systestForceBNCPort=Force BNC of the triax to bnc cable (red cable (10) in picture)
systestGuardBNCPort=Guard BNC of the triax to bnc cable (black cable (11) in picture)
systestGroundPort=triax to bnc adapter x/bnc shorting cap (column 12 in picture)
```

Edit the TestBench.ini file in Notepad as shown in the SystemTest section configuring the output port of each cable harness port and shoring plug as shown in the following code example.

![Example TestBench.ini Section for System Test](../_images/testbench_systemtest_code_example.jpg "Example TestBench.ini file Section for System
Test ")

**Parent topic:**[TestBench Instruments](../../id_docs/testbench/benchtest_instruments.md)

