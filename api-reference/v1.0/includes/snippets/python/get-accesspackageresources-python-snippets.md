---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

query_params = ResourcesRequestBuilder.ResourcesRequestBuilderGetQueryParameters(
		expand = ["scopes"],
)

request_configuration = ResourcesRequestBuilder.ResourcesRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.identity_governance.entitlement_management.catalogs.by_catalog_id('accessPackageCatalog-id').resources.get(request_configuration = request_configuration)


```