---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = CategoriesRequestBuilder.CategoriesRequestBuilderGetQueryParameters(
		orderby = ["id"],
)

request_configuration = CategoriesRequestBuilder.CategoriesRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.education.classes.by_education_class_id('educationClass-id').assignments.by_education_assignment_id('educationAssignment-id').categories.get(request_configuration = request_configuration)


```