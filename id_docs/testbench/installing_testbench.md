# Installing TestBench

To enable instrument control in TestBench however the following software should be installed in this order.

**Tip:** To use the offline \(simulator\) version of TestBench, no additional software is necessary. If you are not connecting to actual instruments, you can skip to Step 3.

1.  Download the following files from the vendors:

    -   National Instruments VISA Drivers: [https://www.ni.com/en/support/downloads/drivers/download.ni-visa.html\#558610](https://www.ni.com/en/support/downloads/drivers/download.ni-visa.html#558610)
        -   ni-visa\_24.8\_online.exe
    -   National Instruments 488.2 Drivers: [https://www.ni.com/en/support/downloads/drivers/download.ni-488-2.html\#559044](https://www.ni.com/en/support/downloads/drivers/download.ni-488-2.html#559044)
        -   ni-488.2\_24.5\_online.exe
    -   Keysight IO Library 16.2 or later: [https://www.keysight.com/us/en/lib/software-detail/computer-software/io-libraries-suite-downloads-2175637.html](https://www.keysight.com/us/en/lib/software-detail/computer-software/io-libraries-suite-downloads-2175637.html)
        -   IOLSPrerequisites-21.1.17-windows-x64.exe
        -   IOLibrariesSuiteMain-21.1.17-windows-x64.exe
    -   Keysight B1530A Instrument Library: [https://www.keysight.com/us/en/lib/software-detail/driver/b1530a-wgfmu-instrument-library--sample-programs-2117445.html](https://www.keysight.com/us/en/lib/software-detail/driver/b1530a-wgfmu-instrument-library--sample-programs-2117445.html)
        -   B1530A-Instrument-Library-A.04.00.2440.5403.exe
2.  Run each of the installers in this order:

    **Important:** Follow the instructions in each installer and wait for installation to complete before running the next installer.

    1.  ni-visa\_24.8\_online.exe
    2.  ni-488.2\_24.5\_online.exe
    3.  IOLSPrerequisites-21.1.17-windows-x64.exe
    4.  IOLibrariesSuiteMain-21.1.17-windows-x64.exe
    5.  B1530A-Instrument-Library-A.04.00.2440.5403.exe
3.  Ensure that the installer file SetupTestBench.msi is on the target machine.

    **Tip:** See your provider for access to the installer.

4.  Double-click the installer file and follow the on-screen prompts to finish the installation.

    When the installation is finished, there will be two new folders on the C:\\ drive: C:\\IBM Research\\TestBench and C:\\BenchTest\\TestSiteInfo.

5.  Navigate to C:\\IBM Research\\TestBench and open the TestBench.ini file in a text editor such as Notepad.

6.  Add the following section to the end of the file, filling out each of the sections with the values provided by the IT team:

    ```
    [IntelligentDesignConfiguration]
    BaseURL=https://intldsgn-test.apps.id1.sde.ibm.com
    ClientId=id-application-client
    ClientSecret=0C5NOD5MRM40XwdaVVuyE2j0eyivvQ9w
    KeycloakRealmURL=https://intldsgn-common-keycloak.apps.id1.sde.ibm.com/realms/intldsgn-test/
    ```


The TestBench application should now be ready for use. A shortcut to the application should have been added to the desktop. If not, the program can be started by double-clicking C:\\IBM Research\\TestBench\\TestBench.exe.

-   **[Logging in to TestBench](../../id_docs/testbench/logging_into_testbench.md)**  
 Intelligent Test \(IT\) and TestBench work together in processing IT test plans. IT sends test plans to TestBench for execution. TestBench returns \(in real-time\) the test plan statuses and results to IT where users can view and monitor test plan statuses. After installation, TestBench users are required to log in to the TestBench app, even though the user might already be logged in to ID.

**Parent topic:**[TestBench Overview](../../id_docs/testbench/testbench_overview.md)

