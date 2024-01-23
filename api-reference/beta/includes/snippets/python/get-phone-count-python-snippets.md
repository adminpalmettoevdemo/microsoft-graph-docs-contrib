---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = ContactsRequestBuilder.ContactsRequestBuilderGetQueryParameters(
		search = "\"displayName:wa\"",
		count = True,
)

request_configuration = ContactsRequestBuilder.ContactsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)
request_configuration.headers.add("ConsistencyLevel", "eventual")


result = await graph_client.contacts.get(request_configuration = request_configuration)


```