# Aspect Template Manager receives PCELL template data

The Aspect Template Manager provides an API endpoint that accepts PCELL template data in JSON format. This allows transfer PCELL definitions directly into Intelligent Design.

## API Endpoint

-   **Method:**

    POST \(JSON Format\)

-   **URL:**

    `POST /api/v1/abls/masterdata/template/import-pcell`


## Swagger Reference

You can view the API definition and test the endpoint through Swagger UI: `https://{application FQDN}/api/v1/abls/masterdata/swagger-ui/index.html#/aspect-template-controller/importPcells`

## Authentication

A valid Bearer Token is required to access this API. For instructions on generating a token, see [Obtaining a Bearer token](obtain_bearer_token.md).

## Request Body Format

The endpoint expects PCELL template data in JSON format.

**Example JSON:**

```
[
  {
    "name":"PCELL name",
    "description":"description",
    "ext":{
      "owner": "owner",
      "lastAuthor": "author",
      "lastModified":"2023/07/21 19:19:24", 
      "version":"1.1",
      "restricted":"",
      "categories":"FET"
    },
    "metaData": [
      {
        "name": "aspect name",
        "type": "numeric",
        "description": "description",
        "range": {"min": 0, "max": 100},
        "required": true,
        "defaultValue": "10",
        "scale": null
        "value": "",
        "items": null
        "ext": {
          "Prompt": "prompt",
          "editable": "yes"
        }
      }
    ]
  }
]

```

## Metadata Guidelines

-   **parameters**: stored as an array
-   **type** can be: "string", "numeric", "enumeration", or "boolean"
-   **type**= numeric
-   -   **scale = 0** → integer \(no decimals\)
-   **scale = 1** → up to one decimal place
-   **scale = null** → no decimal limit
-   **range = null** → no range limit
-   **range = \{"min":0, "max":100\}** → value must be between 0–100 \(inclusive\)

-   **type**= enumeration
    -   **items**: list of allowed values

**ext field**

-   Additional metadata in JSON format

**value field**

-   Always "" in templates; actual data will be stored as a string.

## Optional: Specify Projects and teams

You can add an `"assignment"` entry to the JSON schema to specify an associated project and restrict access to specific teams. The `"restrictedToTeam"` field is optional.

**Example JSON:**

```
],
“assignment”: [
    {“project”:”ProjectABC”, “restrictedToTeam”: [“teamX”] },
    {“project”:”ProjectDEF”, “restrictedToTeam”: [“teamX”, “teamY”] },
    {“project”:”ProjectGHI”, “restrictedToTeam”: [] },
    {“project”:”ProjectJKL”}
]
}
```

If no `"assignment"` entry is specified, the PCELL is globally accessible. If an `"assignment"` specifies a project, only that project can access the PCELL. If an `"assignment"` specifies both a project and `"restrictedToTeam"`, the PCELL is accessible only to that project and the members of that team. When the API is called, the `"assignment"` entry is replaced with the new data provided. If no `"assignment"` entry is included, and all existing assignment data is removed.

