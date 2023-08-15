---
title: "Add or delete custom attributes on a profile card (preview)"
description: "Learn how to use the profile card API in Microsoft Graph to make additional attributes visible and add or delete custom attributes on a profile card."
author: "PollyNincevic"
ms.localizationpriority: high
ms.prod: "people"
ms.custom: scenarios:getting-started
---

# Add or delete custom attributes on a profile card using the profile card API (preview)

On the profile card in Microsoft 365, you can find information about users that is stored and maintained by your organization, for example **Job title** or **Office location**.

Use the [profileCardProperty](/graph/api/resources/profilecardproperty) resource to show additional properties from Azure AD on profile cards for an organization by:

* Making additional attributes visible
* Adding custom attributes

Additional properties display in the **Contact** section of the profile card in Microsoft 365.

You can also [delete](/graph/api/profilecardproperty-delete?view=graph-rest-beta&preserve-view=true) custom attributes from profile cards of the organization.

> [!NOTE]
> Operations on the **profileCardProperty** resource that use delegated permissions require the signed-in user to have a tenant administrator or global administrator role.

## Make additional attributes visible

You can make the following attributes from Azure Active Directory (Azure AD) visible on users' profile cards. These attributes are *not case-sensitive*:

* `UserPrincipalName`
* `Fax`
* `StreetAddress`
* `PostalCode`
* `StateOrProvince`
* `Alias`

The following table shows how the Azure AD attributes correspond with properties of the Microsoft Graph [user](/graph/api/resources/user) entity.

| Azure AD attribute | User entity property |
| ------------------ | -------------------- |
| UserPrincipalName | userPrincipalName |
| Fax | faxNumber |
| StreetAddress | streetAddress |
| PostalCode | postalCode |
| StateOrProvince | state |
| Alias | mailNickname |

You can add any of these attributes to the profile card by configuring your [people admin settings](/graph/api/resources/peopleadminsettings) and adding the attribute as the **directoryPropertyName** property of a **profileCardProperty** in Microsoft Graph. When you make additional attributes visible, you must use the property names for `en-us`. You don't have to add localized values. The additional properties will automatically be shown in the language settings that the user has specified for Microsoft 365.

> [!IMPORTANT]
> When adding an attribute to profile card, it takes up to 24 hours for the addition to be displayed.

## Configure profile card properties using the Microsoft Graph REST API

### Example

The following example displays the `Alias` attribute on the profile card.

``` http
POST https://graph.microsoft.com/beta/admin/people/profileCardProperties
Content-Type: application/json

{
  "directoryPropertyName": "Alias"
}
```

> **Note:** The `/organization/{organizationId}/settings` path is deprecated. Going forward, use the `/admin/people` path.

If successful, the response returns a `201 OK` response code and a **profileCardProperty** object in the response body. The value for the `Alias` attribute would be displayed on a user's profile card.

``` http
HTTP/1.1 201 OK
Content-type: application/json

{
  "directoryPropertyName": "Alias",
  "annotations": []
}
```

## Add a custom attribute

You can add any of the 15 Azure AD [custom extension attributes](/graph/api/resources/onpremisesextensionattributes) to users' profile cards by configuring your organization settings and [adding the corresponding value as a profileCardProperty](/graph/api/peopleadminsettings-post-profilecardproperties) in Microsoft Graph. You can add one **profileCardProperty** resource at a time.

It takes up to 24 hours for the changes to show on profile cards.

Custom properties are not searchable and can't be used to search for people across Microsoft apps and services.

The following table shows how the Azure AD custom extension attribute names correspond to the supported values for the **directoryPropertyName** property of the [profileCardProperty](/graph/api/resources/profilecardproperty) resource. These Azure AD custom extension attribute names are *not case-sensitive*:

| Azure AD custom extension attribute | Value to specify as directoryPropertyName |
| ----------------------------------- | ----------------------------------------- |
| extensionAttribute1 | customAttribute1 |
| extensionAttribute2 | customAttribute2 |
| extensionAttribute3 | customAttribute3 |
| extensionAttribute4 | customAttribute4 |
| extensionAttribute5 | customAttribute5 |
| extensionAttribute6 | customAttribute6 |
| extensionAttribute7 | customAttribute7 |
| extensionAttribute8 | customAttribute8 |
| extensionAttribute9 | customAttribute9 |
| extensionAttribute10 | customAttribute10 |
| extensionAttribute11 | customAttribute11 |
| extensionAttribute12 | customAttribute12 |
| extensionAttribute13 | customAttribute13 |
| extensionAttribute14 | customAttribute14 |
| extensionAttribute15 | customAttribute15 |

### Example

The following example adds the first Azure AD custom extension attribute to the profile card, using the display name **Cost center**. For users that have set their language settings to German, the display name will be **Kostenstelle**.

#### Request

``` http
POST https://graph.microsoft.com/beta/admin/people/profileCardProperties
Content-Type: application/json

{
  "directoryPropertyName": "customAttribute1",
  "annotations": [
    {
      "displayName": "Cost center",
      "localizations": [
        {
          "languageTag": "de",
          "displayName": "Kostenstelle"
        }
      ]
    }
  ]
}
```

> **Note:** The `/organization/{organizationId}/settings` path is deprecated. Going forward, use the `/admin/people` path.

If a language is not supported, the property name will be shown with the default value.

If successful, the response returns a `201 OK` response code and a **profileCardProperty** object in the response body. In this example you can assume that the profile card displays **Kostenstelle** for all users that have set their language settings to German on the profile card. For all other users, **Cost center** will be displayed on the profile card.

#### Response

