---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ConversationThread(
	is_locked = True,
)

result = await graph_client.groups.by_group_id('group-id').threads.by_thread_id('conversationThread-id').patch(request_body = request_body)


```