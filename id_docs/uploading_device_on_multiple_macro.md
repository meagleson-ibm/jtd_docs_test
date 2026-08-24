# Uploading Devices on Multiple Macros

You can quickly create or update Macros and Devices on Testsite macros individually or in bulk in the Macro View by uploading a **Devices-only-csv** file. The **Devices-only-csv** file contains only Device information. When uploading using the **Devices-only-csv** file, devices are added to macros that do not have devices and can also be added to Macros named in the **Devices-only-csv**. Users must follow the .csv import rules and adhere to restrictions when importing macros and devices.

CSV File Structure

-   Each row represents a unique Macro or Device.
-   The file can contain only Macro attributes and aspects or Macro + Device attributes and aspects and pad assignments.
-   Modules and groups cannot be imported by using CSV.
-   If devices are included, the system automatically assigns them to the correct Macro based on the Macro Name.
-   You can add new aspects impromptu by including them in the file.
-   Optional fields must be present but can be null.
-   Custom Fields are only added when values are provided. Custom fields are ignored if empty. If Macros are being updated, custom fields are reset based on .csv content

The following tables outline the **Field Requirements**, **Validation Rules**, and **Error Handling**.

|MacroName|≤ 500 characters|
|Description|≤ 100 characters|
|Priority|Must be one of the following: -   high
-   medium
-   low
-   critical
-   experimental

|
|Macro Status|Must match valid system status values|

|Mandatory Fields|If any required fields are missing, the system displays an error message and you can download a gap file that lists items that failed validation for correction.|
|Invalid Values|The system specifies which field is invalid and the row number where the error occurred.|
|Duplicate Entries in File|Prompted as an error before processing.|
|Existing Macros/Devices|If the name exists, the record is updated. If not, a new record is inserted.|

|Missing fields|Line item displays an error and upload is rejected.|
|Invalid values|Rows with out-of-range or malformed data are highlighted.|
|Duplicate entries|If a macro or device exists, the user is prompted to update or skip.|

Best practices for preparing your .csv file

-   Acquire the sample template first from your project administrator, or [download the Macros/Devices you want to update](download_macros.md).
-   Use consistent naming for Macros and Devices to avoid unintended updates.
-   Validate field values by ensuring that they match allowed values, and check character limits for MacroName and Description.
-   Avoid duplicates within the file.
-   Include all mandatory fields before upload.
-   Add aspects carefully: New aspects can be added impromptu, but must follow naming conventions.
-   Save the file in UTF-8 encoding to prevent special character issues.
-   Test with a small batch first before you upload large files.
-   If using PCELL data, it is recommended to use a file for each PCELL.

How **Import** works.

-   **No Existing Macros**

    The system displays an error that indicates that a Macro does not exist in Intelligent Design. An **Invalid Device Mapping** error displays.


-   **Macros Exist with No Devices**

    Using the **macroName** Field in the csv, devices on the specified Macros are inserted. The system validate devices based on:

    -   Required fields must be present in the csv and contain valid values.
    -   Optional Standard Fields must be present in the csv and contain either a valid value or be null.
    -   Custom Fields in the csv are added if the value is not null.

-   **Mixed Content of Existing Macros and New Macros**

    Using the **macroName**Field in the csv, existing Macros are updated and new Macros are inserted only if the Macro data is included in the csv along with the device information. Devices are replaced where they exist and validated as follows:

    -   Required fields must be present in the csv and must have a valid value
    -   Optional Standard Fields must be present in the csv and contain either a valid value or be null.
    -   Custom Fields in the csv are added if the value is not null.

**Note:** The **macroName** field in the **Devices-only-csv** must contain a valid value \(macro name\).

1.  On the **Macro View** tab, click the Multiple Macro Import icon. ![Upload multiple macros](_images/multi_macro_upload_icon.jpg)

    The Import screen opens.

    ![Viewing the Import Macro](_images/import_macro_csv_1.jpg "Viewing the
    Import Macro ")

2.  Click **Select File** and browse to the .csv file. Click **Open**.

    ![Viewing the Macro Import Device Only](_images/import_macro_desvice_only_csv_SelectFile.jpg "Viewing the Macro Import Device Only ")

3.  Click **Validate** to validate the .csv and the devices within the .csv file.

    ![Viewing Valdation Response for Devices Only csv](_images/import_macro_desvice_only_csv_Validation.jpg "Viewing Valdation Response for Devices Only csv ")

    **Note:** The Validation preview presents the **Warnings and Errors** status of the import and the potential impact on existing devices. Hover over the reason column to see warning details. Make adjustments if necessary.

    ![](_images/import_macro_desvice_only_csv_Validation_HoverText.jpg)

4.  Click **Import** to complete the import. The imported and updated Marco and Devices display.


After a successful upload, the newly created or modified Macro appears at the top of the list. A system notification confirms a successful import. Click **View Update** to browse to the updated Macro View. See [Taking a snapshot of a Macro](take_snapshot.md) snapshots to learn more about snapshots.

![Viewing the Successful Import with Devices Only csv](_images/import_devicesonly_csv_Import_Successful_Message.jpg "Viewing
the Successful Import with Devices Only csv")

**Parent topic:**[Importing Macros and Devices](../id_docs/upload_macros.md)

