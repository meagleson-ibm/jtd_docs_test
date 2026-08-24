# TestBench Troubleshooting

TestBench in simulation mode must be set up correctly to deliver the correct results. Most unexpected results from TestBench can be diagnosed by verifying that the Switch Matrix is set up properly and by performing probe checks.

**Switch Matrix Misconfigurations**

Use these steps to verify correct Switch Matrix configuration.

1.  Check the Switch Matrix connections and set up.
2.  Run a probe check test.
3.  Check that the TestBench is moving the prober to the designated macro.
4.  Check probe alignment.

**Testsite Misconfiguration**

A condition that might occur during TestBench testing is that the Cascade S300 Prober doesn't move to test the designated dies. If die size is entered incorrectly in the testsite, the Cascade S300 might be unable to detect \(locate\) the die. To rectify this situation, you need to confirm the die size is correct in the testsite. Sometimes when a new die size is entered into BenchTest, the value is rounded to the nearest integer but die sizes must be entered as units of millimeters \(mm\). Probers like the Cascade S300, detect only die sizes in units of mm.

To check the die size in a TestBench testsite, the testsite name must be temporarily changed to an alternate name so the die size can be checked and corrected if necessary. When the die size is correctly entered the original name of the testsite can be reinstated.

1.  Browse to the folder where the testsites are stored \(C:/BenchTest/TestSiteInfo/\) and change the testsite folder name to an arbitary name \(Avatar to Avatar\_Temp\). Take a screen capture of the old testsite for reference when you create the temporary testsite.
2.  Using TestSite Manager enter in the correct information including the correct die size in mm.
3.  Copy the devices information .csv file from the old testsite to the new testsite. Move Avatar\_Devices.csv from Avatar Temp to Avatar.
4.  Remove \(delete\) the old testsite \(Avatar\_Temp\).
5.  To have the changes take effect in BenchTest, select a different testsite in the testplan and then select the Avatar \(corrected\) testsite.

**Parent topic:**[TestBench Overview](../../id_docs/testbench/testbench_overview.md)

