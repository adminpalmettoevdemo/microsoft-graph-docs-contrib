---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = User(
	additional_data = {
			"extkmpdyld2_graph_learn_courses" : (
				course_type = "Instructor-led",
				course_id = None,
			),
	}
)

result = await graph_client.users.by_user_id('user-id').patch(request_body = request_body)


```