---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = SetOrderPostRequestBody(
	new_assignment_order = AssignmentOrder(
		order = [
			"City",
			"extension_GUID_ShoeSize",
		],
	),
)

await graph_client.identity.b2x_user_flows.by_b2x_identity_user_flow_id('b2xIdentityUserFlow-id').user_attribute_assignments.set_order.post(request_body)


```