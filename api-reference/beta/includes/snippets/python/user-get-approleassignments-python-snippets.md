---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = AppRoleAssignmentsRequestBuilder.AppRoleAssignmentsRequestBuilderGetQueryParameters(
		count = True,
)

request_configuration = AppRoleAssignmentsRequestBuilder.AppRoleAssignmentsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)
request_configuration.headers.add("ConsistencyLevel", "eventual")


result = await graph_client.users.by_user_id('user-id').app_role_assignments.get(request_configuration = request_configuration)


```