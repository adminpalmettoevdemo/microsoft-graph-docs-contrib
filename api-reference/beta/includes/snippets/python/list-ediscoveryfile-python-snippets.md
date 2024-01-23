---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = FilesRequestBuilder.FilesRequestBuilderGetQueryParameters(
		top = 5,
)

request_configuration = FilesRequestBuilder.FilesRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.security.cases.ediscovery_cases.by_ediscovery_case_id('ediscoveryCase-id').review_sets.by_ediscovery_review_set_id('ediscoveryReviewSet-id').files.get(request_configuration = request_configuration)


```