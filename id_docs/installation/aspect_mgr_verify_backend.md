# Verifying the existence of prerequisite backend services and data

Aspect manager – essential aspect template definition

1.  Access the **Aspect Manager** Swagger interface on the target system.

2.  Expand `aspect-template-controller`.

3.  Expand the `POST /template/search` section.

4.  Click **Try it out**.

5.  5. Repeat the following steps for `NEXT_PUBLIC_ID_ASPECT_PROJECT`, `NEXT_PUBLIC_ID_ASPECT_MACRO`, `NEXT_PUBLIC_ID_ASPECT_DEVICE`, and `NEXT_PUBLIC_ID_ASPECT_PADSET`:

    1.  Enter a value for the **Request body** using the format in the following sample.

        **Example:** "Project Aspect Template" = `NEXT_PUBLIC_ID_ASPECT_PROJECT`.

        ```
        {
          "filters": [
            {
              "key": "name",
              "operator": "EQUAL",
              "field_type": "STRING",
              "logical_operator": "AND",
              "value": "Project Aspect template"
            }
          ],
          "page": 0,
          "size": 10
        }
        
        ```


**Parent topic:**[Aspect Template content](../../id_docs/installation/aspect_template_content.md)

