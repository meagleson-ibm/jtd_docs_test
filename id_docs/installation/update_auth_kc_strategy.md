# Updating Authorization strategy in KeyCloak

1.  Login to Keycloak using an Administrator account.

2.  Switch to the `**intldsgn**` realm.

3.  Click **Clients** in the navigation menu.

4.  Click `**id-application-client**`.

5.  On the **Authorization** tab, select **Permissive** as the **Policy enforcement mode**.

6.  On the **Resources** sub-tab, click **Create resource**.

7.  Enter AllResource as the **Name**.

8.  Enter All Resource as the **Display Name**.

9.  Enter /api/\* in the **URIs** field.

10. Click **Save**.

    `AllResource` is now listed on the **Resources** page.


