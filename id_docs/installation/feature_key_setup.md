# Setting up Feature Keys

Obtain the *Feature Key definition* Excel file as a specification.

1.  Log in to the Keycloak admin console using your GitHub button and w3id SSO login.

2.  Switch to the `intldsgn` realm.

3.  Select **Clients** in the navigation menu.

4.  Click **id-application-client** in the Client ID table.

5.  On the **Authorization** tab, select the **Resources** sub tab.

6.  Repeat the steps for each feature listed in the Excel file.

    Example \(AspectAdd\):

    1.  Create **AspectAdd** resource in the **Resources** tab.

    2.  Create **AspectAdd\_Role\_Policy** in **Policies** \(Role-based policy\)

        -   Add **Role** button to assign roles based on Excel sheet.
    3.  Create **AspectAdd\_Resource\_Permission** in **Permissions** \(Resource-based permission, Affirmative\).

        -   Set AspectAdd as the **Resource**.
        -   Set AspectAdd\_Role\_Policy as the **Policy**.
        **Tip:** Make sure you click **Save** each time, then click **Cancel** to return to the list.


**Note:** After user permissions are changed, restart `intldsgn-accessctlmgr`'s pod. OpenShift's rollout command is recommended.

```
> oc rollout restart deployment intldsgn-accessctlmgr
```

**Parent topic:**[Defining user permissions](../../id_docs/installation/user_permissions.md)

