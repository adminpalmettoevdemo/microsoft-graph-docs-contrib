---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = AppRoleAssignmentsRequestBuilder.AppRoleAssignmentsRequestBuilderGetQueryParameters(
		filter = "resourceId eq 8e881353-1735-45af-af21-ee1344582a4d",
)

request_configuration = AppRoleAssignmentsRequestBuilder.AppRoleAssignmentsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.users.by_user_id('user-id').app_role_assignments.get(request_configuration = request_configuration)


```