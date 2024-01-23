---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = ResourcesRequestBuilder.ResourcesRequestBuilderGetQueryParameters(
		orderby = ["resource/createdDateTime"],
)

request_configuration = ResourcesRequestBuilder.ResourcesRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.education.classes.by_education_class_id('educationClass-id').assignments.by_education_assignment_id('educationAssignment-id').submissions.by_education_submission_id('educationSubmission-id').resources.get(request_configuration = request_configuration)


```