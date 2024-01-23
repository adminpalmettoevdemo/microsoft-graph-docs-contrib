---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)


request_configuration = SubmissionsRequestBuilder.SubmissionsRequestBuilderGetRequestConfiguration()
request_configuration.headers.add("Prefer", "include-unknown-enum-members")


result = await graph_client.education.classes.by_education_class_id('educationClass-id').assignments.by_education_assignment_id('educationAssignment-id').submissions.get(request_configuration = request_configuration)


```