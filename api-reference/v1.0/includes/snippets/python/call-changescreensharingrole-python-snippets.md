---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ChangeScreenSharingRolePostRequestBody(
	role = ScreenSharingRole.Viewer,
)

await graph_client.communications.calls.by_call_id('call-id').change_screen_sharing_role.post(request_body = request_body)


```