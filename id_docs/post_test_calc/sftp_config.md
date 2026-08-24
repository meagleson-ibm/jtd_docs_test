# SFTP-based ISDW automated delivery configuration

To enable reloading TEDs test files and communication with the ISDW database, you must configure an SFTP connection with a password or passkey.

Only users with Post Test Calculation administrative rights can perform this task.

1.  In the Post Test Calculation application, click the profile icon and select **Administration configuration**.

2.  Click **SFTP Config**.

3.  Enter the **Host** name, **Port**, and **User Name**.

    The Host Name and port number define the basic connectivity to the target SFTP server where the ISDW ETL resides.

4.  Enter the **Normal Priority Directory** and a **Low Priority Directory** to transfer TEDs files to the ISDW database.

5.  Enter either a **Password** or an SSH **Passkey**.

    1.  If you are using an SSH passkey, you can enter the **Passkey Password** here also.

    **Note:** If you enter both a **Password** and **Passkey**, the passkey is used.

6.  Set the **Enabled** switch to **On**, and click **Save**.

    TEDS files that are produced through the recalculation process are delivered to the low priority processing directory per the configuration above. The rationale for this is not to overwhelm the ISDW ETL processing with potentially high volumes of updated TEDs files that could potentially delay most recently post calculated TEDs files.


**Parent topic:**[Administration configuration](../../id_docs/post_test_calc/admin_config.md)

**Related information**  


[Reload data to recalculate test results](reload_teds_data.md)

