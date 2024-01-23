---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = DevicesRequestBuilder.DevicesRequestBuilderGetQueryParameters(
		search = "\"displayName:Android\"",
		count = True,
)

request_configuration = DevicesRequestBuilder.DevicesRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)
request_configuration.headers.add("ConsistencyLevel", "eventual")


result = await graph_client.devices.get(request_configuration = request_configuration)


```