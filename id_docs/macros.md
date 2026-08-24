# Macros

Macros are separate sections of semiconductor chips that hold **Devices**. Devices orchestrate the electrical testing of semiconductor chips and is the core technology area. Macro Owners create and configure Macros. Macros can be created inside Testsite Projects **OR** KERF projects. The two types of Macros are not interchangeable and serve different purpose.

The Device contains a core technology that is programmed to perform specialized testing. Macro owners create Macros and Macro designers design how to test the chips using parameters defined on Devices. Each Macro can have up to fifty \(50\) devices depending on the area size and wiring.

There can be different versions of the same Macro, but only one version can be active in a Testsite.

Within projects, Macro Owners administer templates, and configuration and grouping of electrical, optical, and Metrology macros. Macro owners identify and document macro specifications across various components.

-   **[Macro Status Workflow](../id_docs/macro_status_workflow.md)**  
When created, macros are integrated into the Intelligent Design process and follow a defined workflow process. As macros follow this defined workflow process, adjustments to the original macro are often required. Intelligent Design Feature keys dictate which user roles can change each various stages of the workflow process.
-   **[Creating Macros](../id_docs/creating_macros.md)**  
Macro Owners can create Macros in the ID application. All Macros are created within projects with the project being like a folder that holds the Macros. All macros are associated with either a Testsite Project or a Kerf Project. In other words, macros are project-specific.
-   **[Creating Macros - KERF](../id_docs/creating_macros_kerf.md)**  
Macro Owners can create Macros in the ID application.
-   **[Copying Macros](../id_docs/copying_macros.md)**  
Macro Owners can duplicate \(copy\) macros that they created.
-   **[Clone/Edit/Change Status/Lock Macros](../id_docs/clone_edit_change_status_lock_macros.md)**  
Project Administrators, Macro owners and Designers can clone, change status, edit, and lock macros that they created.
-   **[Porting Macros](../id_docs/porting_macros.md)**  
Project Administrators can port macros that they created to another project.
-   **[Coverting Macros into Modules](../id_docs/convert_macros_modules.md)**  
Project Administrators, Macro owners and Designers can convert macros that they created to modules.
-   **[Grouping Macros](../id_docs/grouping_macros.md)**  
Macro owners and Project Administrators can create macro groups containing 2 or 4 macros.
-   **[Importing data from a Reticle Definition File](../id_docs/import_rdf_data.md)**  
Project administrators can import macro aspect data, including X and Y coordinates for each macro in a project, from a Reticle Definition File \(RDF\).
-   **[Viewing changes in a Macro](../id_docs/highlight_edits.md)**  
You can view changed values in any Macro with a status of **Request Complete** or beyond.
-   **[Taking a snapshot of a Macro](../id_docs/take_snapshot.md)**  
You can use the snapshot function to take a snapshot of the state of a Macro and all of its Devices and Padsets at a specific point in time. You can then restore the Macro to the same state at the specific point in time when the snapshot occurred.
-   **[Restoring a Macro from a snapshot](../id_docs/restore_snapshot.md)**  
If you previously created a snapshot of a Macro, you can restore the Macro, including all of its Devices and Padsets, to the exact state it was in at the point in time that you took the snapshot.
-   **[Downloading Macros and Devices](../id_docs/download_macros.md)**  
You can download multiple macros and all associated devices, including all attributes and aspects, in .csv file format.
-   **[Importing Macros and Devices](../id_docs/upload_macros.md)**  
You can quickly create or update Macros and Devices on Testsite macros individually or in bulk in the Macro View by uploading a **csv** file that contains Macro and Device information.
-   **[Deleting a macro](../id_docs/delete_macros.md)**  
Macro owners can delete macros that they own. Deletion is a two-step process and each individual deletion must be confirmed. Deleting macros cannot be undone and removes all associated macro data.

