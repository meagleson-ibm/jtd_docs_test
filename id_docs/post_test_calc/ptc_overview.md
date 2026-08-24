# Post Test Calculation

The Post Test Calculation system is designed to enrich semiconductor in-line electrical test data with a post processor before it is sent to downstream consumers. The enrichment consists of the addition of parameter specification metadata, parameter result categorization, and calculated parameters.

The device under test creates a test plan \(TPL\), which is fed into the hardware tester. After the test is completed, the Post Test Calculation begins.

All measurements done in the testing device are added to a Transducer Electronic Data Sheet \(TEDS\) file. This file goes into Test Plan Manager, which transfers the TEDS file \(via FSTP\) to the Post Test Calculation application.

Test File Purveyor Agent kicks off the Post Test Calculation pipeline. Post Test Calculation parses the file and starts aggregate calculations per lot, then updates the Postgres DB with the data.

Aggregate data is written to a TEDS output report.

Disposition Manager performs disposition rule test - results = Pass or Hold. Decision is communicated to SiView.

-   **[Post Test Calculation design architecture](../../id_docs/post_test_calc/ptc_architecture.md)**  
The following diagrams provide an overview of the Post Test Calculation design architecture.
-   **[Test Results](../../id_docs/post_test_calc/test_results_page.md)**  
When you log in to the Post Test Calculation application, the landing page opens. It is the entry point into the Post Test Calculation application.
-   **[Viewing Lot Data](../../id_docs/post_test_calc/view_lot_data.md)**  
You can view chip-level data measurements from the Test Results and analyze the results to be used for specifications, calculations and disposition.
-   **[Viewing Wafer Data](../../id_docs/post_test_calc/view_wafer_data.md)**  

-   **[Viewing chip-level test results](../../id_docs/post_test_calc/view_chip-level_params.md)**  
You can view details of the test results for each parameter at the chip level.
-   **[Viewing Calculations](../../id_docs/post_test_calc/view_calculations.md)**  
Post Test Calculation automatically performs new aggregate calculations on new collections of parameter values so that a user can analyze the overall trends and characteristics of a dataset by combining multiple parameter values.
-   **[Navigating to Disposition Pages](../../id_docs/post_test_calc/navigating_to_disposition_pages.md)**  
To view, create, and edit lot and wafer dispositions, you need to navigate to the Disposition landing pages using the procedure below.
-   **[Administration configuration](../../id_docs/post_test_calc/admin_config.md)**  
To configure SiView disposition and STFP configuration, click your profile icon, then select **Administration configuration**.

