---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = OnenoteSection(
	display_name = "Section name",
)

result = await graph_client.me.onenote.notebooks.by_notebook_id('notebook-id').sections.post(request_body = request_body)


```