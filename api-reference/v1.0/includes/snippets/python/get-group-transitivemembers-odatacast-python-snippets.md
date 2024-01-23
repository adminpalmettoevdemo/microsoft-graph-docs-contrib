---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = GroupRequestBuilder.GroupRequestBuilderGetQueryParameters(
		count = True,
)

request_configuration = GroupRequestBuilder.GroupRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)
request_configuration.headers.add("ConsistencyLevel", "eventual")


result = await graph_client.groups.by_group_id('group-id').transitive_members.graph_group.get(request_configuration = request_configuration)


```