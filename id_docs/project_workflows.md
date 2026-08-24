# Project workflows

Project workflows define the statuses and gates a project moves through during its lifecycle. Workflows are configured through APIs and selected by Project Administrators in the UI, allowing them to standardize project flows while evolving them over time without disrupting active projects.

Workflows are versioned by design. Each update creates a new version, ensuring that existing projects continue using the version they were created with, while new projects automatically use the latest available version.

Status lists define the statuses and gates within a workflow. They are created and updated using the POST /statuslist/save API, with each update generating a new version. If a status list is marked as default, the newest version automatically becomes the default. Deprecated status lists cannot be used in new workflows.

Administrators can view active status lists, all status lists \(including deprecated versions\), and full status and gate details for all versions of a status list.

Workflows associate a project type with a status list and are created using the POST/workflow/create API. Workflows can be set as the default for a project type, always pointing to the latest valid version. Deprecated status lists cannot be used in new or default workflows.

Project Administrators can choose a workflow directly from the UI when creating or editing a project. When creating or editing a project, select the workflow from the Workflow drop-down menu.

**Note:** Only active \(non deprecated\) workflows are displayed. If a default workflow exists, it is preselected.

**Tip:** Administrators can use View workflow to review the workflow structure before applying it.

## List of APIs

New APIs to handle project workflow assignment:

|`POST /statuslist/save`|Save JSON with statuslist name, versions, and data to update. If statuslist unsused update, if in use create new with incremented version.|
|`POST /workflow/assign`|Create workflow \(assigns project to workflow\). Cannot assign deprecated statuslist \(accept Default statuslist\).|
|`POST /workflow/default/{type}/{listname}`|Make a workflow default \(assigns to latest version\). Cannot assign deprecated statuslist.|
|`GET /statuslist/list/active`|Return unique list of statuslists \(based on listname and version\). Do not show deprecated statuslists.|
|`GET /statuslist/list/all`|Return list of statuslists \(listnames and versions\) including deprecated \(for admin/maintenance\).|
|`Get /list/active/{type}`|Get unique list of listnames and default listname based of type \(eg., PROJECT, MACRO\).|
|`GET /statuslist/{listname}/versions/{versions}`|Allows you to retrieve statuslist based on name and versions. \(used for handling deprecated lists\).|

**Parent topic:**[Projects](../id_docs/id_projects.md)

