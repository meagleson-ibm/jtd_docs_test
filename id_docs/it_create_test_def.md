# Creating a Test Definition

You can create a Test Definition on the Test Definition page of the Intelligent Test app.

To navigate to the Test Definition page:

-   From the Intelligent Design app, click the **Switcher** icon and select **Intelligent Test**.
-   From the Test Plan page, click **Test Definition** from the navigation menu.

**Note:** Only Testers can create, edit, delete, or upload Test Definitions. Test Definitions that are used in a Test Plan cannot be edited or deleted.

1.  On the Test Definition page, click **Create**.

2.  Type a unique **Name**.The name cannot match any other Test Definition already in the system.

3.  Type a **Description** for the Test Plan.

4.  Select a **iltType** for this Test Definition.

5.  Select **iltSubTypes**.

6.  Click **Add Specification**.

7.  Select the **Equipment** from the list.

8.  Select a **Measurement Library** from the list.

9.  Select an **Algorithm** from the list.

    **Note:** If an instrument is associated with the algorithm you select, it displays as read only in the Instrument section.

10. To edit the Input Aspects, Output Aspects, or Device Parameters, click the **Edit** icon in the row you want to change, edit the value, and click the **Done Editing** icon.

11. If @deviceName is used as the input aspect value and a device is selected when creating a test plan, the device will be automatically populated in the corresponding fields in the test plan and the generated TPL. TPLX files. If the format @devicename~suffix is used, the device name will be used followed by the suffix used, for example @deviceName\_test01 would return NEW\_RES\_001~test01, while @device Name would instead return only NEW\_RES\_001

12. Click **Create**.

    **Note:** After you create the Test Definition, you cannot further edit it. The Test Definition is saved, but is not editable.


**Parent topic:**[Test Definition](../id_docs/it_test_definition.md)

