---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = ExportPersonalDataPostRequestBody(
	storage_location = "MyStorageAccount",
)

await graph_client.directory.inbound_shared_user_profiles.by_inbound_shared_user_profile_user_id('inboundSharedUserProfile-userId').export_personal_data.post(request_body)


```