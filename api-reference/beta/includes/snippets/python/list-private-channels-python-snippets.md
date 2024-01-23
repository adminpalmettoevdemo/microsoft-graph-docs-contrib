---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = ChannelsRequestBuilder.ChannelsRequestBuilderGetQueryParameters(
		filter = "membershipType eq 'private'",
)

request_configuration = ChannelsRequestBuilder.ChannelsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.teams.by_team_id('team-id').channels.get(request_configuration = request_configuration)


```