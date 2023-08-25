---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = EnrollAssetsPostRequestBody(
	update_category = UpdateCategory.Feature,
	assets = [
		AzureADDevice(
			odata_type = "#microsoft.graph.windowsUpdates.azureADDevice",
			id = "String (identifier)",
		),
	]
)

await graph_client.admin.windows.updates.updatable_assets.microsoft_graph_window_update_enroll_assets.post(request_body = request_body)


```