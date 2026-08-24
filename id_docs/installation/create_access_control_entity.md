# Creating the access control entity

Create the access control entity by using the Access Control Manager's Swagger.

1.  Expand `access-control-controller` on Access Control Manager Swagger.

2.  Expand the `POST /access-control/team-access` section.

3.  Click **Try it out**.

4.  Fill in the **Request body** text area with JSON data. entityType is always "project" \(all small cases\).

    **Note:** `entityType` is always `"project"` \(all lower case\). `projectId` and `teamId` were obtained in previous steps.

    ```
    {
    "teamId": {team id},
    "entityType": "project",
    "entityId": {project id}
    }
    ```

5.  Click **Execute**.

    Ensure that the Response has status code 200 and body content includes the data you just posted. Status code values other than 200 indicate an error.


**Parent topic:**[Post data migration steps](../../id_docs/installation/post_migration_steps.md)

