---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ExtensionProperty(
	name = "jobGroupTracker",
	data_type = "String",
	target_objects = [
		"User",
	]
)

result = await graph_client.applications.by_application_id('application-id').extension_properties.post(request_body = request_body)


```