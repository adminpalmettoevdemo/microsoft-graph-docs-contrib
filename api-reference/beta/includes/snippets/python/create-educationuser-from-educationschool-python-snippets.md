---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = ReferenceCreate(
	odata_id = "https://graph.microsoft.com/beta/education/users/14008",
)

await graph_client.education.schools.by_education_school_id('educationSchool-id').users.ref.post(request_body)


```