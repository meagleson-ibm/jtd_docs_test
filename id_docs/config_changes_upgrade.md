# Configuration changes from R4

The following changes in configuration were made in Intelligent Design R5.0. Focus on these changes if you are upgrading from ID R4.

-   There is an additional configuration parameter to set in the `[attachmentmgr-svc](admin/adm_attachmentmgr-svc.md)`, `[macromgr-svc](admin/admin_macromgr-svc.md)`, and `[testplanmgr-svc](admin/adm_testplanmgr-svc.md)` service deployments: `server.tomcat.max-swallow-size=-1`.
-   There is an additional configuration parameter to set in the `[testplanmgr-svc](admin/adm_testplanmgr-svc.md)` service deployment: `instrument.terminal.parallel`.
-   There is a new value for the `com.ibm.template.bhtsrch` config paramater in the `[jobexecmgr-svc](admin/admin_jobexecmgr-svc.md)` service deployment.
-   There are 4 new deployment configuration properties in the `[jobexecmgr-svc](admin/admin_jobexecmgr-svc.md)` service deployment.
-   There is a new, optional configuration parameter in the [`0000-common-config-svc`](admin/admin_0000-common-config.md) service deployment: `intldsgn.pcell.aspect-template-group-name`.
-   New instructions for [Preparing WaferProjectMap data](installation/waferprojectmap_prepare_data.md) and [Loading WaferProjectMap data with API](installation/waferprojectmap_load_data_api.md).

