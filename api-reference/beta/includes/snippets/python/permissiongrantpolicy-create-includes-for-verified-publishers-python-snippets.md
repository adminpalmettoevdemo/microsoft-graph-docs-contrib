---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = PermissionGrantConditionSet(
	permission_type = PermissionType.Delegated,
	client_applications_from_verified_publisher_only = True,
)

result = await graph_client.policies.permission_grant_policies.by_permission_grant_policy_id('permissionGrantPolicy-id').includes.post(request_body)


```