---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = ReferenceCreate(
	odata_id = "https://graph.microsoft.com/beta/groups/{id}",
)

await graph_client.print.shares.by_printer_share_id('printerShare-id').allowed_groups.ref.post(request_body)


```