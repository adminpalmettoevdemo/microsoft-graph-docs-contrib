---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = DeltaRequestBuilder.DeltaRequestBuilderGetQueryParameters(
		deltatoken = "sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw",
)

request_configuration = DeltaRequestBuilder.DeltaRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.groups.delta.get(request_configuration = request_configuration)


```