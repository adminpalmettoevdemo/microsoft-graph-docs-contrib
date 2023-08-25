---
title: "Get multiTenantOrganizationIdentitySyncPolicyTemplate"
description: "Get the cross-tenant access policy template with user synchronization settings for a multi-tenant organization."
author: "rolyon"
ms.localizationpriority: medium
ms.prod: "identity-and-sign-in"
doc_type: apiPageType
---

# Get multiTenantOrganizationIdentitySyncPolicyTemplate
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get the cross-tenant access policy template with user synchronization settings for a multi-tenant organization.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|Policy.Read.All, Policy.ReadWrite.CrossTenantAccess|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Policy.Read.All, Policy.ReadWrite.CrossTenantAccess|

[!INCLUDE [rbac-multitenantorganization-apis-read](../includes/rbac-for-apis/rbac-multitenantorganization-apis-read.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /policies/crossTenantAccessPolicy/templates/multiTenantOrganizationIdentitySynchronization
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

If successful, this method returns a `200 OK` response code and a [multiTenantOrganizationIdentitySyncPolicyTemplate](../resources/multitenantorganizationidentitysyncpolicytemplate.md) object in the response body.

## Examples

The following example gets the user synchronization settings of the template.

### Request

<!-- {
  "blockType": "request",
  "name": "get_multitenantorganizationidentitysyncpolicytemplate"
}
-->
``` http
GET https://graph.microsoft.com/beta/policies/crossTenantAccessPolicy/templates/multiTenantOrganizationIdentitySynchronization
```

### Response

The following example response shows the unconfigured (or reset) state of the cross-tenant access policy template for user synchronization settings for multi-tenant organization tenants.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.multiTenantOrganizationIdentitySyncPolicyTemplate"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#policies/crossTenantAccessPolicy/templates/multiTenantOrganizationIdentitySynchronization/$entity",
    "templateApplicationLevel": "newPartners,existingPartners",
    "id": "0e7aad84-cb46-4b8e-a881-522ef25939f1",
    "userSyncInbound": {
        "isSyncAllowed": null
    }
}
```

The following example response shows a configured state of the cross-tenant access policy template for user synchronization settings, after inbound user synchronization has been configured.

``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#policies/crossTenantAccessPolicy/templates/multiTenantOrganizationIdentitySynchronization/$entity",
    "id": "e1a11ff3-01f1-4c48-9784-b9d931571474",
    "templateApplicationLevel": "newPartners,existingPartners",
    "userSyncInbound": {
        "isSyncAllowed": true
    }
}
```
