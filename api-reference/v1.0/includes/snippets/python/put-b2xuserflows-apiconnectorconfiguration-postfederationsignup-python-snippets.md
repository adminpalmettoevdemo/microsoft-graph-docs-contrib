---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ReferenceUpdate(
	odata_id = "https://graph.microsoft.com/v1.0/identity/apiConnectors/{id}",
)

await graph_client.identity.b2x_user_flows.by_b2x_user_flow_id('b2xIdentityUserFlow-id').api_connector_configuration.post_federation_signup.ref.put(request_body = request_body)


```