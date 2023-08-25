---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = TranslateExchangeIdsPostRequestBody(
	input_ids = [
		"{rest-formatted-id-1}",
		"{rest-formatted-id-2}",
	]
	source_id_type = ExchangeIdFormat.RestId,
	target_id_type = ExchangeIdFormat.RestImmutableEntryId,
)

result = await graph_client.me.translate_exchange_ids.post(request_body = request_body)


```