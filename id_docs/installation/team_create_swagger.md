# Creating a team using Swagger

This document illustrates how to setup fictitious users in Swagger, using sample emails with a common email domain like `@example.com`.

1.  Access the **Access Control Manager** Swagger interface on the target system.

2.  Expand `team-controller`.

3.  Expand the `POST /teams` section.

4.  Click **Try it out**.

5.  Fill in the **Request body** text area with `JSON` data:

    -   `“teamName”:` display name of the team being created.
    -   `“description”:` description of the team.
    ```
    {
      "teamName": "My Team 1",
      "description": "My Team 1 is a test team."
    }
    
    ```

6.  Click **Execute**.

7.  Confirm the execution finished with status 200 and the body content includes the data you posted. A status code other than 200 indicates an error..


**Parent topic:**[Team definition](../../id_docs/installation/team_definitions.md)

