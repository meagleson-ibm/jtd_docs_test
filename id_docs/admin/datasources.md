# DataSources

Data Sources are used in **Service Deployments** when deploying a service. The **DataSources** module enables the Administrator to create and manage these sources.

The following procedure walks through the process of adding and managing Data Sources

1.  Click **DataSources** in the ID Admin Module menu to open the DataSource Management page. This page lists each Data Source, showing its name, description, type, last modification date, and whether it is active or inactive.

    ![Admin Module DataSources](../_images/ID%20Admin%20Sources%2001.png "Admin Module DataSources")

2.  Click **Add DataSource** to open the Add / Edit DataSource pane.

3.  On the pane, click the **Pencil Icon** to make the new datasource editable. Enter a Name and Description for the data source, and set it's active state. Select the DataSource Type and then fill in the Source's URL, Driverclass, and Username and Password where applicable.

4.  Click **Save** to add the new Data Source. Click **Close** to return to the DataSource Management page.

    ![Add / Edit DataSource](../_images/ID%20Admin%20Sources%2002.png "Add / Edit DataSource")

5.  To edit a Data Source, click its row to bring up the Add / Edit DataSource pane. Clicking the **Pencil Icon** makes the Source's fields editable. Clicking **Save** updates the source, and **Close** again returns to the DataSource Management module.

    |Name|Description|Param URL \(adjust to your environment\)|
    |----|-----------|----------------------------------------|
    |DesignData|Intelligent Design Data|jdbc:postgresql://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn?currentSchema=intdsgndata|
    |UserAdmin|User Admin Data|jdbc:postgresql://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn?currentSchema=useradmin|
    |SystemConfig|System Configurtion Data|jdbc:postgresql://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn?currentSchema=systemconfig|
    |ApplicationConfig|Application Configuration Data|jdbc:postgresql://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn?currentSchema=appconfig|
    |PostTestCalculation|PostTest Calculation Data|postgresql+psycopg2://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn?currentSchema=ptc|
    |IntegrationManager|Integration Manager Data|jdbc:postgresql://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn?currentSchema=integrationmgr|
    |Integration-ReportConfig|Report Configuration Data|jdbc:postgresql://intldsgn-db-rw.intldsgn.svc.cluster.local:5432/intldsgn?currentSchema=intdsgnrpt,intdsgndata|


**Parent topic:**[Admin Console Overview](../../id_docs/admin/admin_console_overview.md)

