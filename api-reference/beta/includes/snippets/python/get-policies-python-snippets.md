---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = PoliciesRequestBuilder.PoliciesRequestBuilderGetQueryParameters(
		filter = "displayName eq 'SimplePolicy1' or displayName eq 'SimplePolicy2'",
)

request_configuration = PoliciesRequestBuilder.PoliciesRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.identity.conditional_access.policies.get(request_configuration = request_configuration)


```