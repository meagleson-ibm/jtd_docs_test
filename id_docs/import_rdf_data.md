# Importing data from a Reticle Definition File

Project administrators can import macro aspect data, including X and Y coordinates for each macro in a project, from a Reticle Definition File \(RDF\).

An RDF file contains all of the xPos and yPos coordinates of all the macros on a test site. A project administrator can import the RDF file to reconcile all the macros on that project. Essentially, it replaces any zeros in X/Y positions that exist because the coordinates were unknown when the macros were created. The import process also produces a list of any mismatches or missing macros in the RDF file.

1.  On the Project details page, select **Actions** \> **Import RDF file**.

2.  Click Add file, navigate to the RDF \(.txt\) file you want to import, and click **Open**.

3.  Click **Import**.

    The data is imported from the RDF file. If there are any discrepancies between the data in the RDF and the data in Intelligent Design, an import warning is displayed. To download and view all errors in a .csv file, click **Download full list of errors** in the Import warning window.


**Parent topic:**[Macros](../id_docs/macros.md)

