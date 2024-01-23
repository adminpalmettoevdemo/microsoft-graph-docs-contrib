---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = RiskyUsersRequestBuilder.RiskyUsersRequestBuilderGetQueryParameters(
		filter = "riskLevel eq microsoft.graph.riskLevel'medium'",
)

request_configuration = RiskyUsersRequestBuilder.RiskyUsersRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.identity_protection.risky_users.get(request_configuration = request_configuration)


```