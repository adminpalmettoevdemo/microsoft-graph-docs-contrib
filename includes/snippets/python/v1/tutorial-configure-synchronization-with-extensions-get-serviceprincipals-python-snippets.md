---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = ServicePrincipalsRequestBuilder.ServicePrincipalsRequestBuilderGetQueryParameters(
		select = ["id","appId","displayName"],
		filter = "startswith(displayName, 'salesforce')",
)

request_configuration = ServicePrincipalsRequestBuilder.ServicePrincipalsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)
request_configuration.headers.add("Authorization", "Bearer {Token}")


result = await graph_client.service_principals.get(request_configuration = request_configuration)


```