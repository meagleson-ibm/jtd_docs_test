# Die Mapping

Die Mapping allows Intelligent Test users to define, manage and compare Die Maps. You can create die maps by importing a JSON file or manually creating single die map object.

## Die Map JSON Format Guidance

-   **Import Die Maps \(Die Map Table\)**

    -   The **Import Die Maps** function supports importing one or more Die Maps.
    -   Therefore, the JSON file uses an array format \(\[ \]\).
    -   A file downloaded from the Die Map table can be uploaded back through **Import Die Maps** without modification.
    -   System-managed fields, such as **ID**, **Version**, **CreatedBy**, and **CreatedDate** are preserved and supported during import.
-   **Create Die Map → Upload**

    -   The **Create Die Map** function creates a single new Die Map.
    -   Therefore, the upload expects a single JSON object, not a JSON array.
    -   When using a downloaded Die Map file as a template for creating a new Die Map:
        -   Remove the outer array brackets \(\[ \] and\).
        -   Remove system-managed fields such as **ID**, **Version**, and **Audit metadata**.
    -   Uploading the modified file will create a **new Die Map record** rather than updating an existing one.

**Note:**

-   **Import Die Maps** = Import/update one or multiple existing Die Maps \(array format\).
-   **Create Die Map → Upload** = Create a single new Die Map \(single object format\).

-   **[Creating a Die Map](../id_docs/create_die_map.md)**  
You can create a Die Map on the Wafer Definition detail page of the Intelligent Test app.
-   **[Edit a Die Map](../id_docs/edit_die_map.md)**  
Editing a die map allows a user to adjust and correct its details as needed.
-   **[Download a Die Map](../id_docs/download_die_map.md)**  
Downloading a die map allows a user to save a copy for backup or to use for creating other Wafer Definitions..
-   **[Delete a Die Map](../id_docs/delete_die_map.md)**  
Deleting a wafer definition allows a user to clear unused wafer definitions from the wafer management screen..

**Parent topic:**[Wafer Management](../id_docs/wafer_management.md)

