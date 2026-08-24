# Creating a Project

**Note:** Only Project Administrators can create, edit, or delete Projects. Project Administrators can edit the Project's purpose field during Project creation.

1.  In the Project user interface, click the **Project** tab, and then click **Create Project** above the menu bar. The **Create a Project** modal opens.

2.  In the modal, complete the fields that are shown in the following table.

    |Attribute|Description|
    |---------|-----------|
    |**Project Name**|Name of the Project.|
    |**Technology**|Technology associated with the project.|
    |**Project Type**|Classification of the project. Testsite or Kerf Library.|
    |**Teams**|Teams that are assigned to the project.|
    |**Coordinator ID**|Coordinator responsible for the project.|
    |**Centerline Prefix**|Five-digit prefix generated for centerline model naming. Default value = **Auto-generated**.|
    |**Padset Collection**|Optional padset collection that is linked to the project.|
    |**Purpose** The **Purpose** field is only required for Testsite Projects.|The Purpose field defaults to the following values: Device, FEOL, HOL, BEOL GRV; DOE, YIELD, REL, MODELLING, EXP, PRECISION\_RESISTOR, PROCESS, SRAM, TECHDEV, EFUSE, ESD, LITHO, MIMCAP, PASSIVES, and FUNCTIONA.|
    |**Description**|Optional project description.|

3.  Click **Next**.

4.  Select **Edit** in the row for any Aspects you want to modify.

    |Aspect|Description|Default value|
    |------|-----------|-------------|
    |**beolStack**|List of BEOL metal stacks for the project.|M1|
    |**cOrient**|Design data preferred PC orientation. Supported values are H \(implies notch right data orientation\) or V \(implies notch down data orientation\). Device coordinates vary in y for notch right/H and vary in x for notch down/V for a standard placement.|V|
    |**iltAdmin**|Inline test administrator.|N/A|
    |**stepPlanPN**|Part number for step plan. Seven character designation.|N/A|
    |**waferDiameter**|Hardware diameter.|300|
    |**xChipIndices**|Inline test x-axis index used to determine chip location.|1|
    |**xSiteCenterOffset**|X-axis reticle offset.|1|
    |**xSiteOrigin**|X-axis origin for inline test stepping.|1|
    |**xSiteSize**|Reticle size, including kerf, in mm \(stepping periodicity\).|20.0|
    |**yChipIndices**|Inline test y-axis index used to determine chip location.|1|
    |**ySiteCenterOffset**|Y-axis reticle offset.|1|
    |**ySiteOrigin**|Y-axis origin for inline test stepping.|1|
    |**ySiteSize**|Reticle size, including kerf, in mm \(stepping periodicity\).|20.0|

5.  Click **Next**.

6.  To attach files to the Project, click **Upload**, navigate to the file, then click **Open**.

7.  Click **Next**.

8.  Review the Project information, then click **Create**.

    **Note:** When a Project's status is **Design Finalized**, ID users cannot add additional Macros and can edit only existing Macros. However, Project Administrators can add additional macros.


**Parent topic:**[Projects](../id_docs/id_projects.md)

