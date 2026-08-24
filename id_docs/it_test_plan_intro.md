# Test Plan

Test Plan is used to create a TPL file to communicate to a testing device which devices and macros to run tests on and the order in which to run the tests. Test plan creation now requires ID user to specify macro test sides, **Frontside** or **Grindside**. Selecting **Frontside** means that macros marked as **Front** or **Both** are available for selection. Selecting **Grindside** only macros marked as **Both** are available for selection.

Test Plan access respects macro and device restrictions are defined at the project and team level. Each macro can be configured using the **Restricted to** field to limit its visibility and usage to specific teams.

**Note:** Users who are on teams that are assigned to the project that is referenced in a Test Plan are the only ones who can view, edit, delete, export, import, or archive the Test Plan.

-   **[Creating a Test Plan](../id_docs/it_create_test_plan.md)**  
You can create a Test Plan on the Test Plan page of the Intelligent Test app. Users cannot create or view test plans that include macros or devices that are restricted to other teams. If macro restrictions are updated, the changes are automatically refreshed. Test plan creation now requires ID user to specify macro test sides, **Frontside**, or **Grindside**. Selecting **Frontside** means that macros marked as **Front** or **Both** are available for selection. Selecting **Grindside** only macros marked as **Both** are available for selection.
-   **[Editing a Test Plan](../id_docs/it_edit_test_plan.md)**  
You can edit an existing Test Plan on the Test Plan page of the Intelligent Test app. As with test plan creation, users cannot view or edit test plans that include macros or devices that are restricted to other teams. If macro restrictions are updated, the changes are automatically refreshed. Test plans now can contain **Frontside** and **Grindside** macros. Users can edit **Test Plans** and change macros within that Plan. When the macro testing sides are edited and updated, the system must **reapplies** filtering and **validates the edited macro selections** to ensure that the edited macros are compliant with the selected testing side.
-   **[Managing Devices in Test Plans](../id_docs/tesplandevices.md)**  
Multiple Devices can be added to a Test Plan, each with its own Macro and Die Map. When a user accesses a Test Plan, the user can only view and select macros and devices that their team is authorized to access. Restricted macros and their associated devices are not displayed in the device selection table or any related selection modals.
-   **[Duplicating test tasks in a test plan](../id_docs/duplicate_test_tasks.md)**  
Testers can duplicate one or multiple test tasks within the test plan creation interface to save time and effort when creating test plans.
-   **[Deleting a Test Plan](../id_docs/it_delete_test_plan.md)**  
You can delete an existing Test Plan on the Test Plan page of the Intelligent Test app.
-   **[Exporting Test Plans](../id_docs/it_export_test_plan.md)**  
You can export Test Plans on the Test Plan page to a .csv formatted file.
-   **[Importing Test Plans](../id_docs/importing_test_plans.md)**  
You can import Test Plans by using a properly formatted .csv file that contains the required Test Plan fields.
-   **[Upload Bulk Test Plans](../id_docs/upload_bulk_test_plans.md)**  
You can upload Bulk Test Plans on the Test Plan page by uploading a properly formatted .csv file that contains the required Test Plan fields.
-   **[Copying a Test Plan](../id_docs/it_copy_test_plan.md)**  
You can copy any existing Test Plan on the Test Plan page, regardless of its status.
-   **[Parallelism support in Test Plans](../id_docs/it_parallelism_support.md)**  
This feature introduces parallelism support within Test Plans, specifically targeting the P9000 Test System Synchronous \(Sequence-based\) Parallelism. It allows test engineers to specify which device-test combinations can be executed simultaneously during a macro by assigning a matching parallelism label.
-   **[Modifying Test Definitions on the Fly](../id_docs/modifying_test_definitions_on_the_fly.md)**  
During Test Plan testing, modifying test definitions within a **Draft Test Plan** can provide testers with insight into Test Plan results. This feature gives testers a one-time \(on the fly\) opportunity to modify the Test Definition within a **Draft Test Plan**. This one-time modification does not alter the original Test Plan and is not saved for future use. Changes are applied only within the context of the current Test Plan.
-   **[Archiving a test plan](../id_docs/it_archive_test_plan.md)**  
When a Test Plan is outdated or no longer used, you can archive it to remove it from your daily view.

**Parent topic:**[Intelligent Test](../id_docs/intelligent_test_intro.md)

