---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = RejectPostRequestBody(
	reason = RejectReason.Busy,
)

await graph_client.communications.calls.by_call_id('call-id').reject.post(request_body = request_body)


```