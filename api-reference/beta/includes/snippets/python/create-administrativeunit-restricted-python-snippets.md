---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = AdministrativeUnit(
	display_name = "Executive Division",
	description = "Executive division administration",
	is_member_management_restricted = True,
)

result = await graph_client.administrative_units.post(request_body = request_body)


```