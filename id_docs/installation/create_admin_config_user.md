# Creating an admin configuration user

After you install keycloak, you must create a "super user" who can configure the Intelligent Design application using the Admin Console.

Only users with this system admin role can access the [Admin Console](../admin/admin_console_overview.md).

1.  Login to the OpenShift Console.

2.  Switch to the project where Keycloak is deployed.

3.  Navigate to **Workloads** \> **Pods**.

4.  Click **Keycloak Pod**, then click **Terminal link**.

5.  Run the following command to set HOME:

    `export HOME=/opt/keycloak`

6.  Login to keycloak through POD Terminal using default admin credentials provided by keycloak for every installation.

    `/opt/keycloak/bin/kcadm.sh config credentials --server http://localhost:8080 --realm master --user admin --password '<PASSWORD>' --client admin-cli`

7.  Run the following command to create a Realm named intellifab. \(Realm can be any valid name.\)

    `/opt/keycloak/bin/kcadm.sh create realms -s realm=intellifab -s enabled=true`

8.  Run the following command to create role named Administrator. \(Role can be any valid name.\)

    `/opt/keycloak/bin/kcadm.sh create roles -r intellifab -s name=Administrator`

9.  Run the following command to create a user named superadmin with password superadmin. \(Username and Password can be anything.\)

    ```
    /opt/keycloak/bin//kcadm.sh create users -r intellifab \
    -s username=superadmin \
    -s enabled=true \
    -s email=superadmin@example.com \
    -s firstName=superadmin \
    -s lastName=superadmin 
    ```

10. Get user ID first:

    ```
    USER_ID=$(/opt/keycloak/bin/kcadm.sh get users -r intellifab -q username=superadmin --fields id \
    | sed -n 's/.*"id"[[:space:]]*:[[:space:]]*"\([^"]*\)".*/\1/p' \
    | head -1)
    ```

11. Set password \(not temporary\).

    `/opt/keycloak/bin/kcadm.sh set-password -r intellifab --userid $USER_ID --new-password superadmin`

12. Run the following command to link user superadmin to Administrator role:

    `/opt/keycloak/bin/kcadm.sh add-roles --uusername superadmin --rolename Administrator -r intellifab`

13. Login to IntelliFab [Admin Console](../admin/admin_console_overview.md) and configure ID Applications.


**Parent topic:**[Configuring Realm of keycloak - Manual](../../id_docs/installation/config_realm_keycloak_manual.md)

