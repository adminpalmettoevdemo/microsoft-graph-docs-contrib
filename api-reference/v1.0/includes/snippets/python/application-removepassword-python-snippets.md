---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = RemovePasswordPostRequestBody(
	key_id = UUID("f0b0b335-1d71-4883-8f98-567911bfdca6"),
)

await graph_client.applications.by_application_id('application-id').remove_password.post(request_body)


```