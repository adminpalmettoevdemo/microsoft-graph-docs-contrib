---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = ClearPresencePostRequestBody(
	session_id = "22553876-f5ab-4529-bffb-cfe50aa89f87",
)

await graph_client.users.by_user_id('user-id').presence.clear_presence.post(request_body)


```