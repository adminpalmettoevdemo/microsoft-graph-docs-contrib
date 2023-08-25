---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = UpdatePolicy(
	odata_type = "#microsoft.graph.windowsUpdates.updatePolicy",
	deployment_settings = DeploymentSettings(
		odata_type = "microsoft.graph.windowsUpdates.deploymentSettings",
		schedule = ScheduleSettings(
			gradual_rollout = RateDrivenRolloutSettings(
				odata_type = "#microsoft.graph.windowsUpdates.rateDrivenRolloutSettings",
				duration_between_offers = "P1D",
				additional_data = {
						"device_per_offer" : 1000,
				}
			),
		),
	),
)

result = await graph_client.admin.windows.updates.update_policies.by_update_policie_id('updatePolicy-id').patch(request_body = request_body)


```