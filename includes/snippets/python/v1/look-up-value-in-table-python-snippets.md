---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = VlookupPostRequestBody(
	lookup_value = "pear",
	table_array = Json(
		additional_data = {
				"address" : "Sheet1!B2:C7",
		}
	),
	col_index_num = 2,
	range_lookup = False,
)

request_configuration = VlookupRequestBuilder.VlookupRequestBuilderPostRequestConfiguration()
request_configuration.headers.add("workbook-session-id", "{session-id}")


result = await graph_client.drives.by_drive_id('drive-id').items.by_drive_item_id('driveItem-id').workbook.functions.vlookup.post(request_body, request_configuration = request_configuration)


```