---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = TeamsAppSettings(
	odata_type = "#microsoft.graph.teamsAppSettings",
	is_chat_resource_specific_consent_enabled = True,
)

result = await graph_client.teamwork.team_app_settings.patch(request_body = request_body)


```