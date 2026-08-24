# Data source Registration

Register a Test Calculation data source using the Admin Console.

Skip this step if the data source already exists because it has already been registered with a previous release.

Use the information here to construct the data source registration payload. [Instructions to add a data source using the Admin Console](../admin/datasources.md).

DataSource Name: PTC

url = jdbc:postgresql://<server URL\>:<port\>/<database\>?currentSchema=ptc

driverClass = org.postgresql.Driver

username = ???

password = ???

**Parent topic:**[Post Test Calculation deployment](../../id_docs/post_test_calc/ptc_deploy_overview.md)

