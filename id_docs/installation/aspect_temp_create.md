# Creating Aspect Template data

User manager – essential user permission

**Parent topic:**[Aspect Template content](../../id_docs/installation/aspect_template_content.md)

## Creating a template group

1.  Access the **Aspect Manager** Swagger interface on the target system.

2.  Expand `aspect-template-group-controller`.

3.  Expand the `POST /template-group` section.

4.  Click **Try it out**.

5.  Enter a value for the **Request body** using the format in the following sample.

    ```
    {
      "name": "A sample template group",
      "description": "A sample template group"
    }
    
    ```

6.  Click **Execute**.

7.  7. Obtain `data > id` of **Response** \(referred later as `groupId`\) for use in [Adding a template to a group](#id_uw3_mn4_s2c).


## Adding a template to a group

1.  Access the **Aspect Manager** Swagger interface on the target system.

2.  Expand `aspect-template-controller`.

3.  Expand the `POST /template` section.

4.  Click **Try it out**.

5.  Enter a value for the **Request body** using the format in the following sample and the `groupId` value from [Creating a template group](#id_dhd_4n4_s2c).

    ```
    {
          "name": "A sample template",
          "description": "A sample template for XXX entity",
          "status": “Active",
          "metaData": [
        {
          "name": "type",
          "type": "enumeration",
          "description": "description of aspect",
          "items": ["NFET", "PFET"],
          "required": true,
          "defaultValue": "NFET",
          "value": ""
        },
        …
       ],
       "groupId": 100
       ]
    
    ```


