---
title: "List permissionGrants of a user"
description: "List all resource-specific permission grants of a user."
author: "edle"
ms.localizationpriority: high
ms.prod: "microsoft-teams"
doc_type: apiPageType
---

# List permissionGrants of a user

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

List all [resource-specific permission grants](../resources/resourcespecificpermissiongrant.md) of a [user](../resources/user.md). This list specifies the Azure Active Directory apps that have access to the **user**, along with the corresponding kind of resource-specific access that each app has.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission Type                        | Permissions (from least to most privileged)                                                                                                                                                        |
| :------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Delegated (work or school account)     | ResourceSpecificPermissionGrant.ReadForUser, TeamsAppInstallation.ReadForUser, TeamsAppInstallation.ReadWriteSelfForUser, TeamsAppInstallation.ReadWriteForUser, TeamsAppInstallation.ReadWriteConsentSelfForUser,  TeamsAppInstallation.ReadWriteConsentForUser                                    |
| Delegated (personal Microsoft account) | Not supported.                                                                                                                                                                                     |
| Application                            | ResourceSpecificPermissionGrant.ReadForUser.All, TeamsAppInstallation.ReadForUser.All, TeamsAppInstallation.ReadWriteSelfForUser.All, TeamsAppInstallation.ReadWriteForUser.All, TeamsAppInstallation.ReadWriteConsentSelfForUser.All,  TeamsAppInstallation.ReadWriteConsentForUser.All |

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /users/{user-id}/permissionGrants
```

## Optional query parameters

This operation does not support the [OData query parameters](/graph/query-parameters) to customize the response.

## Request headers

| Header           | Value                      |
| :--------------- | :------------------------- |
| Authorization    | Bearer {token}. Required.  |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [resourceSpecificPermissionGrant](../resources/resourcespecificpermissiongrant.md) objects in the response body.

## Examples

### Request

The following is an example of the request.

<!-- {
  "blockType": "request",
  "name": "user_list_permission_grants",
  "sampleKeys": ["2f39ffba-51ca-4d2d-a66f-a020a83ce208"]
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/users/2f39ffba-51ca-4d2d-a66f-a020a83ce208/permissionGrants
```

### Response

The following is an example of the response.

>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.resourceSpecificPermissionGrant"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#permissionGrants",
  "value": [
    {
      "id": "Y2VkZGEyMWUtYTUwZS00ZDI3LWEyZjAtOTk0MTMwMGY3Y2I1IyNDaGF0U2V0dGluZ3MuUmVhZFdyaXRlLkNoYXQjI0FwcGxpY2F0aW9u",
      "clientAppId": "fdebf36e-8b3a-4b00-99fb-2e4d1da706d6",
      "resourceAppId": "00000003-0000-0000-c000-000000000000",
      "clientId": "771b9da9-2260-41eb-a587-4d936e4aa08c",
      "permissionType": "Application",
      "permission": "TeamsActivity.Send.User"
    }
  ]
}
```

## See also

- [List permission grants of a chat](chat-list-permissiongrants.md)
- [List permission grants of a group](group-list-permissiongrants.md)
- [List permission grants of a team](team-list-permissiongrants.md)
