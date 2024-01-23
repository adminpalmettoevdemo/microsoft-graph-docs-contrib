---
title: "Update pronounsSettings"
description: "Update the properties of a pronounsSettings object in an organization."
author: "aymen-ms"
ms.localizationpriority: medium
ms.prod: "people"
doc_type: apiPageType
---

# Update pronounsSettings

Namespace: microsoft.graph

Update the properties of a [pronounsSettings](../resources/pronounssettings.md) object in an organization.

For more information on settings to manage pronouns support, see [Manage pronouns settings for an organization using the Microsoft Graph API](/graph/pronouns-configure-pronouns-availability).

[!INCLUDE [national-cloud-support](../../includes/global-only.md)]

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
| Delegated (work or school account)     | PeopleSettings.ReadWrite.All |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Not supported. |

>**Note:** Using delegated permissions for this operation requires the signed-in user to have a Global Administrator role.

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /admin/people/pronouns
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body

[!INCLUDE [table-intro](../../includes/update-property-table-intro.md)]

|Property|Type|Description|
|:---|:---|:---|
|isEnabledInOrganization|Boolean|`true` to enable pronouns in the organization; otherwise, `false`. The default value is `false`, and pronouns are disabled. Required.|

## Response

If successful, this method returns a `200 OK` response code and an updated [pronounsSettings](../resources/pronounssettings.md) object in the response body.

## Examples

### Request

The following example shows a request.

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_pronounssettings"
}
-->
``` http
PATCH https://graph.microsoft.com/v1.0/admin/people/pronouns
Content-Type: application/json

{
  "isEnabledInOrganization": true
}
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-pronounssettings-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/update-pronounssettings-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/update-pronounssettings-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/update-pronounssettings-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-pronounssettings-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/update-pronounssettings-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/update-pronounssettings-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response

The following example shows the response.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.pronounsSettings",
  "name": "update_pronounssettings"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "isEnabledInOrganization": true
}
```
