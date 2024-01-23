---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = UsageRightsRequestBuilder.UsageRightsRequestBuilderGetQueryParameters(
		filter = "state in ('active', 'suspended') and serviceIdentifier in ('ABCD')",
)

request_configuration = UsageRightsRequestBuilder.UsageRightsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.users.by_user_id('user-id').usage_rights.get(request_configuration = request_configuration)


```