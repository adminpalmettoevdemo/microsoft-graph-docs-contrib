---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = Alert(
	assigned_to = "String",
	closed_date_time = "String (timestamp)",
	comments = [
		"String",
	],
	feedback = AlertFeedback.Unknown,
	status = AlertStatus.Unknown,
	tags = [
		"String",
	],
	vendor_information = SecurityVendorInformation(
		provider = "String",
		vendor = "String",
	),
)

request_configuration = AlertItemRequestBuilder.AlertItemRequestBuilderPatchRequestConfiguration()
request_configuration.headers.add("Prefer", "return=representation")


result = await graph_client.security.alerts.by_alert_id('alert-id').patch(request_body, request_configuration = request_configuration)


```