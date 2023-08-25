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
				permission_value = "OnlineMeeting.ReadBasic.Chat",
				permission_type = TeamsAppResourceSpecificPermissionType.Delegated,
			),
			TeamsAppResourceSpecificPermission(
				permission_value = "ChatMember.Read.Chat",
				permission_type = TeamsAppResourceSpecificPermissionType.Application,
			),
		]
	),
)

await graph_client.chats.by_chat_id('chat-id').installed_apps.by_installed_app_id('teamsAppInstallation-id').upgrade.post(request_body = request_body)


```