---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = GetInaccessibleCloudPcReportsPostRequestBody(
	filter = "region eq 'westus2'",
	order_by = [
		"cloudPcId",
	],
	select = [
		"cloudPcId",
		"aadDeviceId",
		"cloudPcName",
		"userPrincipalName",
		"provisioningStatus",
		"region",
		"deviceHealthStatus",
		"deviceHealthStatusDateTime",
		"recentDeviceHealthFailureCount",
		"recentConnectionFailureCount",
		"systemStatus",
		"systemStatusDateTime",
	],
	top = 10,
	skip = 0,
)

await graph_client.device_management.virtual_endpoint.reports.get_inaccessible_cloud_pc_reports.post(request_body)


```