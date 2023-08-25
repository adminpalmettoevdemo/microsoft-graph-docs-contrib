---
title: "Get multiTenantOrganizationMember"
description: "Get a tenant and its properties in the multi-tenant organization."
author: "rolyon"
ms.localizationpriority: medium
ms.prod: "identity-and-sign-in"
doc_type: apiPageType
---

# Get multiTenantOrganizationMember
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a tenant and its properties in the multi-tenant organization.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|MultiTenantOrganization.ReadBasic.All, MultiTenantOrganization.Read.All, MultiTenantOrganization.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|MultiTenantOrganization.ReadBasic.All, MultiTenantOrganization.Read.All, MultiTenantOrganization.ReadWrite.All|

If called with MultiTenantOrganization.ReadBasic.All permission, the caller can only read the **displayName** and **tenantId** properties.

[!INCLUDE [rbac-multitenantorganization-apis-read](../includes/rbac-for-apis/rbac-multitenantorganization-apis-read.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /tenantRelationships/multiTenantOrganization/tenants/{tenantId}
```

## Optional query parameters
This method supports the `$select` OData query parameter to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [multiTenantOrganizationMember](../resources/multitenantorganizationmember.md) object in the response body.

## Examples

The following example gets a tenant and its properties in the multi-tenant organization.

### Request

<!-- {
  "blockType": "request",
  "name": "get_multitenantorganizationmember"
}
-->
``` http
GET https://graph.microsoft.com/beta/tenantRelationships/multiTenantOrganization/tenants/1fd6544e-e994-4de2-9f1b-787b51c7d325
```


### Response

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.multiTenantOrganizationMember"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#tenantRelationships/multiTenantOrganization/tenants/$entity",
    "tenantId": "1fd6544e-e994-4de2-9f1b-787b51c7d325",
    "displayName": "Contoso",
    "addedDateTime": "2023-05-26T22:05:23Z",
    "joinedDateTime": null,
    "addedByTenantId": "1fd6544e-e994-4de2-9f1b-787b51c7d325",
    "role": "owner",
    "state": "active",
    "transitionDetails": null
}
```

If an update is in progress, `transitionDetails` lists information about the update. The following response indicates the role is being changed from member to owner.

``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#tenantRelationships/multiTenantOrganization/tenants/$entity",
    "tenantId": "5036a0a0-a7a4-4933-9086-5dd54535dd6e",
    "displayName": "Woodgrove Bank",
    "addedDateTime": "2023-05-27T21:52:40Z",
    "joinedDateTime": null,
    "addedByTenantId": "1fd6544e-e994-4de2-9f1b-787b51c7d325",
    "role": "member",
    "state": "pending",
    "transitionDetails": {
        "desiredState": "active",
        "desiredRole": "owner",
        "status": "notStarted",
        "details": null
    }
}
```

