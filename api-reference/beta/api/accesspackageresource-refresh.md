---
title: "accessPackageResource: refresh"
description: "Refresh an accessPackageResource object from an origin system."
author: "vikama-microsoft"
ms.localizationpriority: medium
ms.prod: "governance"
doc_type: apiPageType
---

# accessPackageResource: refresh
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

In [Azure AD entitlement management](../resources/entitlementmanagement-overview.md), refresh the [accessPackageResource](../resources/accesspackageresource.md) object to fetch the latest details for **displayName**, **description**, and **resourceType** from the origin system. For the `AadApplication` originSystem, this operation also updates the **displayName** and **description** for the [accessPackageResourceRole](../resources/accesspackageresourcerole.md). 



## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
| Delegated (work or school account) | EntitlementManagement.ReadWrite.All |
| Delegated (personal Microsoft account) | Not supported. |
| Application | EntitlementManagement.ReadWrite.All |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /identityGovernance/entitlementManagement/accessPackageCatalogs/{accessPackageCatalogId}/accessPackageResources/{accessPackageResourceId}/refresh
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Don't supply a request body for this method.

## Response

If successful, this action returns a `200 OK` response code and no object in the response body.


## Examples

### Request
The following is an example of a request.
<!-- {
  "blockType": "request",
  "name": "accesspackageresourcethis.refresh"
}
-->
``` http
POST https://graph.microsoft.com/beta/identityGovernance/entitlementManagement/accessPackageCatalogs/16b6a9de-f519-4bd2-86cb-793808f70230/accessPackageResources/b078b6f9-15c1-423b-864f-994ccf8d6fbf/refresh
```


### Response

The following example shows the response.

<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK
```
