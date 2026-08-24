# Data configuration for R5.0

Data configuration steps for equipment with Probe, Instruments, Measurement Libraries, and Algorithms.

1.  Download the macro-enabled Excel worksheet Config\_Eqp\_Mlib\_Algo\_Probe\_Inst.xlsm.

2.  Update and verify the data as needed in each tab of the above worksheet.

3.  On the **Generate\_SQL** tab, enter the full file path to where you want to save the generated SQL file, and click **Generate\_SQL**.

    This generates the SQL for the data provided in each tab.

4.  Open the generated SQL file in a text editor, copy the content of the file, and execute in the PostgreSQL database.

5.  Execute the following PL/SQL function command to load data into the respective Intelligent Design tables.

    `select * from intdsgndata.fnconfigequmlibprobeinstdata();`

    **Note:** The above steps will only INSERT or UPDATE the data. Due to data constraints, there is no DELETE function.


**Parent topic:**[Data deployment](../../id_docs/installation/data_deploy.md)

