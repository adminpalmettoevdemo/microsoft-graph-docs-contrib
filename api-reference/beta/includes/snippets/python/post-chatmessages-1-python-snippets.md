---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = ChatMessage(
	body = ItemBody(
		content = "Hello world",
	),
)

result = await graph_client.chats.by_chat_id('chat-id').messages.post(request_body)


```