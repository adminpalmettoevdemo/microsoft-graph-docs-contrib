---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = UsersRequestBuilder.UsersRequestBuilderGetQueryParameters(
		select = ["id","displayName","mail","identities"],
		filter = "endsWith(userPrincipalName,'",
)

request_configuration = UsersRequestBuilder.UsersRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)
request_configuration.headers.add("ConsistencyLevel", "eventual")


result = await graph_client.users.get(request_configuration = request_configuration)


```