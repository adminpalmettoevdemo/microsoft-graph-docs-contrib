---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = DeleteTiIndicatorsByExternalIdPostRequestBody(
	value = [
		"externalId-value1",
		"externalId-value2",
	]
)

result = await graph_client.security.ti_indicators.delete_ti_indicator_by_external_id.post(request_body = request_body)


```