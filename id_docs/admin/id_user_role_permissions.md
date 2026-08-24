# ID User Role Permissions

In the Intelligent Design application, user roles define user permissions. Each user has a defined set of permissions that allow or restrict the configuration actions an ID user can take.

User Roles define user permissions and what configuration actions a user can take. In the ID application, users are added to User Role groups. The following table outlines the User Role groups and their associated user permissions.

For Role Permissions specific to Post Test Calculation, see [PTC Admin and User Role Permissions](../post_test_calc/ptc_role_permissions.md). For Role Permissions specific to [Configuration Management](../config_management.md), see [Configuration Management User Role Permissions](config_mgmt_role_permissions.md).

|**User Roles**|
|**Target Entities**|**Features**|**Project Administrator**|**Macro Owner**|**Designer**|**Tester**|**Test Eng Admin**|
|**Technology**|TechnologyAdd|X| | | | |
|TechnologyEdit|X| | | | |
|TechnologyDelete|X| | | | |
|TechnologyView|X|X|X|X| |
|TechnologyStatusChange|X| | | | |
|**Project**|ProjectAdd|X| | | | |
|ProjectEdit|X| | | | |
|ProjectDelete|X| | | | |
|ProjectView|X|X|X|X| |
|ProjectStatusChange|X| | | | |
|**Macro**|MacroClone|X|X|X| | |
|MacroAdd|X|X|X| | |
|MacroCopy|X|X|X| | |
|MacroView|X|X|X|X| |
|MacroEdit|X|X|X| | |
|MacroDelete|X|X|X| | |
|MacroStatusChange|X|X|X| | |
|MacroPort|X| | | | |
|MacroImport|X|X| | | |
|MacroGroup|X|X|X| | |
|MacroUngroup|X|X|X| | |
|MacroGroupImport|X| | | | |
|MacroModules|X|X|X| | |
|MacroLock|X|X|X| | |
|MacroModulesRemove|X|X|X| | |
|TakeSnapshot|X|X|X| | |
|RestoreSnapshot|X|X|X| | |
|**Device**|DeviceAddNew|X|X|X| | |
|DeviceEdit|X|X|X| | |
|DeviceDelete|X|X|X| | |
|DeviceAddPCELL|X|X|X| | |
|**Padset**|PadsetAdd|X| | | | |
|PadsetEdit|X| | | | |
|PadsetDelete|X| | | | |
|PadsetView|X|X|X|X| |
|**Aspect**|AspectAdd|X|X|X| | |
|AspectEdit|X|X|X| | |
|AspectDelete|X|X|X| | |
|AspectUpload|X|X|X| | |
|AspectDownload|X|X|X| | |
|**Team**|CreateTeam|X| | | | |
|EditTeam|X| | | | |
|DeleteTeam|X| | | | |
|ViewTeam|X|X|X|X| |
|IDAdminConfig|X| | | | |
|PTCAdminConfig| | | | | |
|**DRC**|DRCJobView|X|X|X|X|X|
|DRCJobAdd|X|X|X| | |
|DRCJobEdit|X|X|X| | |
|DRCJobDelete|X|X|X| | |
|DRCResultView|X|X|X|X|X|
|DRCResultAdd|X|X|X| | |
|DRCResultDelete|X|X|X| | |
|DRCResultDownload|X|X|X| | |
|**Test Definition**|TestDefinition|X| | |X|X|
|TestDefinitionAdd| | | |X|X|
|TestDefinitionEdit| | | |X|X|
|TestDefinitionView|X| | |X|X|
|TestDefinitionDelete| | | |X|X|
|TestDefinitionCopy| | | |X|X|
|TestDefinitionArchive| | | |X|X|
|TestDefinitionRestore| | | |X|X|
|TestDefinitionExport|X| | |X|X|
|TestDefinitionImport| | | |X|X|
|TestSpecificationAdd| | | |X|X|
|**TestBench**|TestBench|X| | |X|X|
|TestBenchAdd| | | |X|X|
|TestBenchEdit| | | |X|X|
|TestBenchDelete| | | |X|X|
|TestBenchView|X| | |X|X|
|TestBenchSubmit| | | |X|X|
|TestBenchResubmit| | | |X|X|
|TestBenchReportDownload|X| | |X|X|
|**TestPlan**|TestPlan|X| | |X|X|
|TestPlanAdd| | | |X|X|
|TestPlanEdit| | | |X|X|
|TestPlanView|X| | |X|X|
|TestDefnitionEdit| | | |X|X|
|TestPlanDelete| | | |X|X|
|TestPlanCopy| | | |X|X|
|TestPlanArchive| | | |X|X|
|TestPlanRestore| | | |X|X|
|TestPlanArchivedCopy| | | |X|X|
|TestPlanArchivedDelete| | | |X|X|
|TestPlanBulkArchive| | | |X|X|
|TestPlanBulkRestore| | | |X|X|
|TestPlanExport|X| | |X|X|
|TestPlanImport| | | |X|X|
|TestPlanAddDevices| | | |X|X|
|TestPlanGenerateTPL| | | |X|X|
|TestPlanGenerateTPLX| | | |X|X|
|TestPlanRelease| | | |X|X|
|**Wafer Definition**|WaferDefinition|X|X| |X|X|
|WaferDefinitionView|X|X| |X|X|
|WaferDefinitionEdit|X| | | |X|
|WaferDefinitionCreate|X| | | |X|
|WaferDefinitionDelete|X| | | |X|
|DieMapCreate|X| | | |X|
|DieMapEdit|X| | | |X|
|DieMapDelete|X| | | |X|
|DieMapView|X|X| |X|X|
|**Technology Variables**|TechnologyVar| | | | |X|
|TechnologyVarAdd| | | | |X|
|TechnologyVarEdit| | | | |X|
|TechnologyVarView|X|X|X|X|X|
|TechnologyVarDelete| | | | |X|
|TechnologyVarExport| | | | |X|
|TechnologyVarImport| | | | |X|
|**ILT Device Variables**|ILTDeviceVar| | | | |X|
|ILTDeviceVarAdd| | | | |X|
|ILTDeviceVarEdit| | | | |X|
|ILTDeviceVarView|X|X|X|X|X|
|ILTDeviceDelete| | | | |X|
|TechnologyVarExport| | | | |X|
|TechnologyVarImport| | | | |X|

-   **[Configuration Management User Role Permissions](../../id_docs/admin/config_mgmt_role_permissions.md)**  
In the Intelligent Design application, user roles define user permissions. Each user has a defined set of permissions that allow or restrict the configuration actions an ID user can take. The Configuration Management component in Intelligent Test has its own set of permissions for Administrator, Tester, and Test Engineer Admin roles.

**Parent topic:**[ID User Management](../../id_docs/admin/user_management.md)

