---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = ResizeCloudPcPostRequestBody(
	target_service_plan_id = "30d0e128-de93-41dc-89ec-33d84bb662a0",
)

await graph_client.device_management.managed_devices.by_managed_device_id('managedDevice-id').resize_cloud_pc.post(request_body)


```