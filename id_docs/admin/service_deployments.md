# Service Deployments

Admins use **Service Deployments** to register and assign applications for use in Intelligent Design. Applications are registered in the **Serivce View** and their deployments are tracked and modified in the **Deployments View.**

You must [register and deploy the config-svc service](../installation/config_svc.md) using the **Swagger API** before you can deploy the Admin Console.

The following procedure walks through the process of registering and tracking Application Services and their deployments.

1.  Click **Serivce Deployments** in the ID Admin Module menu to open Service Deployments to the Services View tab. The tab displays each currently registered application, including a description, its type, and a modification date.

    ![Admin Module Services View](../_images/ID%20Admin%20Services%2001.png "Admin Module Services View")

2.  Click **Add** to open the Add or Update Application Service Information window.

3.  Enter a Service Name, select ether the Service Type, either system or application, and enter a Description. Then click **Save** to add the Service to the list. Click **Close** to return to the service view.

    ![Add or Update Application Service Information](../_images/ID%20Admin%20Services%2002.png "Add or Update Application Service Information")

4.  To Edit a Service, click the **Hamburger menu** and select **Edit** from the menu to open the Add or Update Application Service Information window. Changing information and clicking **Save** updates the service. Clicking **Close** again closes the window.

5.  To delete a service, click the **Hamburger menu** and select **Delete**. On the window the appears, click **Confirm** to delete the service and return to the Services View.

6.  To add a Deployment for a service, first click the **Carat** by the Service's name, then click **Add Deployment** to open the Add or Update a Deployment for Service window.

    ![Add Deployment](../_images/ID%20Admin%20Services%2003.png "Add Deployment")

7.  On the Add or Update a Deployment for Service window, there are three tabs that can be filled with information on the deployment. On the Info tab, the Deployment's Title, Label, content, and internal and external URLs must be filled in where applicable, whether or not the deployment uses a data source, if security is enabled, and if the deployment is active. Environmental Variables such as server port, service version, security and system level statecan be added on the Properties tab, and if being used, the data source can be selected on the DataSources tab. The available Data Sources are selected via a drop down list of Data Sources Defined in the [DataSources](datasources.md) module.

    ![Add or Update a Deployment for Service](../_images/ID%20Admin%20Services%2004.png "Add or Update a Deployment for Service")

8.  Once created, a deployment can be viewed beneath the service it is associated with, or on the Deployments View tab. This tab shows each Deployment, listing its name, profile, label, the service it is associated with, whether or not it is active, and its last modified date.

    ![Admin Module Deployments View](../_images/ID%20Admin%20Services%2005.png "Admin Module Deployments View")

9.  To edit a deployment, mouse over the deployment to reveal and then click the **Hamburger menu** and select **Edit** to open the Add or Update a Deployment for Service. This window has the same functions as it did when creating the deployment. Clicking **Save** updates the Deployment and **Close** returns to the Deployments View.

10. To ensure an updated deployment syncs to its associated service, mouse over the deployment to reveal and then click the **Hamburger menu** and select **Sync Changes**. Restart the target service's pod to load the deployment.

11. To delete a deployment, mouse over the deployment to reveal and then click the **Hamburger menu** and select **Delete** to open the Confirm Deletion window. Click **Confirm** to delete the deployment.


-   **[0000-common-config application service information](../../id_docs/admin/admin_0000-common-config.md)**  
Use the following information to deploy the `0000-common-config` application service.
-   **[projectmgr-svc application service information](../../id_docs/admin/admin_projectmgr-svc.md)**  
Use the following information to deploy the projectmgr-svc application service.
-   **[macromgr-svc application service information](../../id_docs/admin/admin_macromgr-svc.md)**  
Use the following information to deploy the macromgr-svc application service.
-   **[aspectmgr-svc application service information](../../id_docs/admin/adm_aspectmgr-svc.md)**  
Use the following information to deploy the aspectmgr-svc application service.
-   **[listvaluemgr-svc application service information](../../id_docs/admin/adm_listvaluemgr-svc.md)**  
Use the following information to deploy the listvaluemgr-svc application service.
-   **[attachmentmgr-svc application service information](../../id_docs/admin/adm_attachmentmgr-svc.md)**  
Use the following information to deploy the attachmentmgr-svc application service.
-   **[usermgr-svc application service information](../../id_docs/admin/adm_usermgr-svc.md)**  
Use the following information to deploy the usermgr-svc application service.
-   **[accessctlmgr-svc application service information](../../id_docs/admin/adm_accessctlmgr-svc.md)**  
Use the following information to deploy the accessctlmgr-svc application service.
-   **[testplanmgr-svc application service information](../../id_docs/admin/adm_testplanmgr-svc.md)**  
Use the following information to deploy the testplanmgr-svc application service.
-   **[diewafermgr-svc application service information](../../id_docs/admin/adm_diewafermgr-svc.md)**  
Use the following information to deploy the diewafermgr-svc application service.
-   **[equipmentmgr-svc application service information](../../id_docs/admin/adm_equipmentmgr-svc.md)**  
Use the following information to deploy the equipmentmgr-svc application service.
-   **[web-ui application service information](../../id_docs/admin/adm_web-ui.md)**  
Use the following information to deploy the web-ui application service.
-   **[intellifabtest-ui application service information](../../id_docs/admin/admin_intellifabtest-ui.md)**  
Use the following information to deploy the intellifabtest-ui application service.
-   **[jobexecmgr-svc application service information](../../id_docs/admin/admin_jobexecmgr-svc.md)**  
Use the following information to deploy the jobexecmgr-svc application service.
-   **[jobresponsemgr-svc application service information](../../id_docs/admin/admin_jobresponsemgr-svc.md)**  
Use the following information to deploy the jobresponsemgr-svc application service.
-   **[integrationmgr-svc application service information](../../id_docs/admin/adm_Integrationmgr-svc.md)**  
Use the following information to deploy the integrationmgr-svc application service.
-   **[integrationpod-svc application service information](../../id_docs/admin/adm_integrationpod-svc.md)**  
Use the following information to deploy the integrationpod-svc application service.
-   **[reportingdashboard-svc application service information](../../id_docs/admin/admin_reportgindashboard-svc.md)**  
Use the following information to deploy the reportingdashboard-svc application service.
-   **[searchmgr-svc application service information](../../id_docs/admin/adm_searchmgr-svc.md)**  
Use the following information to deploy the searchmgr-svc application service.
-   **[userdetail-svc application service information](../../id_docs/admin/admin_userdetail-svc.md)**  
Use the following information to deploy the `userdetail-svc` application service.
-   **[masterdata-svc application service information](../../id_docs/admin/admin_masterdata-svc.md)**  
Use the following information to deploy the `masterdata-svc` application service.
-   **[design-svc application service information](../../id_docs/admin/admin_design-svc.md)**  
Use the following information to deploy the `design-svc` application service.
-   **[testing-svc application service information](../../id_docs/admin/admin_testing-svc.md)**  
Use the following information to deploy the `testing-svc` application service.
-   **[testingresource-svc application service information](../../id_docs/admin/admin_testingresource-svc.md)**  
Use the following information to deploy the `testingresource-svc` application service.

**Parent topic:**[Admin Console Overview](../../id_docs/admin/admin_console_overview.md)

