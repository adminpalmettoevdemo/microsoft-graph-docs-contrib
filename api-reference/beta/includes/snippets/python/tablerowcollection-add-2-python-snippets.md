---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = AddPostRequestBody(
	index = None,
	values = [
		[
			1,
			2,
			3,
		]
		[
			4,
			5,
			6,
		]
	]
)

result = await graph_client.drives.by_drive_id('drive-id').items.by_item_id('driveItem-id').workbook.tables.by_table_id('workbookTable-id').rows.add.post(request_body = request_body)


```