---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = PermissionGrantConditionSet(
	permission_type = PermissionType.Delegated,
	client_applications_from_verified_publisher_only = True,
)

result = await graph_client.policies.permission_grant_policies.by_permission_grant_policie_id('permissionGrantPolicy-id').includes.post(request_body = request_body)


```