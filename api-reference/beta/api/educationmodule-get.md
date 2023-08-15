---
title: "Get educationModule"
description: "Get the properties and relationships of a module."
author: "cristobal-buenrostro"
ms.localizationpriority: medium
ms.prod: "education"
doc_type: apiPageType
---

# Get educationModule

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get the properties and relationships of a [module](../resources/educationModule.md). Only teachers, students, and applications with application permissions can perform this operation.

Students can only see published modules; teachers and applications with application permissions can see all modules in a class.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | EduCurricula.Read, EduCurricula.ReadWrite |
|Delegated (personal Microsoft account) |  Not supported.  |
|Application | EduCurricula.Read.All, EduCurricula.ReadWrite.All |

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/modules/{id}
```

## Optional query parameters
This method supports the  `$select` OData query parameter to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer {token}. Required.  |

## Request body
Don't supply a request body for this method.

## Response
If successful, this method returns a `200 OK` response code and an [educationModule](../resources/educationModule.md) object in the response body.

## Example
### Request
The following is an example of the request.

<!-- {
  "blockType": "request", 
  "name": "get_educationModule"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/education/classes/37d99af7-cfc5-4e3b-8566-f7d40e4a2070/modules/72a3879f-af73-4179-8a0e-4cb29c0fa369
```

### Response
The following is an example of the response.

>**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationModule"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#education/classes('cff47bf3-791b-4b0a-ad6b-92fa66917cc7')/modules/$entity",
    "displayName": "Math Practice - Fall",
    "description": "Description for Math Practice - Fall",
    "resourcesFolderUrl": "https://graph.microsoft.com/v1.0/drives/b!G2qSPDsXR0y4Bb2vODednawfynEIaD1OvPVeH4wbOp_3GV_mcV9MRLur9XlH200N/items/01IVG3LZKSPUPNBJYGQJCJUNG5SOCCD5DF",
    "isPinned": false,
    "status": "draft",
    "createdDateTime": "2023-07-24T22:02:06.8286097Z",
    "lastModifiedDateTime": "2023-07-24T22:02:44.2906308Z",
    "id": "72a3879f-af73-4179-8a0e-4cb29c0fa369",
    "createdBy": {
        "application": null,
        "device": null,
        "user": {
            "id": "cb1a4af3-0aba-4679-aa12-9f99bab0b61a",
            "displayName": null
        }
    },
    "lastModifiedBy": {
        "application": null,
        "device": null,
        "user": {
            "id": "cb1a4af3-0aba-4679-aa12-9f99bab0b61a",
            "displayName": null
        }
    }
}
```
