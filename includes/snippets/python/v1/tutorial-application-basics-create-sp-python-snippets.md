---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ServicePrincipal(
	app_id = "fc876dd1-6bcb-4304-b9b6-18ddf1526b62",
)

result = await graph_client.service_principals.post(request_body = request_body)


```