``` http
HTTP/1.1 201 OK
Content-type: application/json

{
  "directoryPropertyName": "customAttribute1",
  "annotations": [
    {
      "displayName": "Cost center",
      "localizations": [
        {
          "languageTag": "de",
          "displayName": "Kostenstelle"
        }
      ]
    }
  ]
}
```

## Delete a custom attribute

Following the same mapping between Azure AD custom extension attributes and profile card custom attributes (such as `customAttribute1`) as described in the preceding section [Adding a custom attribute](/graph/add-properties-profilecard#adding-a-custom-attribute), you can delete a custom attribute using the [delete](/graph/api/profilecardproperty-delete?view=graph-rest-beta&preserve-view=true) operation, as shown in the following example.

### Example

The following example deletes the custom attribute `customAttribute5` from the organization settings. A successful deletion returns `HTTP 204`.

#### Request

``` http
DELETE https://graph.microsoft.com/beta/admin/people/profileCardProperties/customAttribute5
```

> **Note:** The `/organization/{organizationId}/settings` path is deprecated. Going forward, use the `/admin/people` path.

#### Response

``` http
HTTP/1.1 204 No Content
```

## Configure profile card properties using PowerShell

You can use the [Microsoft Graph PowerShell SDK](/powershell/microsoftgraph/installation) to configure profile card properties in your organization.

### Prerequisites

- **PowerShell module** - Install [module version 1.24.0 or higher](https://www.powershellgallery.com/packages/Microsoft.Graph).
- **.NET Framework** - Install [.NET Framework 4.7.2](https://dotnet.microsoft.com/download/dotnet-framework) or a higher version.

> [!NOTE]
> Because profile card properties commands are only available in beta, switch to the beta profile before running the command.
> ```powershell
>    Select-MgProfile beta
> ```

### Confirm your current settings

To get profile card properties configuration for an organization, use the following command.

```powershell
   Get-MgBetaAdminPeopleProfileCardProperty
```

To get a profile card property configuration in an organization, use the following command.

```powershell
   Get-MgBetaAdminPeopleProfileCardProperty -ProfileCardPropertyId $profileCardPropertyId
```

> [!NOTE]
> The get commands require `PeopleSettings.Read.All` permission. To create a Microsoft Graph session with a specific required scope, use the following command and consent to requested permissions.
>
> ```powershell
>    Connect-MgGraph -Scopes "PeopleSettings.Read.All"
> ```

> **Note:** The `Get-MgBetaOrganizationSettingProfileCardProperty` command is deprecated. Going forward, use the `Get-MgBetaAdminPeopleProfileCardProperty` command.

### Create profile card properties in your organization

You can use the Microsoft Graph PowerShell module to make both additional AAD profile card  properties, and the 15 customizable AAD profile card properties available in your organization.

> [!NOTE]
> The create command requires `PeopleSettings.ReadWrite.All` permission. To create a Microsoft Graph session with a specific required scope, use the following command and consent to requested permissions.
>
> ```powershell
>    Connect-MgGraph -Scopes "PeopleSettings.ReadWrite.All","PeopleSettings.Read.All"
> ```

Use the following command.

```powershell
$params = @{
	directoryPropertyName = "CustomAttribute1"
	annotations = @(
		@{
			displayName = "Cost Center"
			localizations = @(
				@{
					languageTag = "ru-RU"
					displayName = "центр затрат"
				}
			)
		}
	)
}

New-MgBetaAdminPeopleProfileCardProperty -BodyParameter $params
```

> **Note:** The `New-MgBetaOrganizationSettingProfileCardProperty` command is deprecated. Going forward, use the `New-MgBetaAdminPeopleProfileCardProperty` command.

### Update profile card properties in your organization

You can use the Microsoft Graph PowerShell module to update profile card properties available in your organization.

> [!NOTE]
> The update command requires `PeopleSettings.ReadWrite.All` permission. To create a Microsoft Graph session with a specific required scope, use the following command and consent to requested permissions.
>
> ```powershell
>    Connect-MgGraph -Scopes "PeopleSettings.ReadWrite.All","PeopleSettings.Read.All"
> ```

Use the following command, where you replace `$profileCardPropertyId` with the id of the property to be updated.

```powershell
$params = @{
	annotations = @(
		@{
			localizations = @(
				@{
					languageTag = "no-NB"
					displayName = "Kostnads Senter"
				}
			)
		}
	)
}

Update-MgBetaAdminPeopleProfileCardProperty -ProfileCardPropertyId $profileCardPropertyId -BodyParameter $params
```
> **Note:** The `Update-MgBetaOrganizationSettingProfileCardProperty` command is deprecated. Going forward, use the `Update-MgBetaAdminPeopleProfileCardProperty` command.

### Delete profile card properties in your organization

You can use the Microsoft Graph PowerShell module to remove profile card properties from your organization.

> [!NOTE]
> The delete command requires `PeopleSettings.ReadWrite.All` permission. To create a Microsoft Graph session with a specific required scope, use the following command and consent to requested permissions.
>
> ```powershell
>    Connect-MgGraph -Scopes "PeopleSettings.ReadWrite.All","PeopleSettings.Read.All"
> ```

Use the following command, where you replace `$profileCardPropertyId` with the id of the property to be deleted.

```powershell
 Remove-MgBetaAdminPeopleProfileCardProperty -ProfileCardPropertyId $profileCardPropertyId
```
> **Note:** The `Remove-MgBetaOrganizationSettingProfileCardProperty` command is deprecated. Going forward, use the `Remove-MgBetaAdminPeopleProfileCardProperty` command.

## See also

- [onPremisesExtensionAttributes resource type](/graph/api/resources/onpremisesextensionattributes)
- [User resource type](/graph/api/resources/user)
- [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer)
- [Get profileCardProperty](/graph/api/profilecardproperty-get)
