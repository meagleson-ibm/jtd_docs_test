# Projects

A Project is an item within a technology that represents the chip being produced. A Technology can include 1 – 10 Projects.

A Project can be a Testsite Project or a Kerf Project. All Macros are created within projects with the project being like a folder that holds the Macros, like files inside a folder. All macros are associated with either a Testsite Project or a Kerf Project. In other words, macros are project-specific . One configuration difference between Testsite projects and Kerf Projects is that Testsite Projects require completion of a Project purpose field. Values that are defined in the Project‑level Purpose field populate a drop‑down list at the Macro level within that Testsite project. If the Project Purpose field is used, a Project Administrator can edit this field during Project Creation or modify it anytime in the life cycle. For Testsite Projects, the Project's level purpose field values are reflected in drop-down menus within macros within the project. Any updates to the Testsite Project level purpose field are reflected in the macros within the project. There are restrictions that are related to deleting Testsite projects that contain the Purpose field and Macros that are created within those projects. See [Editing a Project](edit_project.md) and [Deleting a Project](delete_project.md).

**Note:** Only Project Administrators can create, edit, or delete Projects. See [Editing a Project](edit_project.md) and [Deleting a Project](delete_project.md) for Testsite Project restrictions.

Click a Project name to open details for the Project.

-   **[Creating a Project](../id_docs/create_project.md)**  

-   **[Editing a Project](../id_docs/edit_project.md)**  
Project Administrators can edit Projects on the **All Projects** tab.
-   **[Deleting a Project](../id_docs/delete_project.md)**  
Project Administrators can delete Projects on the **All Projects** tab.
-   **[Project status](../id_docs/project_status.md)**  
Project Administrators can change the status of a project to consistently track project progress, gating, and exceptions across the workflow.
-   **[Project workflows](../id_docs/project_workflows.md)**  
Project workflows define the statuses and gates a project moves through during its lifecycle. Workflows are configured through APIs and selected by Project Administrators in the UI, allowing them to standardize project flows while evolving them over time without disrupting active projects.

