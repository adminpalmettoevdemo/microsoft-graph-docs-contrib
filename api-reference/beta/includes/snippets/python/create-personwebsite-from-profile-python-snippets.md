---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = PersonWebsite(
	categories = [
		"football",
	]
	display_name = "Lyn Damer",
	web_url = "www.lyndamer.no",
)

result = await graph_client.me.profile.websites.post(request_body = request_body)


```