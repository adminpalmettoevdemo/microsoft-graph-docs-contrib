---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)


request_configuration = JobsRequestBuilder.JobsRequestBuilderGetRequestConfiguration()
request_configuration.headers.add("Authorization", "Bearer {Token}")


result = await graph_client.service_principals.by_service_principal_id('servicePrincipal-id').synchronization.jobs.get(request_configuration = request_configuration)


```