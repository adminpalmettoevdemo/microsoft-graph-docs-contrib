---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = AttributeSetsRequestBuilder.AttributeSetsRequestBuilderGetQueryParameters(
		top = 10,
)

request_configuration = AttributeSetsRequestBuilder.AttributeSetsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.directory.attribute_sets.get(request_configuration = request_configuration)


```