---
title: "Create multiTenantOrganization"
description: "Create a new multi-tenant organization."
author: "rolyon"
ms.localizationpriority: medium
ms.prod: "identity-and-sign-in"
doc_type: apiPageType
---

# Create multiTenantOrganization
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new multi-tenant organization. By default, the creator tenant becomes an owner tenant upon successful creation. Only owner tenants can manage a multi-tenant organization.

To allow for asynchronous processing, you must wait a **minimum of 2 hours** between creation and joining a multi-tenant organization.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|MultiTenantOrganization.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|MultiTenantOrganization.ReadWrite.All|

[!INCLUDE [rbac-multitenantorganization-apis-write](../includes/rbac-for-apis/rbac-multitenantorganization-apis-write.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PUT /tenantRelationships/multiTenantOrganization
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [multiTenantOrganization](../resources/multitenantorganization.md) object.

You can specify the following properties when creating a **multiTenantOrganization**.

|Property|Type|Description|
|:---|:---|:---|
|displayName|String|Display name of the multi-tenant organization. Required.|
|description|String|Description of the multi-tenant organization. Optional.|



## Response

If successful, this method returns a `201 Created` response code and a [multiTenantOrganization](../resources/multitenantorganization.md) object in the response body.

## Examples

The following example creates a new multi-tenant organization.

### Request

<!-- {
  "blockType": "request",
  "name": "create_multitenantorganization_from_"
}
-->
``` http
PUT https://graph.microsoft.com/beta/tenantRelationships/multiTenantOrganization
Content-Type: application/json

{
  "displayName": "Contoso organization",
  "description": "Multi-tenant organization between Contoso, Fabrikam, and Woodgrove Bank"
}
```


### Response

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.multiTenantOrganization"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#tenantRelationships/multiTenantOrganization/$entity",
    "id": "6d8b39e5-039a-4034-bf3a-e0b4f8cd60b6",
    "createdDateTime": "2023-05-26T22:05:23Z",
    "displayName": "Contoso organization",
    "description": "Multi-tenant organization between Contoso, Fabrikam, and Woodgrove Bank",
    "state": "active"
}
```

