---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = OAuth2PermissionGrant(
	scope = "User.Read.All",
)

result = await graph_client.oauth2_permission_grants.by_oauth2_permission_grant_id('oAuth2PermissionGrant-id').patch(request_body = request_body)


```