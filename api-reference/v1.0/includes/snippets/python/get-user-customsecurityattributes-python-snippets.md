---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = UserItemRequestBuilder.UserItemRequestBuilderGetQueryParameters(
		select = ["customSecurityAttributes"],
)

request_configuration = UserItemRequestBuilder.UserItemRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.users.by_user_id('user-id').get(request_configuration = request_configuration)


```