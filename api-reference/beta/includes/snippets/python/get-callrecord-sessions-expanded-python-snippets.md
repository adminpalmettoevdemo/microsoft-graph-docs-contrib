---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = SessionsRequestBuilder.SessionsRequestBuilderGetQueryParameters(
		expand = ["segments"],
)

request_configuration = SessionsRequestBuilder.SessionsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.communications.call_records.by_call_record_id('callRecord-id').sessions.get(request_configuration = request_configuration)


```