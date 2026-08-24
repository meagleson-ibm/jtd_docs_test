# TestPlanMgr setup

## Properties on ConfigMgr

In addition to backend service common properties and common-lib properties, the following properties are required for `TestPlanMgr`.

|Configuration key|Purpose|Default value if omitted \(string\)|
|-----------------|-------|-----------------------------------|
|`intldsgn.testplan.tpl.strict`|Specify TPL generation strict mode \(true/false\):-   true – use strict mode. If CenterLine position data is not found, fails with error.
-   false – use debug mode. If CenterLine position data is not found, warning message is generated on TPL.

|false|

Using the config service, assign these parameters in the runtime environment.

-   **[Preparing CenterLine Position data](../../id_docs/installation/centerline_pos_prepare_data.md)**  

-   **[Loading TestCLPos data with API](../../id_docs/installation/testclpos_load_data_api.md)**  

-   **[Embedded variables for Input/Output/Device parameters](../../id_docs/installation/testplan_variables.md)**  


