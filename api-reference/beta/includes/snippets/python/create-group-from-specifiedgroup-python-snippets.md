---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ReferenceCreate(
	odata_id = "https://graph.microsoft.com/odata/groups('dc3d2ce5-7c5e-4dca-a0ef-2145bf6e53ef')",
)

await graph_client.policies.mobile_device_management_policies.by_mobile_device_management_policie_id('mobilityManagementPolicy-id').included_groups.ref.post(request_body = request_body)


```