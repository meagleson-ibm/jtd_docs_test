# Accessing the database to get the project ID of deployed data

Access the database to get the project ID of deployed data. Services' API, including Swagger, cannot obtain the data, so you must access the DB directly.

1.  Connect to the database directly.

    Example:

    ```
    % oc port-forward svc/intldsgn-db-rw 5432:5432
    ```

    ```
    % psql -h localhost -p 5432 -d intldsgn -U intldsgnapp
    ```

2.  Obtain the ID of the target project.

    Example:

    ```
    intldsgn=> select id,name from intdsgndata.project;
    id | name
    -----+----------------------------------------------
    1 | Project name
    ```


**Parent topic:**[Post data migration steps](../../id_docs/installation/post_migration_steps.md)

