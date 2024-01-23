---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = AuthorizationSystemsRequestBuilder.AuthorizationSystemsRequestBuilderGetQueryParameters(
		filter = "authorizationSystemType eq 'gcp'",
)

request_configuration = AuthorizationSystemsRequestBuilder.AuthorizationSystemsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.external.authorization_systems.get(request_configuration = request_configuration)


```