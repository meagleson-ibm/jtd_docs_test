# Aspect variable tables setup

Before creating a TestPlan, it is necessary to prepare a variable table to store variables referenced by items such as Input Params and Output Params.

There are two types of variable tables available: The Technology variable table, and the `iltDeviceCode` and technology variable table.

## Technology variable table

This table defines variables for each Technology. When the same variable name is referenced within parameters, this table is used to retrieve the corresponding value, returning different values depending on the specific Technology.

The technology variable data is structured in JSON format, containing an array of objects. Each object includes the following properties:

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the variable.|
|value|String|String expression of the variable value.|
|description|String|Description of the variable.|

The following is the sample of technologyVariable with Technology entity.

```
{
      "name": "SampleTech",
      "description": "SampleTech",
      "active": true,
      "ownerId": "user1@sample.com,
      "groupId": "Test",
      "prTemplateGroupId": null,
      "prDefaultTemplateId": null,
      "technologyVariable": [
        {
          "name": "IonN",
          "value": "3.00E-03",
          "description": "Current Value when Device Type N is On"
        },
        {
          "name": "IonP",
          "value": "-3.00E-03",
          "description": "Current Value when Device Type P is On"
        },
        {
          "name": "Ioff_phvt",
          "value": "-3.00E-06",
          "description": "Current Value when Device Type P is On"
        },
        {
          "name": "dly",
          "value": "1.00E-03",
          "description": "Delay before Measurement"
        }
      ]
    }

```

After creating the technologyVariable field, add the record using the ProjectManager API with Swagger.

If you are updating an existing Technology record, first retrieve the existing record with `GET /technology/{id}`, update the `technologyVariable` field, and then submit the updated content via the API using a `create/update API POST /technology`.

## iltDeviceCode and technology variable table

This table first performs a pattern match on the `iltDeviceCodde` field of the target Device, retrieving the corresponding entry. Additionally, a different mapping is applied for each Technology.

If the `iltDeviceCodde` field matches multiple patterns, the pattern matching the characters closest to the beginning of the string is used. For example, "FN12T" matches both "F\*\*\*T" and "FN\*\*T," but "FN\*\*T," which matches up to the second character, is selected.

This table is managed as a single JSON-formatted array, with each element in the array structured as follows:

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the variable.|
|value|String|String expression of the variable value.|
|description|String|Description of the variable.|
|`iltDeviceCode`|String|Matching pattern for `iltDeviceCode`. `*` matches any character.|
|`metaInfo`|Array of Object|List of technology variable.|
|`metaInfo.technologyName`|String|Name of technology.|
|`metaInfo.technologyValue`|String|String expression of variable value for the technology. If the value is empty, parent level value is used. Reference to technology variable is also applicable \(example: `&Ioff_phvt`\)|

The following is an example of the JSON data format:

```
[
  {
    "name": "Ioff",
    "value": "3.00E-06",
    "description": "",
    "iltDeviceCode": "F***T",
    "metaInfo": [
      {
        "technologyName": "2HP",
        "technologyValue": ""
      },
      {
        "technologyName": "DDebug",
        "technologyValue": ""
      },
      {
        "technologyName": "DmacsDebug",
        "technologyValue": ""
      },
      {
        "technologyName": "Technology 1",
        "technologyValue": ""
      },
      {
        "technologyName": "Technology00",
        "technologyValue": ""
      },
      {
        "technologyName": "Technology01",
        "technologyValue": ""
      },
      {
        "technologyName": "Technology11",
        "technologyValue": ""
      }
    ]
  },
  {
    "name": "Ioff",
    "value": "3.00E-06",
    "description": "",
    "iltDeviceCode": "FN**T",
    "metaInfo": [
      {
        "technologyName": "2HP",
        "technologyValue": ""
      },
      {
        "technologyName": "DDebug",
        "technologyValue": ""
      },
      {
        "technologyName": "DmacsDebug",
        "technologyValue": ""
      },
      {
        "technologyName": "Technology 1",
        "technologyValue": ""
      },
      {
        "technologyName": "Technology00",
        "technologyValue": ""
      },
      {
        "technologyName": "Technology01",
        "technologyValue": ""
      },
      {
        "technologyName": "Technology11",
        "technologyValue": ""
      }
    ]
  }
]

```

This table is managed as a property of `TestPlanMgr`. Using the `config-svc`, set the following property in the `TestPlanMgr`:

|Name|Type|Description|
|----|----|-----------|
|`intldsgn.testplan.ilt-device-code`|String|Base64-encoded JSON string of the variable table.|

To create the Base64-encoded string, first save the JSON string to a file, then convert it using one of the following commands.

On Windows: `certutil -f -encode {inputfile} {outputfile}`

\(Use the value between `-----BEGIN CERTIFICATE-----` and `-----END CERTIFICATE-----`\)

On macOS: `cat {inputfile} | base64 > {outputfile}`

