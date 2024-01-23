---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = MeRequestBuilder.MeRequestBuilderGetQueryParameters(
		select = ["id","displayName","mail","mobilePhone"],
		expand = ["extensions"],
)

request_configuration = MeRequestBuilder.MeRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.me.get(request_configuration = request_configuration)


```