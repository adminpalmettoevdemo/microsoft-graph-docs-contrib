---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ReferenceCreate(
	odata_id = "https://graph.microsoft.com/v1.0/education/users/14008",
)

await graph_client.education.schools.by_school_id('educationSchool-id').users.ref.post(request_body = request_body)


```