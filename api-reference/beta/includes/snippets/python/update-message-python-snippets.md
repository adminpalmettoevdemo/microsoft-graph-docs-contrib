---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = Message(
	subject = "subject-value",
	body = ItemBody(
		content_type = BodyType.Text,
		content = "content-value",
	),
	inference_classification = InferenceClassificationType.Other,
)

result = await graph_client.me.messages.by_message_id('message-id').patch(request_body)


```