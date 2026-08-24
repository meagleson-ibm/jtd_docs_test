# Updating Aspect Template data

User manager – essential user permission

1.  Access the **Aspect Manager** Swagger interface on the target system.

2.  Expand `aspect-template-controller`.

3.  Expand the `POST /template/search` section.

4.  Click **Try it out**.

5.  Replace the filters value with a template name for search:

    ```
    {
      "filters": [
        {
          "key": "name",
          "operator": "EQUAL",
          "field_type": "STRING",
          "value": "Template name for search"
        }
      ],
      "page": 0,
      "size": 10
    }
    
    ```

6.  Click **Execute**.

7.  In the **Response body** section, copy the first entry of data array \(example in bold\):

    ```
    "metadata": {
        …
      },
      "data": [**
        \{
         “id”: xxx,
         “version”: xxxx,
         …
         “metaData”: \[
         \(actual data\)
         \]
         “groupId”: xxx
        \}
       \]
    **
    ```

8.  Replace `\(actual data\)` with the new value.

9.  Expand the `POST /template` section.

10. Copy the entire JSON payload to **Request body**.

    **Note:** Leave `groupId` value as-is.

11. Click **Execute**.


**Parent topic:**[Aspect Template content](../../id_docs/installation/aspect_template_content.md)

