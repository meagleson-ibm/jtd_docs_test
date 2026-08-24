# Update PTC backend components environment

Beginning with the 7.0 release, the following environment variables should be present for all backend component for them to be able to acquire their configuration correctly:

-   `spring.application.name`: The name of the application used when creating the App Service Registration
-   `spring.cloud.config.username`: The username for interacting with the config service
-   `spring.cloud.config.password`: The password for interacting with the config service
-   `spring.config.import`: The configuration service URL
-   `com.ibm.iw.service.datasource.url`: The URL for retrieving the datasource
-   `spring.cloud.config.profile`: The profile of the service deployment
-   `spring.cloud.config.label`: The label of the service deployment

**Parent topic:**[Post Test Calculation deployment](../../id_docs/post_test_calc/ptc_deploy_overview.md)

