---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = RemovePasswordPostRequestBody(
	key_id = UUID("f0b0b335-1d71-4883-8f98-567911bfdca6"),
)

await graph_client.applications.by_application_id('application-id').remove_password.post(request_body = request_body)


```