---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = ItemEmail(
	display_name = "Business Email",
	type = EmailType.Work,
)

result = await graph_client.users.by_user_id('user-id').profile.emails.by_item_email_id('itemEmail-id').patch(request_body)


```