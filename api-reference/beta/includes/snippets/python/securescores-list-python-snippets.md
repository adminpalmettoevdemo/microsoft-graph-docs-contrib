---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = SecureScoresRequestBuilder.SecureScoresRequestBuilderGetQueryParameters(
		top = 1,
)

request_configuration = SecureScoresRequestBuilder.SecureScoresRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.security.secure_scores.get(request_configuration = request_configuration)


```