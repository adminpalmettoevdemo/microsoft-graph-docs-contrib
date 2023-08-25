---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = UpgradePostRequestBody(
	consented_permission_set = TeamsAppPermissionSet(
		resource_specific_permissions = [
			TeamsAppResourceSpecificPermission(
				permission_value = "Channel.Create.Group",
				permission_type = TeamsAppResourceSpecificPermissionType.Application,
			),
			TeamsAppResourceSpecificPermission(
				permission_value = "ChannelMeeting.ReadBasic.Group",
				permission_type = TeamsAppResourceSpecificPermissionType.Delegated,
			),
		]
	),
)

await graph_client.teams.by_team_id('team-id').installed_apps.by_installed_app_id('teamsAppInstallation-id').upgrade.post(request_body = request_body)


```