---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = User(
	account_enabled = True,
	display_name = "Adele Vance",
	mail_nickname = "AdeleV",
	user_principal_name = "AdeleV@contoso.onmicrosoft.com",
	password_profile = PasswordProfile(
		force_change_password_next_sign_in = True,
		password = "xWwvJ]6NMw+bWH-d",
	),
)

result = await graph_client.users.post(request_body)


```