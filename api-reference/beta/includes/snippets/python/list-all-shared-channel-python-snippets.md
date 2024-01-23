---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = AllChannelsRequestBuilder.AllChannelsRequestBuilderGetQueryParameters(
		filter = "membershipType eq 'shared'",
)

request_configuration = AllChannelsRequestBuilder.AllChannelsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.teams.by_team_id('team-id').all_channels.get(request_configuration = request_configuration)


```