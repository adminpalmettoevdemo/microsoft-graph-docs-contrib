---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = RemoveAllAccessForUserPostRequestBody(
	user = TeamworkUserIdentity(
		odata_type = "microsoft.graph.teamworkUserIdentity",
	),
)

await graph_client.chats.by_chat_id('chat-id').remove_all_access_for_user.post(request_body)


```