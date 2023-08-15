---
title: "List module resources"
description: "Get all the resources associated with a module."
author: "cristobal-buenrostro"
ms.localizationpriority: medium
ms.prod: "education"
doc_type: apiPageType
---

# List module resources

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get all the [educationModuleResource](../resources/educationmoduleresource.md) objects associated with a [module](../resources/educationmodule.md). Only teachers, students, and applications with application permissions can perform this operation.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) |  EduCurricula.Read, EduCurricula.ReadWrite |
|Delegated (personal Microsoft account) |  Not supported.  |
|Application | EduCurricula.Read.All, EduCurricula.ReadWrite.All | 

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/modules/{id}/resources
```

## Optional query parameters

This method supports the `$expand` OData query parameter to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).


## Request headers
| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer {token}. Required.  |

## Request body
Don't supply a request body for this method.

## Response
If successful, this method returns a `200 OK` response code and a collection of [educationModuleResource](../resources/educationmoduleresource.md) objects in the response body.

## Example
### Request
The following is an example of the request.

<!-- {
  "blockType": "request",
  "name": "get_moduleresources_1"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/37d99af7-cfc5-4e3b-8566-f7d40e4a2070/modules/ba8e4215-4fb2-4dba-abe7-a8f2585177d3/resources
```

### Response
The following is an example of the response. 

>**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationModuleResource",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#education/classes('37d99af7-cfc5-4e3b-8566-f7d40e4a2070')/modules('74b318fa-e882-4dad-8e1c-dab091b12fe7')/resources",
    "value": [{
        "id": "291f3577-7e48-4faa-8bde-f0b9bbdab5eb",
        "resource": {
            "@odata.type": "#microsoft.graph.educationLinkResource",
            "displayName": "2023-07-26T21_22_29_804Z",
            "createdDateTime": "2023-07-25T21:22:30.1455092Z",
            "lastModifiedDateTime": "2023-07-25T21:22:30.1455106Z",
            "link": "https://www.bing.com",
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
    }, 
    {
        "id": "bfbf27cb-2316-47f0-81d4-7bb028f01964",
        "resource": {
            "@odata.type": "#microsoft.graph.educationLinkedAssignmentResource",
            "displayName": "2023-07-26T21_22_48_707Z",
            "createdDateTime": "2023-07-25T21:22:49.2808156Z",
            "lastModifiedDateTime": "2023-07-25T21:22:49.2808174Z",
            "url": "https://graph.microsoft.com/beta/education/classes/37d99af7-cfc5-4e3b-8566-f7d40e4a2070/assignments/b563da70-710e-4a9b-ba86-94a4d73e5d21/",
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
    }, 
    {
        "id": "151c668c-6c77-495e-a28e-c02fa155375a",
        "resource": {
            "@odata.type": "#microsoft.graph.educationWordResource",
            "displayName": "test_2023-07-26T21_22_51_471Z.docx",
            "createdDateTime": "2023-07-25T21:22:53.549826Z",
            "lastModifiedDateTime": "2023-07-25T21:22:53.5498285Z",
            "fileUrl": "https://graph.microsoft.com/v1.0/drives/b!-Ik2sRPLDEWy_bR8l75jfeDcpXQcRKVOmcml10NQLQ1F2UVvTgEnTKi0GO59dbCL/items/01VANVJQ23DHK5BYNOKJCZOUJZJBOAOUZP",
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
    }]
}
```
