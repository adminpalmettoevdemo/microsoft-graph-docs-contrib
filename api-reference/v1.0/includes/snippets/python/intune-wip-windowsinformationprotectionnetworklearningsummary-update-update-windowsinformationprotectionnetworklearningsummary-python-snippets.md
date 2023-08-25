---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = WindowsInformationProtectionNetworkLearningSummary(
	odata_type = "#microsoft.graph.windowsInformationProtectionNetworkLearningSummary",
	url = "Url value",
	device_count = 11,
)

result = await graph_client.device_management.window_information_protection_network_learning_summaries.by_window_information_protection_network_learning_summarie_id('windowsInformationProtectionNetworkLearningSummary-id').patch(request_body = request_body)


```