---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = Group(
	description = "Contoso Life v2.0",
	display_name = "Contoso Life Renewed",
)

result = await graph_client.groups.by_group_id('group-id').patch(request_body)


```