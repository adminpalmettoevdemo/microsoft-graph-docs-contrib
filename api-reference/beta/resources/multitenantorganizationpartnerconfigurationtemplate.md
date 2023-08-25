---
title: "multiTenantOrganizationPartnerConfigurationTemplate resource type"
description: "Defines an optional cross-tenant access policy template with inbound and outbound partner configuration settings for multi-tenant organization tenants."
author: "rolyon"
ms.localizationpriority: medium
ms.prod: "identity-and-sign-in"
doc_type: resourcePageType
---

# multiTenantOrganizationPartnerConfigurationTemplate resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Defines an optional cross-tenant access policy template with inbound and outbound partner configuration settings for multi-tenant organization tenants. Each tenant has its own template. For more information, see [crossTenantAccessPolicyConfigurationPartner resource type](../resources/crosstenantaccesspolicyconfigurationpartner.md).

* If your tenant is joining a multi-tenant organization, the template is applicable to the partner configuration settings for all multi-tenant organization tenants.
* If another tenant joins your multi-tenant organization, the template is applicable only to the partner configuration settings of the newly joined multi-tenant organization tenant.

Whether the template is applied to the partner configuration settings of relevant tenants is configurable with the `templateApplicationLevel` property.

* If the template is configured to apply, it is only applied to partner configuration properties where the corresponding template property has a non-null value.

In its default and unconfigured state, where all template properties (other than `templateApplicationLevel`) are null, the template has no effect on partner configuration settings.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[Get multiTenantOrganizationPartnerConfigurationTemplate](../api/multitenantorganizationpartnerconfigurationtemplate-get.md)|[multiTenantOrganizationPartnerConfigurationTemplate](../resources/multitenantorganizationpartnerconfigurationtemplate.md)|Get the inbound and outbound partner configuration settings of the template.|
|[Update multiTenantOrganizationPartnerConfigurationTemplate](../api/multitenantorganizationpartnerconfigurationtemplate-update.md)|[multiTenantOrganizationPartnerConfigurationTemplate](../resources/multitenantorganizationpartnerconfigurationtemplate.md)|Update the inbound and outbound partner configuration settings of the template.|
|[resetToDefaultSettings](../api/multitenantorganizationpartnerconfigurationtemplate-resettodefaultsettings.md)|None|Reset the inbound and outbound partner configuration settings of the template to the default values.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|ID of the template. Key.|
|automaticUserConsentSettings|[inboundOutboundPolicyConfiguration](../resources/inboundoutboundpolicyconfiguration.md)|Determines the partner-specific configuration for automatic user consent settings. Unless specifically configured, the **inboundAllowed** and **outboundAllowed** properties are `null` and inherit from the default settings, which is always `false`.|
|b2bCollaborationInbound|[crossTenantAccessPolicyB2BSetting](../resources/crosstenantaccesspolicyb2bsetting.md)|Defines your partner-specific configuration for users from other organizations accessing your resources via Azure AD B2B collaboration.|
|b2bCollaborationOutbound|[crossTenantAccessPolicyB2BSetting](../resources/crosstenantaccesspolicyb2bsetting.md)|Defines your partner-specific configuration for users in your organization going outbound to access resources in another organization via Azure AD B2B collaboration.|
|b2bDirectConnectInbound|[crossTenantAccessPolicyB2BSetting](../resources/crosstenantaccesspolicyb2bsetting.md)|Defines your partner-specific configuration for users from other organizations accessing your resources via Azure B2B direct connect.|
|b2bDirectConnectOutbound|[crossTenantAccessPolicyB2BSetting](../resources/crosstenantaccesspolicyb2bsetting.md)|Defines your partner-specific configuration for users in your organization going outbound to access resources in another organization via Azure AD B2B direct connect.|
|inboundTrust|[crossTenantAccessPolicyInboundTrust](../resources/crosstenantaccesspolicyinboundtrust.md)|Determines the partner-specific configuration for trusting other Conditional Access claims from external Azure AD organizations.|
|templateApplicationLevel|templateApplicationLevel|Specifies whether the template will be applied to partner configuration settings of certain tenants. The possible values are: `none`, `newPartners`, `existingPartners`, `unknownFutureValue`. You can also specify multiple values like `newPartners,existingPartners` (default). `none` indicates the template is not applied to any new or existing partner tenants. `newPartners` indicates the template is applied to new partner tenants. `existingPartners` indicates the template is applied to existing partner tenants, those who already had partner-specific partner configurations in place.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.multiTenantOrganizationPartnerConfigurationTemplate",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.multiTenantOrganizationPartnerConfigurationTemplate",
  "inboundTrust": {
    "@odata.type": "microsoft.graph.crossTenantAccessPolicyInboundTrust"
  },
  "b2bCollaborationOutbound": {
    "@odata.type": "microsoft.graph.crossTenantAccessPolicyB2BSetting"
  },
  "b2bCollaborationInbound": {
    "@odata.type": "microsoft.graph.crossTenantAccessPolicyB2BSetting"
  },
  "b2bDirectConnectOutbound": {
    "@odata.type": "microsoft.graph.crossTenantAccessPolicyB2BSetting"
  },
  "b2bDirectConnectInbound": {
    "@odata.type": "microsoft.graph.crossTenantAccessPolicyB2BSetting"
  },
  "automaticUserConsentSettings": {
    "@odata.type": "microsoft.graph.inboundOutboundPolicyConfiguration"
  },
  "templateApplicationLevel": "String"
}
```

