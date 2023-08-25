---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = UnifiedRoleManagementPolicyEnablementRule(
	odata_type = "#microsoft.graph.unifiedRoleManagementPolicyEnablementRule",
	id = "Enablement_Admin_Assignment",
	enabled_rules = [
		"Justification",
		"MultiFactorAuthentication",
	]
	target = UnifiedRoleManagementPolicyRuleTarget(
		odata_type = "microsoft.graph.unifiedRoleManagementPolicyRuleTarget",
		caller = "Admin",
		operations = [
			UnifiedRoleManagementPolicyRuleTargetOperations.All,
		]
		level = "Assignment",
		inheritable_settings = [
		]
		enforced_settings = [
		]
	),
)

result = await graph_client.policies.role_management_policies.by_role_management_policie_id('unifiedRoleManagementPolicy-id').rules.by_rule_id('unifiedRoleManagementPolicyRule-id').patch(request_body = request_body)


```