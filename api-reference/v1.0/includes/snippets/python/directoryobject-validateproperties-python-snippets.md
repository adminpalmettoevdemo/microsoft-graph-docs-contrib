---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ValidatePropertiesPostRequestBody(
	entity_type = "Group",
	display_name = "Myprefix_test_mysuffix",
	mail_nickname = "Myprefix_test_mysuffix",
	on_behalf_of_user_id = UUID("onBehalfOfUserId-value"),
)

await graph_client.directory_objects.validate_properties.post(request_body = request_body)


```