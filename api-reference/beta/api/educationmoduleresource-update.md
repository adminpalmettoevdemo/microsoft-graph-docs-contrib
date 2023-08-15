---
title: "Update educationModuleResource"
description: "Update an education module resource."
ms.localizationpriority: medium
author: "cristobal-buenrostro"
ms.prod: "education"
doc_type: apiPageType
---

# Update educationModuleResource

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update a [resource](../resources/educationmoduleresource.md) in a [module](../resources/educationmodule.md). Only teachers can perform this operation.

The only one property that can be updated is **displayName**, for all resource types.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) |  EduCurricula.ReadWrite  |
|Delegated (personal Microsoft account) |  Not supported.  |
|Application | Not supported.  | 

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/classes/{class-id}/modules/{module-id}/resources/{resource-id}
```
## Request headers
| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer {token}. Required.  |
| Content-Type  | application/json  |

## Request body
In the request body, supply the new value for the **displayName** field that will be updated.

## Response
If successful, this method returns a `200 OK` response code and an [educationModuleResource](../resources/educationmoduleresource.md) object in the response body.

## Examples
### Request
The following is an example of the request.

<!-- {
  "blockType": "request",
  "name": "create_educationmoduleresource_patch"
}-->
```http
PATCH https://graph.microsoft.com/beta/education/classes/0b78e924-9623-49d8-b444-23bfabafa4fe/modules/fa1f6b67-7da6-458d-82fd-0d671df7bc31/resources/2fb5e262-611b-4672-8f55-1236b7f2804a
Content-type: application/json

{
    "resource": {
        "displayName" : "new pdf file patched.pdf"
    }
}
```

### Response
The following is an example of the response. 

>**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationExcelResource"
} -->
```http
HTTP/1.1 200 Ok
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#education/classes('0b78e924-9623-49d8-b444-23bfabafa4fe')/modules('fa1f6b67-7da6-458d-82fd-0d671df7bc31')/resources/$entity",
    "id": "2fb5e262-611b-4672-8f55-1236b7f2804a",
    "resource": {
        "@odata.type": "#microsoft.graph.educationFileResource",
        "displayName": "new pdf file patched.pdf",
        "createdDateTime": "2023-04-19T20:56:36.6529565Z",
        "lastModifiedDateTime": "2023-04-19T20:56:36.6529598Z",
        "fileUrl": "https://graph.microsoft.com/v1.0/drives/b!b8MR4rrk6kK793yj5m0azKvekbG46dBGsI2G7Vlzar_XjshebPh4RIbAjeFl67oU/items/01LGT6P7HL7I7CL2W3VNAYPD67G6SBIEB7",
        "createdBy": {
            "application": null,
            "device": null,
            "user": {
                "id": "93f30bbf-7f10-4dbb-a5bd-b59f75d4f690",
                "displayName": null
            }
        },
        "lastModifiedBy": {
            "application": null,
            "device": null,
            "user": {
                "id": "93f30bbf-7f10-4dbb-a5bd-b59f75d4f690",
                "displayName": null
            }
        }
    }
}
```
