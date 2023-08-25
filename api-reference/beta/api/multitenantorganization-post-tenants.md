---
title: "Add multiTenantOrganizationMember"
description: "Add a tenant to a multi-tenant organization."
author: "rolyon"
ms.localizationpriority: medium
ms.prod: "identity-and-sign-in"
doc_type: apiPageType
---

# Add multiTenantOrganizationMember
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Add a tenant to a multi-tenant organization. The administrator of an owner tenant has the permissions to add tenants to the multi-tenant organization. The added tenant is in the pending state until the administrator of the added tenant joins the multi-tenant organization by submitting a join request. Note that a tenant can be part of only one multi-tenant organization.

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
POST /tenantRelationships/multiTenantOrganization/tenants
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [multiTenantOrganizationMember](../resources/multitenantorganizationmember.md) object.

You can specify the following properties when creating a **multiTenantOrganizationMember**.

|Property|Type|Description|
|:---|:---|:---|
|tenantId|String|Tenant ID of the Azure Active Directory tenant to add to the multi-tenant organization. Required.|
|displayName|String|Display name of the tenant added to the multi-tenant organization. Currently, cannot be changed once set. Required.|
|role|multiTenantOrganizationMemberRole|Role of the tenant in the multi-tenant organization. The possible values are: `owner`, `member` (default), `unknownFutureValue`. Optional.|


## Response

If successful, this method returns a `201 Created` response code and a [multiTenantOrganizationMember](../resources/multitenantorganizationmember.md) object in the response body. If the tenant is already pending or active in this multi-tenant organization, you get a 'Request_BadRequest' error.

## Examples

The following example adds the Fabrikam tenant to the multi-tenant organization.

### Request

<!-- {
  "blockType": "request",
  "name": "create_multitenantorganizationmember_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/tenantRelationships/multiTenantOrganization/tenants
Content-Type: application/json

{
  "tenantId": "4a12efe6-aa14-4d03-8dff-88fc89e2e2ad",
  "displayName": "Fabrikam"
}
```


### Response

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.multiTenantOrganizationMember"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#tenantRelationships/multiTenantOrganization/tenants/$entity",
    "tenantId": "4a12efe6-aa14-4d03-8dff-88fc89e2e2ad",
    "displayName": "Fabrikam",
    "addedDateTime": "2023-05-27T19:24:29Z",
    "joinedDateTime": null,
    "addedByTenantId": "1fd6544e-e994-4de2-9f1b-787b51c7d325",
    "role": "member",
    "state": "pending",
    "transitionDetails": null
}
```

If tenant is already pending or active in this multi-tenant organization, you get a 'Request_BadRequest' error.

```http
HTTP/1.1 400 Bad Request
Content-Type: application/json

{
    "error": {
        "code": "Request_BadRequest",
        "message": "Tenant is already being added in Multi-Tenant Organization.",
        "innerError": {
            "date": "2023-05-27T20:56:14",
            "request-id": "a1e5973c-66f1-4853-9e3d-39e6b4f606d1",
            "client-request-id": "651548c3-e864-4509-837b-4f5d4cf546a5"
        }
    }
}
```
