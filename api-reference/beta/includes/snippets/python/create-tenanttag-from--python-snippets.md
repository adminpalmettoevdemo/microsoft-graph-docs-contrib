---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = TenantTag(
	display_name = "Support",
	description = "Tenants that have purchased extended support",
)

result = await graph_client.tenant_relationships.managed_tenants.tenant_tags.post(request_body)


```