# Steps to Execute SQL Script in PostgreSQL on OpenShift - R5.1

Special instructions for Intelligent Design hotfix 5.1.

1.  Download the 2 SQL scripts from the \\src\\main\\resources\\master\_data-sheet folder in the intldsgn-data-application repository.

    1.  Save the iltDeviceCodeVarLookup.sql file to a known local directory.

    2.  Save the technologyvariable.sql file to a known local directory.

2.  Update the `where` condition in the technologyvariable.sql file with the actual `technologyName`.

3.  Open Terminal. Use PowerShell, Git Bash, or any terminal of your choice.

4.  Log in to OpenShift Cluster.

5.  Switch to the correct project.

6.  Navigate to the Script Directory.

7.  Identify the Pod Running PostgreSQL.

8.  Execute the SQL Script:

    ```
    Get-Content .\iltDeviceCodeVarLookup.sql | oc exec -i <POD_NAME> -- psql -U <DB_USERNAME> -d <DB_NAME>
    Get-Content .\technologyvariable.sql | oc exec -i <POD_NAME> -- psql -U <DB_USERNAME> -d <DB_NAME>
    
    ```

    Replace:

    -   `<POD\_NAME\>` with your PostgreSQL pod name
    -   `<DB\_USERNAME\>` with your database username
    -   `<DB\_NAME\>` with your database name

